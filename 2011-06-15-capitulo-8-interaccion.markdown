---
layout: post
title: "capítulo 8 - interacción"
date: 2011-06-15 09:02
comments: true
categories: processing
---
*El capítulo 7 estará dedicado a las funciones en **Processing**. Puesto que ya hemos avanzado este tema de mano del blog [Processing Cafe](http://processing.mondonerd.com/tutorial/372), paso al siguiente capítulo dedicado a la interacción.
La versión final del **Primeros Pasos con Processing** si contará con un capítulo 7 dedicado a las funciones.*

En deferencia desde el tiempo pasado desde la última entrada voy a publicar esta en varias notas sucesivas, de forma que podáis ir leyendo sin tener que esperar a que termine por completo de escribir este capítulo

En el [capítulo 6](/blog/2011/05/28/capitulo-6-bota-mi-pelota/) aprendimos como realizar una animación sencilla, una pelota que caía y botaba. En este haremos un juego de frontón, que será una especie de versión simplificada del mítico **Pong**. En lugar de la típica vista cenital del campo de juego, reproduciremos un alzado del perfil.

Verdaderamente, deberíamos dedicar un apartado al diseño del juego, describiendo el aspecto que se quiere conseguir, las reglas, etc. Para evitar extenderme en una guía breve como ésta, voy a describir el diseño conforme os muestro el código, pero esto solo es recomendable hacerlo para un juego de proporciones tan reducidas como éste.

<!-- more -->

En primer lugar dibujaremos el terreno de juego. Vamos a hacerlo creando unas funciones específicas para ello, `dibuja_fronton()` y `dibuja_suelo()` . Esto añade un poco de complejidad a la hora de diseñar y escribir el programa, pero hace mucho más sencillo leerlo y modificarlo más adelante.

Ahora añadiremos nuestra pala de pelotari. También introduciremos una función para ello. Vamos a cambiar la estructura del programa, e introducir el bloque draw().

{% gist 3158752 %}
 
Con esto ya tenemos tres de los cuatro elementos básicos de nuestro de frontón, solo nos falta la pelota. En la próxima entrada del blog describiremos el funcionamiento de la pelota, añadiendo las reglas básicas (o físicas) del juego, como los rebotes, etc.

Por último, y a modo de curiosidad, os dejo este video en el que se muestra el primer videojuego electrónico con gráficos interactivos: **Tennis for Two**, que también utilizaba una vista en alzado para simular un partido de tenis.

<iframe width="420" height="315" src="http://www.youtube.com/embed/s2E9iSQfGdg" frameborder="0" allowfullscreen></iframe>
