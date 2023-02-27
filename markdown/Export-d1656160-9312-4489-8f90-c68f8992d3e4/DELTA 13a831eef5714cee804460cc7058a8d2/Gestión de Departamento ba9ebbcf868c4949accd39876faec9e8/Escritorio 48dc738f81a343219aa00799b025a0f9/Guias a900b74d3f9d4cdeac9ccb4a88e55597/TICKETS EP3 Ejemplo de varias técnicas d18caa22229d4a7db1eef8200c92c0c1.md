# TICKETS EP3: Ejemplo de varias técnicas

Must Read: Yes
Tags: Calidad, Desarrollo, Tickets

## Problemática

Veamos el siguiente fragmento de *********************tickets*********************, y apliquemos los temas de los episodios pasados:

```jsx
exports.lista = (request, response, next) => {
  if(14 in request.session.privilegios){
    Ticket.fetchList()
    .then(([rowsTickets, fielData]) => {
      Tipo_incidencia.fetchAll()
        .then(([rowsIncidencias, fielDataIncidencias]) => {
          Ticket.fetchPrioridades()
            .then(([rowsPrioridades, fieldDataPrioridades]) => {
              Ticket.fetchProcedencias()
            .then(([rowsProcedencias, fieldDataPrioridades]) => {
              Usuario.fetchAll()
            .then(([rowsUsuarios, fieldDataPrioridades]) => {
              Ticket.fetchEstado()
                .then(([rowsEstados, fielDataEstados]) => {
                  response.render("panel_principal", {
                    usuarios: rowsUsuarios,
                    procedencias: rowsProcedencias,
                    tickets: rowsTickets,
                    prioridades: rowsPrioridades,
                    estados: rowsEstados,
                    incidencias: rowsIncidencias,
                  });
                })
                .catch((err) => {
                  console.log(err);
                });
            })
            .catch((err) => {
              console.log(err);
            });
          })
          .catch((err) => {
            console.log(err);
          });
        })
        .catch((err) => {
          console.log(err);
        });
        })
        .catch((err) => {
          console.log(err);
        });
    })
    .catch((err) => console.log(err));
  }else{
    response.redirect("/");
  }
  
};
```

## Resultado

No error handling que no hace nada, no nesting de callbacks complejo, early exit para condicionales más sencillos:

```jsx
exports.lista = async (request, response, next) => {
  if (!(Privilegios.Borrar in request.session.privilegios)) {
    response.redirect("/");

    return;
  }

  const rowsTickets = await Ticket.fetchList();
  const rowsIncidencias = await Tipo_incidencia.fetchAll();
  const rowsPrioridades = await Ticket.fetchPrioridades();
  const rowsProcedencias = await Ticket.fetchProcedencias();
  const rowsUsuarios = await Usuario.fetchAll();
  const rowsEstados = await Ticket.fetchEstado();
  response.render("panel_principal", {
    usuarios: rowsUsuarios,
    procedencias: rowsProcedencias,
    tickets: rowsTickets,
    prioridades: rowsPrioridades,
    estados: rowsEstados,
    incidencias: rowsIncidencias,
  });
};
```

Aquí se esconde otra situación, la cuál descubriremos en el siguiente episodio.

### Episodio pasado

[TICKETS EP2: Catch, o porque “console.log” no es error handling apropiado](TICKETS%20EP2%20Catch,%20o%20porque%20%E2%80%9Cconsole%20log%E2%80%9D%20no%20es%20er%20649a078dd67949a7add9d851fc22e2f1.md)

### Episodio siguiente

[TICKETS EP4: Como utilizar Promise.all para optimizar queries](TICKETS%20EP4%20Como%20utilizar%20Promise%20all%20para%20optimiz%20844686d0ba7642a18c7d39b4429874c1.md)