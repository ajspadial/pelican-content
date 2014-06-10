Category: Blog
Author: Antonio Jesus Sanchez Padial
Title: capítulo 8.2 - dinámica
Date: 2011-06-22 17:27
Tags: processing
Category: Blog
Author: Antonio Jesus Sanchez Padial

En la anterior publicación del [capítulo 8](/blog/2011/06/15/capitulo-8-interaccion/) quedaron definidos algunos elementos del juego como el suelo, el muro o la pala del pelotari. He dejado para esta edición lo concerniente a la pelota.

La pelota de esta versión tendrá una parte común con la que vimos en el [capítulo 6](/blog/2011/05/28/capitulo-6-bota-mi-pelota/), aunque en este caso tendremos que añadir un movimiento horizontal que acerque y aleje a la pelota del muro, incluyendo su rebote.

Añadiremos variables para controlar la posición (como la variable altura del capítulo 6) y la velocidad del pelota (como la variable incremento del mismo capítulo).

{% gist 3437796 %}

<!-- more -->

Podemos ajustar el comportamiento de la pelota , modificando los valores iniciales de `velXPelota` y `velYPelota`.

Ahora vamos a añadir la interacción con el pelotari, en `updatePelota()` habrá que añadir una condición para el caso de que la pelota toque la paleta.

{% gist 3437865 %}

Ya tenemos el esqueleto del juego, si bien faltan todos los detalles como la puntuación, las vidas, etc. También hacer el juego un poco más jugable, aunque eso os lo dejo como ejercicio, por ejemplo haciendo que la pelota pierda velocidad en cada rebote. ¿Qué estrategia se os ocurre para conseguirlo?

