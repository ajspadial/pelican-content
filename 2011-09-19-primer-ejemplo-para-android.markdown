Category: Blog
Author: Antonio Jesus Sanchez Padial
Title: primer ejemplo para android
Date: 2011-09-19 10:43
Tags: processing
Category: Blog
Author: Antonio Jesus Sanchez Padial

Una de las principales diferencias de programar para **Android** respecto al PC (o+ Mac) es el uso del ratón. Los dispositivos Android no suelen tener ratón o equivalente y algunos elemetos de **Processing** como `mouseClicked` no tienen sentido.

Processing nos facilita la vida de todos modos, y viejos conocidos como `mouseX`, `mouseY` siguen estando disponibles, ofreciendo la última pulsación en la pantalla.

En el siguiente código se muestra como podemos arrastrar una imagen por la pantalla de nuestro dispositivo.

{% gist 3476335 %}

Otra diferencia con respecto a la programación de nuestro ordenador, es el uso de la función `size()`. En Android el tamaño de la pantalla está fijado por las dimensiones del dispositivo, por lo que no podemos fijar el tamaño. Es suficiente con no hacer uso de ella.

Podéis escoger cualquier imagen que queráis para substituir el seat.png del ejemplo, Processing admite todos los tipos más populares de ficheros gráficos (.jpg, .gif, .png, ...). Debéis almacenar dicho fichero en una carpeta `data` dentro de la carpeta de vuestra aplicación.

Con esto ya tendréis vuestra primera y sencila aplicación para Android hecha en Processing. No dudéis en dejar vuestras dudas o ideas en los comentarios, hasta la próxima sesión.
