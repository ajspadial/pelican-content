Title: el muro 3. introducción al array
Date: 2011-07-05 10:00
Tags: processing
Category: Blog
Author: Antonio Jesus Sanchez Padial


Hasta este momento hemos puesto ladrillos y hecho botar nuestra pelota destructora, pero ... ¡todavía no destruye nada!

Para simular la destrucción de los ladrillos debemos tener una variable que almacene el estado de cada uno de ellos. Sin embargo, como a la hora de dibujarlos, puede parecer complejo controlar 80 variables con el estado de cada uno de los ladrillos. **Processing** como la mayoría de los lenguajes de programación, nos ofrece una estructura de datos para estos casos: el **array**. Mantengo la nomenclatura inglesa, porque ninguna de las traducciones o adaptaciones de array al castellano se ha impuesto entre los programadores, aunque en algunos lugares se pueda hablar de *arreglos*, *vectores*, o *matrices*.

El `array` es una variable que se declara con un tamaño dado, por ejemplo 80, y que se puede acceder a cada uno de sus valores con un índice, posición 7, por ejemplo. Podemos imaginarlo como una especie de casillero. Veamos unos ejemplos de declaración y acceso a un array.

``` java
int[] ejemplo; // declaración de la variable 
ejemplo = new int[20]; // reserva de memoria, tamaño 20 
ejemplo[0] = 1; // acceso a la primera casilla 0 
ejemplo[19] = 29; // acceso a la última casilla 19 
```

<!-- more -->

Usamos los corchetes, **[ ]** para declarar que la variable será un `array`. Antes de usarla por primera vez, debemos indicarle a Processing, qué tamaño necesitamos. Para ello usamos `new`, como en el caso de los objetos. Por último accedemos a cada posición del `array`, haciendo uso de los corchetes. Por su naturaleza, solemos trabajar con los `arrays` mediante bucles, como `for`.

``` java
PVector[] puntos; // declaramos un array de objetos PVector
puntos = new PVector[20]; // reservamos memoria para 20 huecos
for (int i=0; i<20;i++) { // Recorremos nuestro array 
  puntos[i] = new PVector(); // debemos reservar memoria para cada PVector   
  puntos[i].x = random(width); // y le damos valores iniciales a sus atributos 
  puntos[i].y = random(height); 
} 
for (int i=0;i<puntos.length;i++) {
}
```

Creo que ya ha llegado el momento de integrar esto en nuestro juego del muro, de modo que empecemos a ver caer ladrillos. Usaremos un array de tipo **bool**. Las variables bool solo pueden tener los valores verdadero (*true*) o falso (*false*).

{% gist 3476104 %}

Podéis encontrar en el código la inicialización del `array`, por un lado con `new`, y por otro lado un `for` que lo recorre y pone a `true` todas las casillas.

Los valores del `array` se comprueban en otras tres ocasiones:

1. al pintar el muro, comprobamos que exista el ladrillo
2. al calcular la colisión, idem
3. en caso de colisión, ponemos a false el valor del ladrillo

Cuando ejecutéis el programa, veréis que hay algunas (bastantes) imperfecciones en el cálculo de las colisiones. Es algo que resolveremos en la próxima entrada de esta colección, donde ya empezaremos a pulir los detalles, y que nuestro **El Muro** empiece a parecer un juego de verdad.

Un saludo a todos, hasta la próxima escueladebits
