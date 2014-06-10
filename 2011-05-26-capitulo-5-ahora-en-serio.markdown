Category: Blog
Author: Antonio Jesus Sanchez Padial
Title: capitulo 5 - ahora en serio
Date: 2011-05-26 20:23
Tags: processing
Category: Blog
Author: Antonio Jesus Sanchez Padial

Hay algo más en **Processing** que primitivas. Si has jugado un poco con ellas habrás visto que aunque interesantes, pueden ser un poco aburridas. El primer paso para crear un sistema interactivo, que atienda a las acciones del usuario, es ver la estructura de un programa en Processing.

	void setup() {
	 // iniciacion 
	}
	 
	void draw() {
	 // proceso 
	}

Estos  bloques se llaman **funciones**, en la función `setup()` pondremos el código que haya que ejecutar al comenzar nuestro programa. Sólo se ejecuta una vez. Solemos alojar en ese bloque la configuración inicial de nuestro programa como el tamaño de la pantalla, colores, etc.

En `draw()` colocaremos el código que forma el núcleo de nuestra aplicación. Processing se encargará de llamarla una vez tras otra hasta que finalicemos la aplicación, bien cerrando la ventana, bien con el botón `stop` del entorno de Processing.

<!-- more -->

Vamos a ver un ejemplo, no dejéis de probarlo en vuestro editor de Processing:

	void setup() {
	  size(200,200); 
	}
 	
	void draw() { 
	  ellipse(width/2, height/2, mouseX, mouseY); 
	}

Ahora sí hemos creado un sistema interactivo de verdad, ¿no? Como véis he introducido dos variables del sistema nuevas `mouseX` y `mouseY`, en las que podemos consultar a Processing la posición del ratón en la pantalla.

Hasta aquí llega esta capítulo, no dejéis de enviar a la web vuestra dudas, comentarios, y por supuesto **¡¡vuestros primeros pasos con processing!!**

{% blockquote ajspadial http://escueladebits.com/content/cap%C3%ADtulo-5-ahora-en-serio-tu-primer-programa#comment-213776306 %}
Apunte para mí mismo, cuando redactes el capítulo para el libro comenta brevemente el uso de llaves, paréntesis y ";"
{% endblockquote %}

{% blockquote @evgalvan http://escueladebits.com/content/cap%C3%ADtulo-5-ahora-en-serio-tu-primer-programa#comment-425448041 %}
y la importancia de las mayúsculas o minúsculas
{% endblockquote %}
