# Cómo llenar los requisitos funcionales en formato de Historia de Usuario

Autor: Monica Ayala
Date: March 1, 2023
ID: 2
Tags: Requisitos

## Documentos relacionados

## Formato

En Google Sheets se encuentra el formato de requisitos funcionales, antes de comenzar a llenarlo, cada equipo debe de hacer una copia y **trabajar sobre ella**. El link se encuentra a continuación:

[](https://docs.google.com/spreadsheets/d/1X-HpEdOKAKUIVbcqLjRyCIJW7jiraa5Oqq25f2Gk0vE/edit#gid=0)

## Backlog

En la primera hoja del documento podemos ver que hay tablas, cada una de ellas correspondiendo a un **módulo** en particular. En cada tabla se van a definir las historias de usuario que componen a cada módulo.

![Untitled](Co%CC%81mo%20llenar%20los%20requisitos%20funcionales%20en%20formato%20638cc52e59414835b4bfce35adfa651c/Untitled.png)

1. Cambiar el **título** en las celdas A1:E1 al nombre del Módulo. 
    1. Ejemplo: *Módulo 1 - Módulo de Ventas*.
2. Comenzar a llenar los datos de una historia de usuario. Veamos los **criterios de entrada** de cada dato.
    1. El **ID** es único para cada historia de usuario, se compone sabiendo el número de módulo y el número de historia de usuario. **ID: M[Número de Modulo]_S[Número de historia de usuario]**. 
        1. Ejemplo: la historia de usuario 3 en el módulo 5 sería: **M5_S3**
    2. El nombre es el como se llama la historia de usuario.
        1. Ejemplo: la historia de usuario donde un usuario llena todos los datos de un nuevo usuario se llama **Registrar Usuario.**
    3. El valor agregado es cuanto agrega de valor para los Stakeholders en un rango de 1 a 3, donde 3 es lo más grande.
    4. La estimación en puntos ágiles. (Posibles valores: 1,3,5,8,13. Estos van de menor a mayor). Para decidir una estimación es buena práctica definir un **pivote** en equipo (una historia de usuario con peso “medio”, es decir, de 5 puntos) y a partir de el usar estrategias como el **planning poker** (link explicativo: [https://www.atlassian.com/blog/platform/a-brief-overview-of-planning-poker](https://www.atlassian.com/blog/platform/a-brief-overview-of-planning-poker))
    5. Sprint se refiere al número de sprint al que corresponde la historia de usuario. Es decir, ¿para qué sprint se planeo la historia de usuario?
3. Podremos ver que después de la parte **violeta**, hay más **columnas azules y naranjas**. Estas se llenarán más adelante como una manera de tener **trazabilidad** del estado de cada módulo e historia de usuario.

## Descripción de una historia de usuario

En el Backlog de la primera hoja se definen todas las historias de usuarios, en la columna A registramos el ID de la historia de usuario. En esa celda se creará un link de referencia a una nueva hoja correspondiente a cada historia de usuario. En esa hoja nueva tendremos que copiar y pegar el formato que se encuentra en la hoja de “Formato de detalle de User Story”

![Untitled](Co%CC%81mo%20llenar%20los%20requisitos%20funcionales%20en%20formato%20638cc52e59414835b4bfce35adfa651c/Untitled%201.png)

*NOTA: ID y Nombre deben de ser los mismos valores ya llenados en la primera hoja (el Backlog)*

**Como <Rol, persona>**

Persona o rol de usuario que tiene la necesidad.

**Quiero <objetivo, comportamiento>**

Lo que quiere obtener: una funcionalidad, característica, etc.

**Para poder <motivo, razón, valor>**

Motivo por el que se necesita, valor que se obtiene como resultado, etc.

**Validación**

Flujo básico para la aceptación de la historia de usuario. 

### Ejemplo de descripción de historia de usuario

![Untitled](Co%CC%81mo%20llenar%20los%20requisitos%20funcionales%20en%20formato%20638cc52e59414835b4bfce35adfa651c/Untitled%202.png)

## ¿Qué hay del resto?

Las tablas en un color distinto al azul pertenecen al diseño de pruebas y se hará otra guía para rellenarlas.

## Historial de cambios

[Manejo de versiones ](Co%CC%81mo%20llenar%20los%20requisitos%20funcionales%20en%20formato%20638cc52e59414835b4bfce35adfa651c/Manejo%20de%20versiones%202a82813cf98c4bcaaa3193b042c27365.md)