# Definición de alcance v0.1

**ESPECIFICACIÓN DE MODULOS DE SOFTWARE**

**SISTEMA DE SEGUIMIENTO Y GESTIÓN DE INFORMACIÓN PARA *GRUPO ASESORES RAM®***

![../../Productos%20de%20Trabajo%2097cd5526070c4c4aaa931c06e02b08d9/Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/image2.png](../../Productos%20de%20Trabajo%2097cd5526070c4c4aaa931c06e02b08d9/Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/image2.png)

21/02/2023

## Simbología

### Tipos de usuarios (Roles)

[M] - Administrador

[G] - Gerente

[A] - Agente

## **Módulos (PRIORIZADOS)**

1. ***CURSOS***

Gerentes conocen el progreso general y particular de los agentes en la realización de cursos de capacitación. Agentes consultan y actualizan su progreso en el cumplimiento de cursos. Administrador gestiona los cursos en el sistema.

Acciones específicas del módulo incluyen:

1. Registrar, Modificar, Visualizar y Eliminar cursos [M/G]
2. Marcar cursos como realizados [A]
3. Visualizar métricas de cursos realizados [Todos]
4. Verificar el cumplimiento de los cursos por parte de los agentes [G]

**NOTA:** Se administrarán los cursos y grupo de cursos desde el panel de administrador del programa.

1. ***VENTAS***

Gerentes conocen el acumulado de ventas general y particular de los agentes según su tipo de seguro y periodo. Agentes consultan y registran sus ventas.

Acciones específicas del módulo incluyen:

1. Registrar venta [A]
2. Visualizar métricas de acumulados de ventas [G/A]
3. Verificar la venta de un agente [G]

**NOTA:** Se llevará un proceso de verificación para cada venta que registre un agente, un gerente es responsable de la aceptación del registro de venta.

1. ***USUARIOS***

Se registran usuarios que pueden interactuar con el sistema.

Acciones específicas del módulo incluyen:

1. Registrar usuario

**NOTA 1:** Con el control de acceso implementado, se elegirá un rol de usuario, del cual dependerá el acceso a diferentes métricas y funcionalidades.

**NOTA 2:** El proceso de registro de usuario esta por definir.

1. ***CONTROL DE ACCESO***

Se definen las funcionalidades a las cuales tiene acceso cada tipo de usuario.

Acciones específicas del módulo incluyen:

1. Segmentación de privilegios del sistema

1. ***PROSPECTOS***

Gerentes visualizan la lista y métricas de prospectos de venta de los agentes. Agentes registran nuevos prospectos y su avance en el proceso de venta con los mismos, así como también visualizan métricas de la misma lista.

Acciones específicas del módulo incluyen:

1. Registrar y Actualizar prospecto [A]
2. Visualizar métricas numéricas y gráficas [G/A]

1. ***CALENDARIO** [En investigación de viabilidad]*

Conexión con calendario de cuenta Outlook para la gestión de eventos de la empresa y personales.

Acciones específicas del módulo incluyen:

1. Visualizar eventos [Todos]
2. Crear, Modificar y Eliminar eventos [Todos]

**NOTA:** Se está investigando la posibilidad de la integración de este módulo por el sistema de comunicación de la aplicación (API).

1. ***MI PROGRESO***

Agentes definen metas personales y analizan su progreso en cursos y ventas. Gerentes visualizan el progreso de sus agentes en sus metas, cursos y ventas.

Acciones específicas del módulo incluyen:

1. Definir una meta personal de capacitación o de ventas [A]
2. Visualizar información de progreso hacia metas [G/A]
3. Notificaciones de progreso hacia metas [A]

8. ***MANAGEMENT***

Panel administrativo para modificar información y restricciones del sistema, asegurando  escalabilidad y autogestión del proyecto por parte de RAM.

Acciones específicas del módulo incluyen:

1. Crear y Eliminar:
    - Procedencia de agente (Referido, LinkedIn, etc.)
    - Tipos de Seguros
    - Cursos y Grupo de cursos
    - Metas departamentales y personales
    - Tipos de usuario (Roles)
    - Etc.
2. Asignar privilegios de sistema a rol

**NOTA:** El contenido de este módulo está sujeto a cambios según las necesidades del sistema y del equipo tanto de desarrollo como de Asesores RAM

1. **AYUDA**

Los agentes, gerentes y administradores acceden a la sección de preguntas frecuentes, ayuda y videotutoriales en caso de tener una duda.

Acciones específicas del módulo incluyen:

1. Preguntas frecuentes
2. Videotutoriales
3. Contactos

**DEFINICIÓN DE MVP Y ENTREGAS**

![../../Productos%20de%20Trabajo%2097cd5526070c4c4aaa931c06e02b08d9/Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/Manejo%20de%20Versiones%2035db8bf8116049bbb9b82ffb03ac5823/0%201%200%20d612a844ed204ac680432c99a169d777/image1.png](../../Productos%20de%20Trabajo%2097cd5526070c4c4aaa931c06e02b08d9/Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/Manejo%20de%20Versiones%2035db8bf8116049bbb9b82ffb03ac5823/0%201%200%20d612a844ed204ac680432c99a169d777/image1.png)

**MVP**

El Producto Mínimo Viable o Minimum Viable Product (MVP) es el conjunto mínimo de funcionalidades del producto que aporten valor al cliente y recibir retroalimentación de las mismas.

La propuesta de MVP consiste en la primera implementación de los primeros tres módulos (Cursos, Ventas y Usuarios), de los cuáles se desarrollarán las funcionalidades necesarias para poder marcar un curso como realizado, registrar una nueva venta y atribuirla a un usuario, ver métricas sobre el progreso general y particular de los agentes sobre cursos completados y ventas. Dichas funcionalidades se desarrollarán como primer avance y están sujetas a evolución.

**MLP**

El Producto Mínimo Adorado o Minimum Lovable Product (MLP), es el conjunto mínimo de funcionalidades para que el usuario adore el producto desde el principio.

Nuestra propuesta MLP es la evolución de las primeras funcionalidades e implementación de los siguientes tres módulos (Control de Acceso, Calendario y Prospectos). Las funcionalidades adicionales al MVP que éste tendría son:

- Tener roles de usuario, limitando funcionalidades del sistema según su nivel de acceso como son métricas generales, etc.
- Crear un acceso al calendario de Outlook para visualizar, crear y editar eventos
- Generar una lista de prospectos de clientes para los agentes
- Métricas sobre lista de prospectos (Personales y generales según políticas de acceso)
- Métricas con información adicional sobre cursos y ventas