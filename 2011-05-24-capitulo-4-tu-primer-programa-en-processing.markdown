Title: capítulo 4 - tu primer programa en processing
Date: 2011-05-24 18:40
Tags: processing
Category: Blog
Author: Antonio Jesus Sanchez Padial

Una vez abierto Processing escribiremos la siguiente línea.

	ellipse(0,0,50,50);

Y ejecutaremos el programa pulsando el botón `Play`, en la esquina superior izquierda de la interfaz (también sirve `Ctrl + R`). El resultado será una nueva pantalla similar a la siguiente.

{% img http://farm9.staticflickr.com/8423/7604430350_75460fdf82_m.jpg %}


## ¿Qué ha ocurrido?

La instrucción `ellipse` dibuja una elipse, como su propio nombre indica. Los dos primeros parámetros de valor 0, indican las coordenadas x e y del centro de la elipse. Los dos últimos de valor 50, los diámetros de cada uno de los dos ejes. Al tener ambos el mismo valor, la elipse resultante es una circunferencia. Los colores utilizados son los fijados por Processing por defecto, y más adelante aprenderemos a modificarlos.

<!-- more -->

Prueba a ejecutar de nuevo el programa modificando los parámetros del centro (dos primeros valores) y del diámetro, los dos últimos. Puedes comprobar que la esquina superior izquierda es la coordenada 0,0; y que la x crece hacia la derecha y la y hacia abajo.

## La pantalla

Processing nos ofrece las variables width y height para acceder al tamaño de la pantalla.

	ellipse(width, height,50,50);

{% img http://farm8.staticflickr.com/7255/7604430428_d431ff9e17_m.jpg %}

Para conseguir valores proporcionales al tamaño de la pantalla podemos hacer uso de los operadores `+`,`-`,`*` y `/`.

	ellipse(width/2, height/2,50,50);

{% img http://farm9.staticflickr.com/8012/7604430288_8cd93c829e_m.jpg %}
### Referencia

Los comandos de Processing tienen hipervínculos a la referencia (ayuda) de Processing. Este documento está en inglés, <s>pero lo traduciremos gradualmente en la escuela de bits</s>.
