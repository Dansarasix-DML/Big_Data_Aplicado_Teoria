# Unidad 1: Gestión de Soluciones
---
### Resultados de Aprendizaje

|Contenido|Criterios de Evaluación|
|--|--|
|*Diseño y Construcción de Soluciones*| RA5075.1a - Se ha caracterizado el proceso de diseño y construcción de soluciones en sistemas de almacenamiento de datos. RA5075.2a - Se ha determinado la importancia de los sistemas de almacenamiento para depositar y procesar grandes cantidades de cualquier tipo de datos rápidamente.|
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

#### 2. La carrera entre los datos y la tecnología
#### 3. Los datos: los de ayer y los de hoy
#### 4. Soluciones Big Data
#### 5. Almacenes de datos
##### 1. Sistemas de ayuda de toma de decisiones
##### 2. Almacenes de datos: Concepto
##### 3. Almacenes de datos: Arquitectura
#### 6. Data Lake
##### 1. Concepto
##### 2. Data Lake vs Data Warehouse