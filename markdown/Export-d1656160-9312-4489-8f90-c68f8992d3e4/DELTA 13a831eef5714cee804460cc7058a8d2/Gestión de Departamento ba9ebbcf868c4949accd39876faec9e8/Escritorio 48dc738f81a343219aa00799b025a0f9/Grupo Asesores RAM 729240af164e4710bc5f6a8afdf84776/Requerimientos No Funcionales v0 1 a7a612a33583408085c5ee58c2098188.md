# Requerimientos No Funcionales v0.1

Este documento es la primer revisión de ****requerimientos no funcionales****.

********Definiciones:******** Las siguientes definiciones serán utilizadas y compartidas en el resto del documento.

- *********************************INTERACCIÓN*********************************: Se refiere a una acción en la página web. Ejemplos son: hacer click en un botón, enviar un formulario, descargar un archivo, recargar una tabla de datos.
- *********************************************USUARIO ACTIVO*********************************************: Se refiere a un usuario con una sesión activa en la página web. Este usuario no está realizando acciones o interactuando con la página, pero puede estar recibiendo datos continuamente.
- *********************************************************USUARIO INTERACTIVO*********************************************************: Se refiere a un usuario con una sesión activa en la página web. Este usuario realiza acciones continuamente, como pedir una lista de datos, o enviar formularios.
- ***************************************************************UTILIZACIÓN REGULAR***************************************************************: Se refiere a **30 usuarios activos** (pero no realizando acciones, es decir, sólo existen las sesiones activas, sin interacción directa) y **5 usuarios interactivos**.
- *******UTILIZACIÓN ELEVADA*******: Se refiere a **60 usuarios activos** (pero no realizando acciones, es decir, sólo existen las sesiones activas, sin interacción directa) y **15 usuarios interactivos**.

******************************Notas de autor:******************************

- Las secciones en letra color rojo, están pendientes de revisión.

---

## Rendimiento y Escalabilidad

¿Qué tan rápido el sistema arroja resultados?

¿Qué tanto puede cambiar este rendimiento bajo cargas de trabajo elevadas?

**********NFR-RE01.1:********** La carga inicial de la página web - sin importar la página destino - bajo *********************************UTILIZACIÓN REGULAR*********************************, tendrá un **tiempo promedio para interactividad menor a 7 segundos**.

**********NFR-RE01.2:********** La carga inicial de la página web - sin importar la página destino - bajo *********************************UTILIZACIÓN ELEVADA*********************************, tendrá un **tiempo promedio para interactividad menor a 10 segundos**.

******************NFR-RE02.1:****************** El tiempo de carga o actualización después de cualquier interacción en la página web bajo ******************UTILIZACIÓN REGULAR******************, tendrá un **tiempo promedio de resultados menor a 3 segundos**.

******************NFR-RE02.2:****************** El tiempo de carga o actualización después de cualquier interacción en la página web bajo ******************UTILIZACIÓN ELEVADA******************, tendrá un **tiempo promedio de resultados menor a 5 segundos**.

Base de datos

Almacenamiento archivos

API

## Mantenibilidad, Disponibilidad y Fiabilidad

¿Qué tan seguido el sistema experimenta fallas críticas?

¿Cómo se compara el tiempo de disponibilidad del sistema al tiempo de no operación?

********************NFR-MDF01.1:******************** El **tiempo de no operación debido a fallas** de infraestructura será menor al **0.01%**.

**************************NFR-MDF01.2:************************** El **tiempo de no operación debido a fallas por despliegue** de código será menor a 1 hora por incidente. En estos casos,, se recurrirá a un rollback de versiones pasadas para activar el sistema de nuevo temporalmente hasta encontrar una solución.

## Compatibilidad y Portabilidad

¿Qué hardware, software, sistemas operativos, browsers, y sus versiones, serán soportados por el sistema?

******************NFR-CP01:****************** El sistema soportará oficialmente la versión de **Node LTS 18.14.2**.

******************NFR-CP02:****************** El sistema soportará oficialmente servidores con sistema operativo Linux. (OS especifico por definir).

********************NFR-CP03:******************** El sistema soportará oficialmente únicamente las **últimas versiones de los navegadores de Chromium**.

Base de datos y versión.

## Usabilidad

****************NFR-U01:**************** El usuario promedio tardará menos de **60 segundos** en encontrar el área necesaria para realizar una operación.

## Localización

****************NFR-L01:**************** La página web únicamente soportará el **idioma Español**.

## Seguridad

******NFR-S01******: Todos los archivos almacenados por el sistema, estarán protegidos por pólizas de autenticación y autorización.

**NFR-S02:** La base de datos estará protegida por pólizas de autenticación y autorización.

********NFR-S03:******** El acceso a la página web únicamente será mediante HTTPS.