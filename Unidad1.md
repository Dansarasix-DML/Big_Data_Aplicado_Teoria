# Unidad 1: Gestión de Soluciones
---
### Resultados de Aprendizaje

|Contenido|Criterios de Evaluación|
|--|--|
|*Diseño y Construcción de Soluciones*| RA5075.1a - Se ha caracterizado el proceso de diseño y construcción de soluciones en sistemas de almacenamiento de datos. &nbsp; RA5075.2a - Se ha determinado la importancia de los sistemas de almacenamiento para depositar y procesar grandes cantidades de cualquier tipo de datos rápidamente.|
|*Procedimientos y Mecanismos de Ingesta de Datos*|RA5075.1b - Se han determinado los procedimientos y mecanismos para la ingestión de datos.|
|*Formato de Datos Adecuado para el Almacenamiento*|RA5075.1c - Se ha determinado el formato de datos adecuado para el almacenamiento.|
---
### Índice

1. Diseño y Construcción de Soluciones
   1. Introducción de los datos al conocimiento
   2. La carrera entre los datos y la tecnología
   3. Los datos: los de ayer y los de hoy
   4. Soluciones Big Data
   5. Almacenes de datos
      1. Sistemas de ayuda de toma de decisiones
      2. Almacenes de datos: Concepto
      3. Almacenes de datos: Arquitectura
   6. Data Lake
      1. Concepto
      2. Data Lake vs Data Warehouse
2. Procedimientos y Mecanismos de Ingesta de Datos
   1. El proceso de Extracción, Transformación y Carga (ETL)
      1. Extracción
      2. Transformación
      3. Carga
      4. Frameworks ETL
   2. Diseño de Estrella
   3. Diseño de Copo de Nieve
3. Formato de Datos Adecuado para el Almacenamiento
   1. Teorema de CAP
   2. Bases de datos NoSQL
      1. NoSQL vs SQL
      2. Tipos de bases de datos NoSQL
   3. Bases de datos XML
      1. DTD
      2. XML Schema
      3. XPath
      4. XSLT
      5. XQuery
   4. Bases de datos documentales: MongoDB
      1. Características, funciones, método
      2. Ventajas e Inconvenientes
      3. Estructura y uso
   5. Bases de datos basadas en grafos
      1. Características principales
      2. Areas de aplicación

---

### 1. Diseño y Construcción de Soluciones

#### 1. Introducción de los datos al conocimiento

* **Dato**: Es una representación sintáctica, generalmente numérica, que puede manejar un dispositivo electrónico *(normalmente un ordenador)* sin significado por sí solo. Sin embargo, es a su vez fundamental y el elemento de entrada necesario en cualquier sistema y/o proceso que pretenda extraer información o conocimiento sobre un dominio determinado.
* **Información**: Es el **dato** interpretado, es decir, el **dato** con significado. Para obtener información, ha sido necesario un proceso en el que, a partir de un dato como elemento de entrada, se realice una interpretación de ese dato que permita obtener su significado, es decir, información a partir de él. La información es también el elemento de entrada y de salida en cualquier proceso de toma de decisiones.
* **Conocimiento**: Es **información** aprendida, que se traduce a su vez en reglas, asociaciones, algoritmos, etc. que permiten resolver el proceso de toma de decisiones. Así pues, la **información** obtenida a partir de los datos permite generar conocimiento, es decir, aprender. El conocimiento no es estático, como tampoco lo es siempre el aprendizaje. Aprender, construir conocimiento, implica necesariamente contrastar y validar el conocimiento construido con nueva **información** que permita, a su vez, guiar el aprendizaje y construir conocimiento nuevo.

![imagen1](https://jaimerabasco.github.io/CE-IABD_BigDataAplicado_IESGranCapitan/UD1%20-%20Gesti%C3%B3n%20de%20soluciones/images/Figura1.1.jpg)

*Figura 1.1: Relación entre datos, información y conocimiento en el proceso de toma de decisiones. (Fuente: UCLM)*

Por tanto, datos, información y conocimiento están **estrechamente relacionados** entre sí y dirigen cualquier proceso de toma de decisiones. La figura1.1 muestra la relación entre datos, información y conocimiento, en un proceso genérico de toma de decisiones:

Aquí hay un ejemplo:

|Etapa|Ejemplo|
|--|--|
|Obtener Datos|El profesor corrige el examen de Pablo, que ha sacado un 3. Esta calificación, por sí sola, es simplemente un dato.|
|Sacar información|A continuación, el profesor calcula la calificación final de Pablo, en base a la nota del examen, sus trabajos y prácticas de laboratorio. La nota final de Pablo es un 4. Esto último es información.|
|Toma de decisiones|¿Ha aprobado Pablo? La información de entrada al proceso de decisión es su calificación final de 4 puntos, obtenida en el paso anterior. El conocimiento del profesor sobre el sistema de calificación le indica que una nota menor a 5 puntos se corresponde con un suspenso y, en caso contrario, con un aprobado.|
|Sacar información|La información de salida tras este proceso de decisión es que Pablo está suspenso en matemáticas.|
---
|***Pregunta: Siguiendo el ejemplo anterior ¿Cómo se produce el proceso de toma de decisiones para determinar si un número es primo?***|
|--|
---

Aunque se trate de un ejemplo trivial, la importancia del proceso de toma de decisiones no lo es. En **marketing**, por ejemplo, se analizan bases de datos de clientes para identificar distintos grupos e intentar predecir el comportamiento de estos. En el mundo de las **finanzas**, las inversiones realizadas por grandes empresas responden a un proceso complejo de toma de decisiones donde los datos son el eje fundamental de este proceso. En **medicina**, existe una gran cantidad de sistemas de ayuda a la decisión que permiten a los doctores contrastar y validar sus diagnósticos de forma precoz. 

En definitiva, no hay área de conocimiento ni ámbito de aplicación que escape al proceso de toma de decisiones.

#### 2. La carrera entre los datos y la tecnología

Que los **datos** son el elemento fundamental en cualquier proceso y/o sistema de toma de decisiones no es algo nuevo. Sin embargo, los **datos** no siempre han estado al alcance de los expertos y no siempre ha sido posible ni sencillo procesarlos según las necesidades concretas de cada caso de aplicación.

La **información**, por tanto, siempre ha sido poder y el gran reto ha sido y sigue siendo extraer **información** a partir de datos para generar conocimiento. Para ello, es necesario contar con dos factores que deben estar alineados: datos y tecnología.

En el pasado, obtener datos era complicado debido a la limitada disponibilidad y alto costo de los sensores, que además no ofrecían las prestaciones actuales. Por ello, la monitorización de procesos y recolección de datos se enfocaba principalmente en grandes empresas industriales. Ante esta limitación, se utilizaban modelos matemáticos de simulación para generar datos realistas, conocidos como datos sintéticos, en contraste con los datos reales obtenidos de sensores. Además de los datos, es esencial contar con tecnología avanzada para su generación, almacenamiento y procesamiento, lo cual presenta retos tecnológicos significativos.

Generar, almacenar y procesar todos estos datos no es una tarea trivial, y plantea una serie de problemas tecnológicos a resolver.

* El *primer problema tecnológico* a resolver es el almacenamiento. Las soluciones incluyen sistemas de información distribuida, que usan varios ordenadores conectados en red para almacenar datos, y los sistemas en la nube, que permiten alquilar espacio en servidores privados gestionados por un proveedor.
* El *segundo problema tecnológico* es el procesamiento de los datos almacenados. Este aspecto cobra especial relevancia en función del caso de aplicación, pudiendo distinguirse entre procesamiento on-line (en línea/**stream**) y procesamiento off-line (fuera de línea/**batch**).
* 💻 El procesamiento **on-line** o **stream** processing consiste en procesar los datos a medida que se generan, ya que se requiere una respuesta en tiempo real. Un ejemplo es un sistema de control de tráfico, donde los semáforos se ajustan según los datos de tráfico en tiempo real.
* ❎ El procesamiento **off-line** o **batch** processing no requiere que los datos se procesen en tiempo real. Por ejemplo, en la detección de fraude bancario, es posible analizar los movimientos de un cliente de manera posterior, sin necesidad de evaluar cada transacción en el momento en que ocurre.

En este sentido, la **computación distribuida**, en donde múltiples máquinas realizan el procesamiento optimizando el rendimiento o la **computación en la nube**, que permite adquirir recursos de procesamiento al igual que se puede adquirir espacio de almacenamiento, son dos soluciones al problema del procesamiento.

Otras alternativas son la **programación paralela** y la **programación multi-procesador**, que permiten, respectivamente, aprovechar el paralelismo de múltiples hilos de ejecución dentro de un procesador y realizar el procesamiento dividiéndolo en múltiples hilos en diferentes procesadores

|***Pregunta: Piensa en procesos cotidianos que requieran un procesamiento on-line y en otros que requieran un procesamiento off-line.***|
|--|

⏳ La proliferación de sensores asequibles y de alto rendimiento ha generado un aumento exponencial en la cantidad de datos disponibles, permitiendo monitorizar casi cualquier proceso, desde el consumo eléctrico doméstico hasta la actividad física. Aunque la tecnología ha avanzado significativamente, la generación de datos sigue superándola, lo que plantea un reto continuo. Para enfrentar este desafío, la **tecnología** evoluciona tanto en **hardware**, con arquitecturas de mayor capacidad de procesamiento y almacenamiento, como en **software**, mediante modelos que optimizan el manejo de los datos.

#### 3. Los datos: los de ayer y los de hoy
#### 4. Soluciones Big Data
#### 5. Almacenes de datos
##### 1. Sistemas de ayuda de toma de decisiones
##### 2. Almacenes de datos: Concepto
##### 3. Almacenes de datos: Arquitectura
#### 6. Data Lake
##### 1. Concepto
##### 2. Data Lake vs Data Warehouse