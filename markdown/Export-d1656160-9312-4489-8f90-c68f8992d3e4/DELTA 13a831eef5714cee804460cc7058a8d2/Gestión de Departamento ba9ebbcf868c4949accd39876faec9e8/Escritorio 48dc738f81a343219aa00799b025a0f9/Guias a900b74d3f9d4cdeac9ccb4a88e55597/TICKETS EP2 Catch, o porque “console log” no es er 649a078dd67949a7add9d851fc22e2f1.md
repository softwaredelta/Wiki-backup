# TICKETS EP2: Catch, o porque “console.log” no es error handling apropiado

Must Read: Yes
Tags: Calidad, Desarrollo, Tickets

# Problemática

Veamos el siguiente fragmento de *********************tickets*********************, una línea llama nuestra atención:

```jsx
exports.postEliminar_tp = (request, response, next) => {
    id_tp = request.params.id_tipo_incidencia;
    Tipo_incidencia.cambiar_visibilidad(id_tp)
    .then(() => response.status(200).json({}))
    .catch(err => console.log(err)); // QUE ES ESTOOOOOO !!!
}
```

**¿Pero qué está mal con esta práctica?**

De manera sencilla: el error no está siendo considerado. Simplemente estamos loggeando un error, lo cual tiene *exactamente 0 impacto* en la aplicación y el usuario final.

Por ejemplo:

1. Un usuario de la página web realiza una request a este endpoint.
2. Un error surge en la lógica del endpoint.
3. El error handler imprime un error.
4. **El usuario nunca recibe una respuesta.**

**ESTO NO SE PUEDE CONSIDERAR “ERROR HANDLING”.**

## Solución

El manejo de errores es un tema demasiado complejo para describir en una sola guía. Como guía básica, uno se puede guiar por los siguientes puntos:

1. El backend, no puede quedar en un estado inválido, no importa que proceso o función genere un error.
2. El frontend, debe recibir y actuar adecuadamente frente a respuestas de error (mostrar mensaje de problemas técnicos por ejemplo).
3. El backend, debe alertar al frontend en situaciones de problemas, o intentar enviar respuestas válidas de otra manera.
4. *Y sí, también podemos loggear los errores.*

## Resultado

```jsx
// backend
exports.postEliminar_tp = (request, response, next) => {
    id_tp = request.params.id_tipo_incidencia;
    Tipo_incidencia.cambiar_visibilidad(id_tp)
    .then(() => response.status(200).json({}))
    .catch(() => response.status(500).json({})); // Indica error de servidor
}

// frontend
const res = await fetch(...);
if (res.status === 500) {
   // mostrar mensaje de error...
}
...
```

### Episodio anterior

[TICKETS EP1: Como utilizar enums para reducir valores hard-codeados](TICKETS%20EP1%20Como%20utilizar%20enums%20para%20reducir%20valor%20642da60d999a49c491def7f633871e92.md)