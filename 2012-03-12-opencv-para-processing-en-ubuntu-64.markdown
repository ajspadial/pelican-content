---
layout: post
title: "opencv para processing en ubuntu 64"
date: 2012-03-12 16:45
comments: true
categories: [processing, opencv]
---
Hola a todos,

Tras una incursión por el taller de [Big Games](http://uncoded.es/biggames) que se celebró hace un par de semanas en Medialab-Prado (Madrid) me he puesto a instalar opencv en processing.

Para ello es necesario instalar OpenCV, y una librería para Processing (y Java) que actúa de intermediario. [Se puede descargar de aquí] (http://ubaa.net/shared/processing/opencv).

El inconveniente es que esta librería parece no funcionar en las versiones de 64 bits de Ubuntu. A continuación os cuento como lo solucioné, de forma que podáis practicar si usáis este sistema operativo.

<!-- more -->

En primer lugar tuve que sustituir el OpenJDK (java open source) que tenía en Ubuntu por la versión *oficial* de <s>Sun</s> Oracle, ya que parecía que OpenJDK daba algún problema con la librería de captura de vídeo. De todos modos, no puedo asegurar que esto sea necesario para hacer funcionar la librería de OpenCV, ya que no lo he experimentado.

A continuación descubrí en el foro de processing, que es necesario recompilar la librería de opencv. Se trata del mensaje #59 del usuario *minmuz*, [al final de esta págin] (http://processing.org/discourse/yabb2/YaBB.pl?num=1238338691/45)

El comando javah genera una cabecera .h de **C**, pero lo hace a partir del código compilado en Java. Es necesario que compiles las fuentes (archivos java) de la librería OpenCV para Processing. El comando para compilar Java, es `javac`.

``` bash
javac Blobs.java
javac OpenCV.java
```

Con esto conseguirás los archivos de tipo `.class` que son los que necesita `javah`.

Una vez creada esta cabecera hay que recompilar la librería de C++, para ello se usa el comando `g++` del foro citado.

Para conseguirlo tuve que descargar todas las cabeceras (*headers*), ya que no las tenía en mi sistema. Las podéis encontrar en [koders](http://www.koders.com/c/fidEEBBA0C88A62051A9FFAD3F516721120F0C3E3AE.aspx)

Sencillamente fui descargándolas conforme el compilador iba avisando de que faltaban.

Por último las librerías `-lcv` y `-lhighgui` tenían otro nombre en mi instalación. Para averiguar qué nombre tienen esas librerías en tu sistema seguí [las instrucciones de este foro](http://ubuntuforums.org/howthread.php?t=683555)

Este es el comando
``` bash
pkg-config --libs opencv
```

Esto nos da un listado completo de las librerías opencv en nuestro sistema. Me guíe por el nombre para decidir cuales eran las alternativas a las `lcv`, y `lhighgui` que no encontraba. En mi caso los sustituí por `lopencv_core`y `lopencv_highgui`.

Espero que esto sirva a quiénes hayan encontrado algún problema con este asunto. Si mi explicación no está clara, o tenéis algún problema en alguno de los pasos no dudéis en escribir a la escuela, o dejar un comentario. Intentaré ayudaros en base a mi experiencia con este asunto.

Un saludo a todos, ¡y a por los bits!

