---
layout: post
title: "capitulo 6 - bota, bota, mi pelota"
date: 2011-05-28 21:09
comments: true
categories: processing
---
Nuestro objetivo en este capítulo es diseñar una animación de una pelota rebotando.

Como hemos visto en el capítulo anterior habrá una sección `setup()` donde programaremos la configuración inicial, y una sección `draw()` donde programaremos la animación propiamente dicha.

Cada ejecución de `draw()` se encargará de dibujar un fotograma de la animación.  La pelota la dibujaremos con la función `ellipse()`, que también hemos visto.

{% gist 3150156 %}

<!-- more -->

Comprobaréis que el código anterior solo dibuja una pelota estática en la parte superior de la pantalla. Necesitamos decidir la nueva posición de la pelota en cada fotograma. Y debemos apuntarla en algún sitio. Processing nos ofrece la variables para apuntar estos valores.

En primer lugar tenemos que declarar la variable. Con esta orden le indicamos a Processing el tipo de la variable (`float`: número real, `int`: número entero, `color`: un color, `String`: una cadena de texto, etc.) seguido de su nombre.

En nuestro usaremos un número real, que llamaremos altura.

{% gist 3150164 %}

Hemos usado `setup()` para inicializar la variable, pero también lo podríamos haber hecho en su declaración con `float altura=0;`

Pero si ejecutáis el programa anterior veréis que la pelota sigue estática. Es necesario actualizar la posición de la pelota en cada iteración. Por ejemplo, `altura=altura+1;` que incrementa en 1 el valor de altura.

Si añadís esta línea y ejecutáis el programa tampoco quedaréis satisfechos, ya que los fotogramas se superponen unos a otros sin conseguir el efecto deseado. Necesitamos borrar el fotograma anterior antes de dibujar el actual. Para ello usaremos el comando `background()`.

Con esto el programa quedará así:

{% gist 3150168 %}

Ahora ya es una animación, pero no hemos cumplido el enunciado. Nos falta el efecto del bote. Para simularlo debemos de comprobar cuando la bola toca los extremos de la pantalla.

La comprobación se hace con la sentencia `if` que en función de que se cumpla o no una condición, ejecuta un bloque de sentencias u otro.

{% gist 3150170 %}	

Finalmente, tenemos una pelota que bota abajo y arriba en la pantalla. Ahora os invito a experimentar, a cambiar valores, probar un rebote horizontal en vez de vertical, o ajustar el rebote para que ocurra en el borde de la pelota en vez de en el centro. Si os atascáis o tenéis cualquier duda no dudéis en preguntar en los comentarios.

<s>Y hablando de botar, ya he llegado a la mitad del mini libro (panfleto) de Introducción a Processing,y tengo que pensar en los próximos artículos de la escuela. ¿Has votado ya en la encuesta que contenidos quieres ver en el blog? No lo dejes para mañana, porque la encuesta estará activa solo una semana.</s> Nos vemos en el próximo capítulo de escuela de bits.
