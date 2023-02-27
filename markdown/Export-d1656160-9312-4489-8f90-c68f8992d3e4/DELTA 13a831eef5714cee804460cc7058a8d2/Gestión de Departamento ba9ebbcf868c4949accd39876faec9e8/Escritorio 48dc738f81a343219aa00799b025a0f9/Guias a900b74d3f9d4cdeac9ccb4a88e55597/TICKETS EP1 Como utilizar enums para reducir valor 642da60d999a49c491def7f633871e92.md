# TICKETS EP1: Como utilizar enums para reducir valores hard-codeados

Must Read: Yes
Tags: Calidad, Desarrollo, Tickets

# Problemática

En el siguiente fragmento del backend de *********************tickets*********************, existe una línea que llama nuestra atención:

```jsx
exports.getTipo_Incidencia = (request, response, next) => {
    if(request.session.privilegios.includes(4)){   // QUE ESTÁ PASANDO AQUIÍIIII
    Tipo_incidencia.fetchAll()
    .then(([rowsTipo_Incidencia, fieldDataTipo_Incidencia]) => {
        Tipo_incidencia.fetchAllPreguntas()
            .then(([rowsPreguntas, fieldDataPreguntas]) => {
                response.render('tipo_incidencia/lista_tipo_incidencia', {
                    Tipo_Incidencias: rowsTipo_Incidencia,
                    Preguntas: rowsPreguntas
                });
            })
            .catch(err => console.log(err));
        })
    .catch(err => console.log(err));
    }else{
        response.redirect("/")
    }
}
```

El problema es que cualquiera que lea este código, no tiene ni idea de que significa un privilegio “4”. Esto no solo hace innecesariamente difícil el proceso de lectura del código, sino que cualquier posible cambio futuro, tendrá un riesgo *enorme* de causar alguna regresión si se olvida de cambiar algún valor en algún sitio.

## Solución

El lenguaje nos proporciona `enums`. Podemos crear una enumeración para los privilegios, así toda la información esta codificada en un sólo lugar, y cualquier uso nos hace entender que está pasando:

```jsx
export enum Privilegios {
  Leer = 1,
  Escribir = 2,
  Borrar = 3,
  Modificar = 4,
}

exports.getTipo_Incidencia = (request, response, next) => {
  if (request.session.privilegios.includes(Privilegios.Modificar)) { // Ahhhh pero que diferencia
    Tipo_incidencia.fetchAll()
      .then(([rowsTipo_Incidencia, fieldDataTipo_Incidencia]) => {
        Tipo_incidencia.fetchAllPreguntas()
          .then(([rowsPreguntas, fieldDataPreguntas]) => { // Ouch, leer TICKETS EP0
            response.render("tipo_incidencia/lista_tipo_incidencia", {
              Tipo_Incidencias: rowsTipo_Incidencia,
              Preguntas: rowsPreguntas,
            });
          })
          .catch((err) => console.log(err));
      })
      .catch((err) => console.log(err));
  } else {
    response.redirect("/");
  }
};
```

Obtenemos código mucho más fácil de leer y mantener, refactorizar, y menos riesgo de introducción de regresiones.

### Episodio pasado

[TICKETS EP0: Como reescribir código para reducir nesting y complejidad](TICKETS%20EP0%20Como%20reescribir%20co%CC%81digo%20para%20reducir%20n%20fdb332b899454876b5c07b3e07e97e54.md)

### Episodio siguiente

[TICKETS EP2: Catch, o porque “console.log” no es error handling apropiado](TICKETS%20EP2%20Catch,%20o%20porque%20%E2%80%9Cconsole%20log%E2%80%9D%20no%20es%20er%20649a078dd67949a7add9d851fc22e2f1.md)