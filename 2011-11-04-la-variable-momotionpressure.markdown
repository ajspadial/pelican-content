---
layout: post
title: "la variable momotionpressure"
date: 2011-11-04 17:17
comments: true
categories: [processing, android]
---
Hola a todos, 

en mi aprendizaje de **Processing** para **Android** he echado en falta documentación sobre algunos elementos. En particular, prácticamente no he encontrado nada sobre `motionPressure` que en la documentación del [wiki de processing](http://wiki.processing.org) aparecía apenas citado y descrito como una función.

A través de prueba y error he hecho un pequeño análisis, y como fruto tengo el orgullo de añadir unas pocas líneas a [la documentación del proyecto **Processing**](http://wiki.processing.org/w/Android#Mouse.2C_Motion.2C_Keys.2C_and_Input)

Pero supongo que algunos os preguntáreis aún **¿qué es motionPressure?**. En pocas palabras, con `motionPressure` nos informa de la intensidad de las pulsaciones en la pantalla.

**¿Cómo funciona *motionPressure*?** Se trata de una variable en lugar de una función, que es de tipo `float` (esto si estaba bien en la *wiki*), que Processing actualiza en cada ciclo `draw()` con un valor proporcional a la intensidad de la pulsación.

Valores de `motionPressure`
min: 0
max: 0.3 (en mi dispositivo, un Sony XPERIA 8). Supongo que otros dispositivos podrían devolver otros valores.

Ojo: Processing **no actualiza** `motionPressure` si no hay actualización en pantalla, por lo que en ocasiones pueden devolver un valor de contacto que no corresponde con la realidad. Para evitarlo, podemos añadir la siguiente línea al final del ciclo `draw()`
``` java
motionPressure = 0;
```

En resumen, `motionPressure` es una variable muy interesante, que ahora está un poquito mejor documentada en inglés y en castellano.
