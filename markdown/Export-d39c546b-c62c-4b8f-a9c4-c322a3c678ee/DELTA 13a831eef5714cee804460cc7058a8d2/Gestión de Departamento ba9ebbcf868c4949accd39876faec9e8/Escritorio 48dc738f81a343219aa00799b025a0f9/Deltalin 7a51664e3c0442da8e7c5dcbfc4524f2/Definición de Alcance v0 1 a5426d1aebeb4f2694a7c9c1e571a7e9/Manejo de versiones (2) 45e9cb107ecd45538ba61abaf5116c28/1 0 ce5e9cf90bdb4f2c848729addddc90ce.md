# 1.0

Autor: Jorge Guerrero Díaz, Cristian Rico
Descripción: Creación de la primera versión del SRS.
Correcciones ortográficas.
Cambio de nombre.
Se agrega nueva sección Comunicación con el Cliente.
Revisado: Reviewed
Revisado por: @Emiliano Vásquez Olea @Andres

**ESPECIFICACIÓN DE MÓDULOS DE SOFTWARE**

**APLICACIÓN MÓVIL DE AUDITORIAS Y APLICACIÓN WEB ADMINISTRATIVA PARA EMPRESA *Michelin***

![../../../Productos%20de%20Trabajo%2097cd5526070c4c4aaa931c06e02b08d9/Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/image2.png](../../../Productos%20de%20Trabajo%2097cd5526070c4c4aaa931c06e02b08d9/Definicio%CC%81n%20de%20Alcance%20ca920809c33b4daeb7cecc1d35bc67c6/image2.png)

21/02/2023

## Simbología

### Tipos de usuarios (Roles)

[A] - Administrador

[M] - Manager

[T] - TMB

## **Módulos (PRIORIZADOS)**

### Módulos de Aplicación

1. ***RECORRIDO***

Módulo centrado en el desarrollo del ambiente de Unity, donde se manejará el progreso de la auditoria e integración con módulo formulario. 

Acciones específicas del módulo incluyen:

1. Selección de Punto de Venta
2. Interacción con el Exterior e Interior
3. Resumen final de la auditoria
4. Manejar el progreso del proceso (Check-points)

**NOTA:**

Este módulo tendrá integración con el modulo de formulario. 

1. ***Formulario***

Módulo que engloba las secciones de preparación, entrevista con el cliente y entrevista con el mánager del punto de venta.

Acciones específicas del módulo incluyen:

1. Responder Preguntas
2. Interacción de Cámara
3. Tipo de Punto de Venta

1. ***Reporte***

Manejo de la información del formulario y recorrido para la generación del reporte en formato pdf

Acciones específicas del módulo incluyen:

1. Diseño del Reporte

1. ***Correo***

Módulo del desarrollo de la API para el envío de los reportes por correo

Acciones específicas del módulo incluyen:

1. Escribir los correos de los interesados
2. Automatizar el envío de correo

1. ***Autenticación***

Módulo para manejar el acceso a la aplicación a través de la verificación de credenciales.

Acciones específicas del módulo incluyen:

1. Inicio de sesión

### Módulos Web

1. ***Administración Usuarios***

Módulo para la administración de los miembros , tanto roles y los equipos.

Acciones específicas del módulo incluyen:

1. Crear, Modificar y Eliminar Usuarios
2. Crear, Modificar y Eliminar Equipos

1. ***Administración Puntos de Venta***

Módulo de Puntos de venta que trabaja la empresa Michelin

Acciones específicas del módulo incluyen:

1. Crear, Modificar y Eliminar Puntos de Venta
2. Recuperar información de API google

1. ***Historial***

Módulo del registro de todos los reportes pasados.

Acciones especificas del modulo incluyen:

1. Filtrar los reportes
2. Reenviar correos 
3. Visualizar resúmenes y reportes

1. ***Preguntas***

Módulo de las preguntas realizadas durante las auditorias

Acciones especificas del modulo incluyen:

1. Crear, Modificar y Eliminar Preguntas 
2. Asignar preguntas a categorías

1. ***Métricas***

Módulo para visualizar información relevante y general del desempeño de los TBMs

Acciones especificas del modulo incluyen:

1. Consultar las métricas
2. Filtrar métricas

**DEFINICIÓN DE MVP Y ENTREGAS**

**MVP**

La propuesta de MVP consiste en la primera implementación de los módulos móvil (Recorrido, Formulario, Reporte, Correo) y módulos web (Administración Usuarios, Puntos de Venta, Preguntas) y módulo de Autenticación.

1. Recorrido
    1. Navegar por el mapa
    2. Guardar los progresos
    3. Ver los modelos y animaciones básicas
2. Formulario
    1. Responder preguntas
    2. Guardar la información
    3. Tomar fotos para el reporte
3. Reporte
    1. Generar el reporte
    2. Visualizar el reporte
4. Correo
    1. Enviar correo del reporte
5. Autenticación
    1. Inicio de sesión
    2. Cerrar sesión
6. Administración Usuarios 
    1. Registrar Usuarios
7. Administración Puntos de Venta
    1. Ver los puntos de venta
    2. Registrar puntos de venta 
8. Preguntas
    1. Registrar preguntas
    2. Ver preguntas

Dichas funcionalidades se desarrollarán como primer avance y están sujetas a evolución.

**MLP**

Nuestra propuesta MLP es la evolución de las primeras funcionalidades e implementación de los siguientes módulos (Métricas, Historial). Las funcionalidades adicionales al MVP que éste tendría son:

- Tener roles de usuario, limitando funcionalidades del sistema según su nivel de acceso como son métricas de equipos, acceso de historial, etc.
- Editar a los usuarios, puntos de venta y preguntas del sistema.
- Generar métricas visuales para ver de manera general el desempeño de todos los empleados
- Métricas del desempeño de los TBMs en sus respectivas zonas
- Métricas con información sobre los puntos de venta que evalúan