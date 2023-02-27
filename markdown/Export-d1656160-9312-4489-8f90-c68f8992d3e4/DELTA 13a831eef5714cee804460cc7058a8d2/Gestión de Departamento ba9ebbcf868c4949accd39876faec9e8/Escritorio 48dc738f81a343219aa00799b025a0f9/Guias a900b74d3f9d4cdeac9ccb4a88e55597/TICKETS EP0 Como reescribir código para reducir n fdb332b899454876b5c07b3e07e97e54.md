# TICKETS EP0: Como reescribir código para reducir nesting y complejidad

Must Read: Yes
Tags: Calidad, Desarrollo, Tickets

Este será el episodio 0 de *********************tickets*********************, como reescribir código para mejorar la calidad. Si lees un episodio, deja un comentario para saber si te sirvió, si se te hizo interesante, o si lo odiaste, así sabemos cuánto sirven estos documentos.

Repositorio de referencia: 

[GitHub - JuanManuelGlez/Div-Dev at d186a67ec12d9197232cd4878daa96f7766c1a68](https://github.com/JuanManuelGlez/Div-Dev/tree/d186a67ec12d9197232cd4878daa96f7766c1a68)

# Problemática

El siguiente fragmento es un endpoint del backend creado para *********************TICKETS*********************, el código es difícil de leer y comprender, debido a los multiples niveles de nesting con condicionales y callbacks*********************:*********************

```jsx
exports.login_post = (request, response, next) => {
  Usuario.findOne(request.body.correo)
    .then(([rows, fielData]) => {
      let error = 1;
      if (rows.length < 1) {
        response.status(200).json({ errores: error });
      } else {
        const usuario = new Usuario(
          rows[0].Nombre_Usuario,
          rows[0].Login,
          rows[0]["Contraseña"],
          rows[0].URL_Foto
        );
        bcrypt
          .compare(request.body.contrasenia, usuario.contrasenia_usuario)
          .then((doMatch) => {
            let error = 1;
            if (doMatch) {
              Usuario.getOneActive(usuario.login_usuario)
                .then(([rowsActive, fielData]) => {
                  error = 2;
                  if (rowsActive[0].Activo == 1) {
                    error = 0;
                    request.session.isLoggedIn = true;
                    request.session.usuario = usuario;
                    request.session.correo = usuario.login_usuario;
                    //console.log(request.session.usuario);
                    Usuario.getId(request.session.correo)
                      .then(([rowsid, fieldData]) => {
                        request.session.id_usuario = rowsid[0].Id_Usuario;
                        Usuario.fetchRolUsuario(request.session.id_usuario)
                          .then(([rowsprivilegios, fielData]) => {
                            let privilegios = [];
                            for (let privilegio in rowsprivilegios) {
                              privilegios.push(
                                rowsprivilegios[privilegio].Id_Privilegio
                              );
                            }
                            request.session.privilegios = privilegios;
                            return request.session.save((err) => {
                              response.status(200).json({ errores: error });
                            });
                          })
                          .catch((err) => {
                            console.log(err);
                          });
                      })
                      .catch((err) => {
                        console.log(err);
                      });
                  } else {
                    response.status(200).json({ errores: error });
                  }
                })
                .catch((err) => {
                  console.log(err);
                });
            } else {
              response.status(200).json({ errores: error });
            }
          })
          .catch((err) => {
            console.log(err);
          });
      }
    })
    .catch((error) => {
      console.log(error);
    });
};
```

En este fragmento existen varias prácticas que ************************************************************NO QUEREMOS VER EN NUEVO CÓDIGO!!!************************************************************

1. **Nesting intenso de condicionales**

```jsx
if () {
}
else {
	if () {
	}
	else {
		if () {
			}
			else {
					.....
			}
	}
}
```

1. **Nesting intenso de callbacks**

```jsx
fetch().then((something) => {
	something.then(foo => {
		foo.then( ...)	
	}).catch(...)
}).catch(...)
```

****************************************************PERO NO SE PREOCUPEN :))))****************************************************

Existe una sencilla solución.

### Nesting de condicionales

Siempre que sea posible, utiliza un escape temprano de la función. Si existe una condición que en su ****if**** o en su ********else******** solo realiza alguna función y termina en return, deja esta parte como el condicional, y el resto puede vivir fuera de un else.

Ejemplo:

```jsx
if (a < 1) {
	bla bla bla
} else {
	console.log("bad")
	return
}

// ======>
if (a >= 1) {
	console.log("bad")
	return
}

bla bla bla
```

De esta manera reducimos la complejidad de los condicionales y hace más fácil leer y entender el código.

Más información: [The early return pattern in JavaScript | Go Make Things](https://gomakethings.com/the-early-return-pattern-in-javascript/)

### Nesting de callbacks

En lugar de hacer uso directo de las interfaces de promesas (`then`, `catch`, `finally`), prefiere el uso de `async / await`.

Ejemplo:

```jsx
query.then(a => {
	secondQuery.then(b => {
		response.text(a + b);
	})
})

// =====>

const a = await query()
const b = await query()
return a + b;
```

De esta manera mejoramos la redacción del código asíncrono y resultará más sencillo mantenerlo.

Más información: [async function - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)

# Resultado final:

```jsx
exports.login_post = async (request, response, next) => {
  const [rows] = await Usuario.findOne(request.body.correo);

  let error = 1;
  if (rows.length < 1) {
    response.status(200).json({ errores: error });
    return;
  }

  const usuario = new Usuario(
    rows[0].Nombre_Usuario,
    rows[0].Login,
    rows[0]["Contraseña"],
    rows[0].URL_Foto
  );

  const doMatch = await bcrypt.compare(
    request.body.contrasenia,
    usuario.contrasenia_usuario
  );

  if (!doMatch) {
    response.status(200).json({ errores: error });
    return;
  }

  const [rowsActive] = await Usuario.getOneActive(usuario.login_usuario);
  error = 2;
  if (rowsActive[0].Activo != 1) {
    response.status(200).json({ errores: error });
    return;
  }

  error = 0;
  request.session.isLoggedIn = true;
  request.session.usuario = usuario;
  request.session.correo = usuario.login_usuario;
  //console.log(request.session.usuario);
  const [rowsid] = await Usuario.getId(request.session.correo);
  request.session.id_usuario = rowsid[0].Id_Usuario;

  const rowsprivilegios = await Usuario.fetchRolUsuario(
    request.session.id_usuario
  );

  let privilegios = [];
  for (let privilegio in rowsprivilegios) {
    privilegios.push(rowsprivilegios[privilegio].Id_Privilegio);
  }

  request.session.privilegios = privilegios;

  return request.session.save((err) => {
    response.status(200).json({ errores: error });
  });
};

```

### Episodio siguiente

[TICKETS EP1: Como utilizar enums para reducir valores hard-codeados](TICKETS%20EP1%20Como%20utilizar%20enums%20para%20reducir%20valor%20642da60d999a49c491def7f633871e92.md)