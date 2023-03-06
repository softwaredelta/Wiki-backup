# Definición de Alcance

Assign: Rodrigo Muñoz Guerrero, Kenny Eduard Vercaemer González
Description: Este documento define el alcance de un proyecto sin una especificación de requerimientos detallada. Permite establecer un acuerdo inicial con el cliente para comenzar a trabajar en el diseño.
Proyecto: RAM
Status: Done
Tags: Fase: Análisis
Tipo de Producto: Definición de Alcance

**ESPECIFICACIÓN DE MODULOS DE SOFTWARE**

**SISTEMA DE SEGUIMIENTO Y GESTIÓN DE INFORMACIÓN PARA *GRUPO ASESORES RAM®***

![Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/image2.png](Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/image2.png)

28/02/2023

---

## **Objetivo de Proyecto**

<aside>
💡 Obtener información actualizada sobre el progreso de ventas y capacitación de los agentes en menos de 5 minutos

</aside>

---

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
4. Seguimiento de negocios PAI[G/A]

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

1. ****************************ADMINISTRACIÓN****************************

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

1. **BONOS**

Se registran bonos ganados por agentes para tener métricas generales y particulares de bonos, así como metas de departamento.

Acciones específicas del módulo incluyen:

1. Registrar bono
2. Visualizar bonos registrados.

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

1. **AYUDA**

Los agentes, gerentes y administradores acceden a la sección de preguntas frecuentes, ayuda y videotutoriales en caso de tener una duda.

Acciones específicas del módulo incluyen:

1. Preguntas frecuentes
2. Videotutoriales
3. Contactos

## **DEFINICIÓN DE MVP Y ENTREGAS**

### **MVP**

La propuesta de MVP consiste en la primera implementación de los primeros tres módulos (Cursos, Ventas y Usuarios), de los cuáles se desarrollarán las funcionalidades siguientes:

1. Cursos
    1. Marcar un entregable como realizado
    2. Ver avance de grupos activos
    3. Ver historial de grupos y entregables
    4. Ver cantidad de agentes por grupo activo
    5. Ver cantidad de agentes que han completado entregables de un grupo
    6. Ver grupo activo y entregables del mismo de un agente en particular
    7. Gestionar grupos y entregables
2. Ventas
    1. Registrar una venta
    2. Verificar la venta de un gerente
    3. Consultar acumulado de ventas personal de un agente
    4. Consultar acumulado general de ventas de agentes
3. Usuarios
    1. Iniciar sesión
    2. Cerrar sesión
    3. Registrar usuario en app

Dichas funcionalidades se desarrollarán como primer avance y están sujetas a evolución.

### **MLP**

Nuestra propuesta MLP es la evolución de las primeras funcionalidades e implementación de los siguientes tres módulos (Control de Acceso, Prospectos, Administración y Bonos). Las funcionalidades adicionales al MVP que éste tendría son:

- Cálculo de negocios PAI según ventas y periodicidad de pagos
- Tener roles de usuario, limitando funcionalidades del sistema según su nivel de acceso como son métricas generales, etc.
- Generar una lista de prospectos de clientes para los agentes
- Métricas sobre lista de prospectos (Personales y generales según políticas de acceso)
- Panel administrativo para manejo de escalabilidad del sistema
- Registro de bonos de agentes
- Seguimiento de metas departamentales

## **Glosario**

*MVP -* El Producto Mínimo Viable o Minimum Viable Product (MVP) es el conjunto mínimo de funcionalidades del producto que aporten valor al cliente y recibir retroalimentación de las mismas.

*MLP* - El Producto Mínimo Adorado o Minimum Lovable Product (MLP), es el conjunto mínimo de funcionalidades para que el usuario adore el producto desde el principio.

********************Entregable -******************** Tarea, actividad o clase que se pueda marcar como realizado y aporte al progreso de un grupo.

*****Grupo***** - Conjunto de entregables.

********Negocio PAI -******** Medida interna de GNP para estimación de valor de póliza de agentes.

****************Escalabilidad -**************** Capacidad del sistema para aumentar su alcance sin necesidad del equipo de desarrollo.

---

[Manejo de Versiones](Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/Manejo%20de%20Versiones%2035db8bf8116049bbb9b82ffb03ac5823.md)