# Como LLENAR y LEER las tablas y las graficas para el cálculo del SPI y CPI

Autor: Diego Emilio Barrera Hernández
Date: March 2, 2023
ID: 4
Tags: CPI, Monitorización, SPI

## Documentos relacionados

[DELTA](../../../../DELTA%2013a831eef5714cee804460cc7058a8d2.md)

[Cómo HACER las tablas y las graficas para el cálculo del SPI y CPI](Co%CC%81mo%20HACER%20las%20tablas%20y%20las%20graficas%20para%20el%20ca%CC%81l%20d14a21a34f6749d292e3e3d6cc78e358.md)

[Cómo ajustar las estimaciones del calendario](Co%CC%81mo%20ajustar%20las%20estimaciones%20del%20calendario%20ec42623b533e49a281c7272e7bc4d048.md)

## Tablas del calendario

1. La columna de “**Id**” la llenaremos con un número que identifique cada task. Debido a que esta tabla se llenará por iteración seguiremos una secuencia numérica normal y se reiniciará en cada iteración nueva.
    
    ![Untitled](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Untitled.png)
    

1. La columna “**Task**” se llenará con una tarea del proyecto y la escribiremos de una manera corta y sencilla de entender.
    
    ![Untitled](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Untitled%201.png)
    

1. La columna “**Assigned to**” la llenará el/la team leader actual y tendrá que asignar las personas necesarias para dicha tarea.
    
    ![Untitled](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Untitled%202.png)
    
2. Ahora nos saltaremos hasta la columna “**AP´s**”, esta se llenará con la forma de una serie Fibonacci y dependiendo la dificultad de la task aumentará su valor.
    
    ![Untitled](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Untitled%203.png)
    
    ***NOTA**: La serie Fibonacci va de la siguiente manera → 1, 2, 3, 5, 8, 13. Si alguna task valiera más de 13 tendrá que ser fragmentada en dos o más.*
    

1. La columna “**Duration(hrs)**” la llenará la persona que fue asignada en cada task, en dado caso de que haya más de una persona se llegará a un conceso entre todos.
    
    ![Untitled](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Untitled%204.png)
    

1. La columna “**Progress**” se llenará en las **DAILIES** o **WEEKLIES** y este cambio lo realizará la/el Team Lead actual.
    
    ![Untitled](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Untitled%205.png)
    

1. Las siguientes 3 columnas son fechas en formato **DÍA/MES/AÑO**.
    1. “**Due date**” será la fecha planeada de cada task y se establecerá según la decisión de los asignados. 
        
        ***NOTA**: ES IMPORTANTE RECORDAR QUE NO ES NECESARIO ENTREGAR EN ESA FECHA LAS ACTIVIDADES, ES UNA FECHA PLANEADA QUE SE ESTIMO DEPENDIENDO EL ESFUERZO, LA HABILIDAD Y LA DISPONIBILDAD DE TIEMPO DE LOS ASIGNADOS.*
        
    2. “**Start**” es la fecha en la que se empezó dicha task. 
        
        ***NOTA**: En el momento que se inicia una task se tomará el tiempo de inicio para que las estimaciones salgan de una forma más exacta.*
        
    3. “**End**” es la fecha en la que se termino la task.
        
        ***NOTA**: En el momento que se termina una task se deberá terminar de tomar el tiempo para después escribirla en la siguiente columna.*
        
        ![Untitled](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Untitled%206.png)
        
2. “**Real Time**” será el registro del tiempo que se tomó en el paso pasado.
    
    ***NOTA**: Debe ser lo más exacto posible para poder hacer correcto los cálculos de los costos.*
    
    ![Untitled](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Untitled%207.png)
    

## Graficas

1. Estas graficas se nombran “Valor planeado vs Valor ganado”. Nos muestran lo que deberíamos llevar vs los que llevamos en cada fecha mostrada en la parte inferior.
2. Es importante saber que las líneas y puntos azules es lo que deberíamos llevar y las líneas y puntos rojos es lo que llevamos.
    1. En dado caso que algún punto rojo esté en la misma posición que algún punto azul significa que la estimación de costo y esfuerzo fue la correcta, por lo tanto, todo se hizo a tiempo y forma.
    2. En dado caso que algún punto rojo esté por encima de algún punto azul significa que ese día se trabajó de MÁS, por lo tanto, se tendrá que ajustar las estimaciones.
    3. En dado caso que algún punto rojo esté debajo de algún punto azul podrá significar dos cosas:
        1. Que no hemos trabajado lo suficiente para llegar a cumplir las tareas de ese día, por lo tanto, deberemos de ajustar nuevamente nuestra forma de trabajo para lograr terminar las tareas a tiempo.
        2. Que nuestras estimaciones no fueron las correctas, ya que creímos que una task nos tomaría más tiempo, por lo tanto, se deberá ajustar dichas estimaciones.

![Untitled](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Untitled%208.png)

## SPI y CPI

1. Primeramente es importante entender que preguntas responde cada una de estas estimaciones.

1. **SPI** responde a ¿Vamos de acuerdo al calendario?
    1. Si en el **SPI** llegamos a ver .75 significa que llevamos un 75% trabajado de acuerdo a nuestro calendario, es decir, nos falta un 25% por terminar.
    2. Si llegamos a ver un 1.00 significa que llevamos un 100% trabajado de acuerdo al calendario, es decir, estamos completos y a tiempo.
    
2. **CPI** responde a ¿Vamos de acuerdo al costo?
    1. Si en el **CPI** vemos .75 significa que estuvimos un 75% cerca de nuestra estimación de costo, es decir, trabajamos un 25% menos de lo que creímos que trabajaríamos; por lo tanto, se debe reestructurar y ajustar las estimaciones.
    2. Si en el **CPI** llegamos a ver 1.15 significa que estuvimos un 115% cerca de nuestra estimación de costo, es decir, trabajamos 15% más de lo que creímos que trabajaríamos; por lo tanto, se debe reestructurar y ajustar las estimaciones.
    3. Si en el **CPI** llegamos a ver 1.00 significa que estuvimos un 100% cerca de nuestra estimación de costo, es decir, toda la estimación fue correcta.
    
    ![Untitled](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Untitled%209.png)
    

[Manejo de versiones ](Como%20LLENAR%20y%20LEER%20las%20tablas%20y%20las%20graficas%20para%20%20796befd2de26494f8e51c3aa1b7588da/Manejo%20de%20versiones%20d16385cbaaa74686a60b462fe4123f4a.md)