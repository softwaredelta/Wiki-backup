# Gestión de Configuración

Abreviación: CM
Book Link: https://resources.sei.cmu.edu/asset_files/whitepaper/2010_019_001_28782.pdf#page=209
Metas Específicas: ../Metas%20Especi%CC%81ficas%2001a59630d53145479e64a6d0e43d64e0/Seguir%20y%20controlar%20los%20cambios%20a537c807da014a66b10e1e24da179c39.md, ../Metas%20Especi%CC%81ficas%2001a59630d53145479e64a6d0e43d64e0/Establecer%20la%20integridad%209618db253cc141fabc5d00e4bc3e4e8e.md, ../Metas%20Especi%CC%81ficas%2001a59630d53145479e64a6d0e43d64e0/Establecer%20las%20li%CC%81neas%20base%20c382b0af42cd4e1499bc83af273afb7b.md
Nivel de Madurez: 2
Propósito: El propósito de la Gestión de Configuración (CM) es establecer y mantener la integridad de los productos de trabajo utilizando la identificación de la configuración, el control de la configuración, el informe del estado de la configuración y las auditorías de la configuración.
Prácticas Específicas: ../Pra%CC%81cticas%20Especi%CC%81ficas%203e22172ab8ed4ff2b3612a605de70f12/Establecer%20los%20registros%20de%20gestio%CC%81n%20de%20configurac%20f9b4fb68122342b69d880b1f3b3b3369.md, ../Pra%CC%81cticas%20Especi%CC%81ficas%203e22172ab8ed4ff2b3612a605de70f12/Realizar%20auditori%CC%81as%20de%20configuracio%CC%81n%202afef92fe4a0485b99f1a6c7ab6972a4.md, ../Pra%CC%81cticas%20Especi%CC%81ficas%203e22172ab8ed4ff2b3612a605de70f12/Identificar%20los%20elementos%20de%20configuracio%CC%81n%204635dbea72704735919fcf580e728c33.md, ../Pra%CC%81cticas%20Especi%CC%81ficas%203e22172ab8ed4ff2b3612a605de70f12/Establecer%20un%20sistema%20de%20gestio%CC%81n%20de%20configuracio%CC%81%206f8cb123a7164a40897a29e36fbdda78.md, ../Pra%CC%81cticas%20Especi%CC%81ficas%203e22172ab8ed4ff2b3612a605de70f12/Crear%20o%20liberar%20las%20li%CC%81neas%20base%205d530ee7e9e3407d8f28e1750cee659b.md, ../Pra%CC%81cticas%20Especi%CC%81ficas%203e22172ab8ed4ff2b3612a605de70f12/Seguir%20las%20peticiones%20de%20cambio%20e9b9ef6d7fe24e4e9ab538ce77d4c9dd.md, ../Pra%CC%81cticas%20Especi%CC%81ficas%203e22172ab8ed4ff2b3612a605de70f12/Controlar%20los%20elementos%20de%20configuracio%CC%81n%20b0131bbcd1594bd48ce82f161fbbc534.md
Tags: completed

El área de proceso de Gestión de Configuración implica las siguientes actividades:

- Identificar la configuración de los productos de trabajo seleccionados que componen las líneas base en puntos determinados en el tiempo.
- Controlar los cambios a los elementos de configuración.
- Construir o proporcionar las especificaciones para construir los productos de trabajo a partir del sistema de gestión de configuración.
- Mantener la integridad de las líneas base.
- Proporcionar a los desarrolladores, usuarios finales y clientes datos precisos del estado y de la configuración actual.

Los productos de trabajo puestos bajo gestión de configuración incluyen los productos que se entregan al cliente, los productos de trabajo internos seleccionados, los productos adquiridos, las herramientas y otros elementos utilizados para crear y describir estos productos de trabajo (véase la definición de “gestión de configuración” en el glosario).

<aside>
💡 Algunos ejemplos de productos de trabajo que pueden ponerse bajo gestión de configuración son:

- Hardware y equipamiento.
- Diagramas.
- Especificaciones de producto.
- Configuraciones de herramientas.
- Código y bibliotecas.
- Compiladores.
- Herramientas de pruebas y scripts de pruebas.
- Registros de instalación.
- Ficheros de datos de producto.
- Publicaciones técnicas de producto.
- Planes.
- Historias de usuario.
- Backlogs de iteración.
- Descripciones de proceso.
- Requisitos.
- Documentación de la arquitectura y datos de diseño.
- Planes de líneas de producto, procesos y activos base.
</aside>

Puede ser necesario que los productos adquiridos se pongan bajo gestión de configuración tanto por el proveedor como por el proyecto. Para llevar a cabo la gestión de configuración, se deberían establecer las provisiones en los acuerdos con el proveedor. Se deberían establecer y mantener métodos para asegurar que los datos están completos y son consistentes.

Para más información sobre cómo establecer acuerdos con el proveedor:

[Gestión de Acuerdos con Proveedores](Gestio%CC%81n%20de%20Acuerdos%20con%20Proveedores%2004468e4302d54e828933fd7148021c6d.md)

La gestión de configuración de los productos de trabajo se puede realizar en diferentes niveles de detalle. Los elementos de configuración se pueden descomponer en componentes de configuración y en unidades de configuración. El término “elemento de configuración” sólo se utiliza en este área de proceso. Por tanto, en estas prácticas, el “elemento de configuración” se puede interpretar como “componente de configuración” o “unidad de configuración” según proceda (véase la definición de “elemento de configuración” en el glosario).

Las líneas base proporcionan una base estable para la evolución continua de los elementos de configuración.

<aside>
💡 Un ejemplo de una línea base es una descripción aprobada de un producto
que incluye versiones de requisitos consistentes a nivel interno, de matrices de trazabilidad de requisitos, de diseño, de elementos específicos de
una disciplina y de la documentación de usuario final.

</aside>

Las líneas base se añaden al sistema de gestión de configuración a medida que se desarrollan. Los cambios a las líneas base y a las versiones de los productos de trabajo construidos a partir del sistema de gestión de configuración, se controlan y monitorizan sistemáticamente mediante: el control de la configuración, la gestión de cambios y las funciones de auditoría de configuración de gestión de configuración.

Este área de proceso se aplica no sólo a la gestión de configuración en proyectos, sino también a la gestión de configuración de los productos de trabajo de la organización, tales como: estándares, procedimientos, bibliotecas de reutilización y otros activos de soporte compartidos.

La gestión de configuración se centra en el control riguroso de los aspectos de gestión y técnicos de los productos de trabajo, incluyendo el producto o servicio entregado.

Este área de proceso cubre las prácticas para realizar la función de gestión de configuración y es aplicable a todos los productos de trabajo que se ponen bajo gestión de configuración.

Para líneas de productos, la gestión de la configuración implica consideraciones adicionales debido a la compartición de activos básicos a través de los productos de la línea de productos y a través de múltiples versiones de los activos y productos base (véase la definición de “línea de productos” en el glosario).

<aside>
💡 En entornos ágiles, la gestión de la configuración (CM) es importante debido a la necesidad de soportar cambios y ensamblados frecuentes (normalmente a diario), múltiples líneas base, y múltiples espacios de trabajo soportados por CM (p. ej., para individuos, equipos, e incluso para la programación por pares). Los equipos ágiles pueden atascarse si la organización no: 1) automatiza CM (p. ej., creación de scripts, informes de estado, comprobación de integridad) y 2) implementa CM como un único conjunto de servicios estándar. En su inicio, un equipo ágil debería identificar a la persona que será responsable de garantizar que la CM esté correctamente implementada. Al inicio de cada iteración, es necesario reconfirmar las necesidades de soporte de CM. CM está cuidadosamente integrada en los ritmos de cada equipo centrándose en minimizar la distracción del equipo para realizar el trabajo (véase “Interpretando CMMI al utilizar enfoques ágiles”, en la Primera Parte)

</aside>

## Relacionado

Para más información sobre cómo monitorizar el proyecto frente al plan y gestionar las acciones correctivas hasta el cierre:

[Monitorización y Control del Proyecto](Monitorizacio%CC%81n%20y%20Control%20del%20Proyecto%20432710662d134b619e76c5e620fdf2ea.md)

Para más información sobre cómo desarrollar un plan de proyecto:

[Planificación del Proyecto](Planificacio%CC%81n%20del%20Proyecto%206dba5b9a080c4ef0a4babec2ebb5d62f.md)