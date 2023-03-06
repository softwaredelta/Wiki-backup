# Manual de Arquitectura

![../Productos%20de%20Trabajo%2097cd5526070c4c4aaa931c06e02b08d9/Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/image2.png](../Productos%20de%20Trabajo%2097cd5526070c4c4aaa931c06e02b08d9/Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/image2.png)

# Introducción

En este documento se abarcan las tecnologías, diseño y decisiones que componen el sistema de recorridos trabajado para Michelin. El equipo de desarrollo se hace cargo de implementar estos elementos dentro de las diferentes etapas del sistema, de los cuales se detalla su función, así como la razón por la cuál fueron elegidos. A continuación, se presentan en diferentes secciones los objetivos del sistema y su arquitectura, las tecnologías utilizadas y su descripción, diseño de elementos del software y finalmente las conclusiones sobre los componentes utilizados.

# Objetivos

En este proyecto se busca reducir el tiempo invertido en auditorías para los diferentes puntos de venta de Michelín. Para esto, se propone un sistema que consiste de una aplicación móvil como herramienta para llenar y enviar reportes de recorridos rápidamente, y una web que tendrá diferentes funciones administrativas para los miembros del equipo de Michelin. Adicionalmente, se cuenta con un servicio en la nube encargado de alojar la aplicación web y de almacenar los datos utilizados por ambos componentes.

Previo al desarrollo de esta propuesta, se definieron las tecnologías que serían utilizadas, acompañadas con ciertas decisiones de diseño. De forma general, se integran herramientas para crear interfaces accesibles y que se apegan a los estándares de Michelin dentro de las aplicaciones, junto con un servicio web de alto rendimiento con el fin de procesar la información generada y enviada de las auditorías en puntos de venta. Es posible que a lo largo de las etapas del proyecto haya sido necesario cambiar las propuestas iniciales de arquitectura, con el fin de alcanzar los objetivos del proyecto a pesar de dificultades que se presenten.

# Tecnologías Utilizadas

### Unity

Un motor que permite diseñar juegos o escenas en 3D o 2D. Es usualmente utilizado para crear videojuegos, simuladores o cualquier otra aplicación que requiera de interacción con un espacio en 3D. Sobre esta tecnología podremos importar el modelo de la sucursal de Michelin y posteriormente incorporar el formulario interactivo para iPads.

**Beneficios:**

  - Permite exportar la aplicación a la mayoría de las plataformas, incluyendo las de Apple.
  - Brinda herramientas para manejar objetos en 3D fácilmente. 
  - Probar el desarrollo es un proceso rápido y sin necesidad del dispositivo final. 
  - Se podrá trabajar con la versión gratis de la aplicación.
  - Buena documentación y comunidad activa.

### React

Librería de JavaScript utilizada para crear interfaces de usuario interactivas y de forma rápida. Junto con Tailwind, será utilizado para la página web administrativa que conforma la propuesta.

**Beneficios:**
  - Permite una integración sencilla del trabajo en equipo.
  - Código legible y mantenible.
  - Buen rendimiento.
  - Basado en componentes

### Tailwind CSS

Tailwind es un framework utilizado para diseñar páginas web atractivas. A comparación de otros frameworks, no solo ofrece componentes ya estilizados, lo que permite mayor libertad y customización.

**Beneficios:**

  - Mantiene los archivos CSS pequeños.
  - Fácil de editar sin temor a cometer errores.
  - Ofrece diferentes plantillas.

### Fastify

Un framework diseñado para soportar el desarrollo de aplicaciones web y fácil implementación de servicios, recursos y APIs. Fastify está inspirado en Express y promete ser una alternativa más rápida que utiliza menos recursos. Utilizado para el servicio web del sistema, permitiendo el acceso a las funciones necesarias por las aplicaciones de navegador y móvil.

**Beneficios:**

  - Alto rendimiento.
  - Fácil integración con APIs y otras tecnologías.
  - Accesible para desarrolladores.

### MySQL

MySQL es un sistema de manejo de base de datos. Tiene como función el acceso y edición de los datos almacenados en la nube para las aplicaciones del sistema.

**Beneficios:**

  - El equipo de desarrollo se encuentra familiarizado con esta tecnología.
  - Es una herramienta segura
  - Buena escalabilidad y flexibilidad

### Amazon EC2

# Diseño

### Diagrama de Arquitectura

![FotoDiagrama2.png](Manual%20de%20Arquitectura%2080aad387749d4ee3bbdca56867f338c6/FotoDiagrama2.png)

### Modelo Entidad-Relación (diagrama de base de datos)

![v1.0.png](../Productos%20de%20Trabajo%2097cd5526070c4c4aaa931c06e02b08d9/MER%20c25769febabe43399091a01c8a5dfd08/v1.0.png)

### Patrones de diseño

# Conclusiones