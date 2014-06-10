Category: Blog
Author: Antonio Jesus Sanchez Padial
Title: El muro 2 pvector y operadores lógicos
Date: 2011-07-01 09:37
Tags: processing
Category: Blog
Author: Antonio Jesus Sanchez Padial

En la última entrada nos quedamos con las ganas de destruir nuestro bonito muro, así que es el momento de empezar.

En primer lugar añadiremos una pelota en movimiento, esto ya lo hemos estudiado en capítulos anteriores. Usaremos un nuevo tipo de variable para almacenar la posición, el **PVector**. Y sendas funciones para dibujar la pelota y actualizar su posición.

{% gist 3475807 %}

Hay dos cosas fundamentales en este trozo de código. <!-- more -->Por un lado nuestro primer uso de **objetos**, en este caso de tipo PVector. Los objetos son tipos especiales de variables. Se declaran igual que int, etc., pero es necesario inicializarlas: es decir, reservar memoria para ellas. Esto se hace con la función new(), que podemos ver en el setup() de nuestro ejemplo.

Los objetos como PVector ofrecen al programador **atributos** y **métodos**. Accedemos a ambos por medio de la sintáxis '.'. Los **atributos** son variables internas que almacenan las características del objeto. PVector tiene como atributos valores reales (float) llamados x e y. Por ejemplo, en la línea 9, accedemos al atributo x escribiendo pelotaPos.x.

Los objetos también ofrecen **métodos**. Son funciones internas que pueden acceder a los atributos del objeto sin necesidad de indicarlo en la llamada a la función. PVector ofrece distintas funciones para el trabajo con vectores. En la línea 22, vemos la llamada a la función add(), que suma un vector a otro.

Por otro lado en la condición de choque de la pelota he introducido un nuevo operador: **||**. Se trata del operador lógico OR. El resultado de OR es cierto (true) si **alguno** (cualquiera) de los dos valores operados (a la izquierda y derecha de ||) es cierto.

Existen otros operadores lógicos, por ejemplo AND, representado con **&&**. Este operador sólo es cierto, si **todos** los valores operados lo son.

Llegados a este punto podemos añadir el código de dibujo del muro del último artículo de la web. Al hacerlo veréis que no le hemos explicado a **Processing**, cómo debe botar la pelota contra los ladrillos.

Para hacerlo debemos comprobar la posición de la pelota contra cada uno de los ladrillos. Podéis apostar que cada vez que aparezca una expresión del tipo *cada uno* en vuestra descripción de un efecto, habrá un bucle `for` implicado.

``` java
void actualizaPelota() { 
  // ... resto del código ya visto 
  for (int i = 0; i < 5; i++) { 
    for (int j = 0; j < 17; j++) { 
      int desplazamientoX = 0; 
      int desplazamientoY = altoLadrillo * 2; 
      if (i % 2 == 0) 
        desplazamientoX = - anchoLadrillo / 2;
        int minimoX = desplazamientoX + j * anchoLadrillo;
        int maximoX = minimoX + anchoLadrillo; 
        if (minimoX <= 0) 
          minimoX = 0; 
        int minimoY = desplazamientoY + i * altoLadrillo; 
        int maximoY = minimoY + altoLadrillo; 
        if ((pelotaPos.x >= minimoX) && (pelotaPos.x <= maximoX) && (pelotaPosY >= minimoY) && (pelotaPos.y <= minimoY)) {
          // colisión 
          pelotaVel.x = -pelotaVel.x; 
          pelotaVel.y = -pelotaVel.y; 
        } 
      } 
  } 
}
``` 

Cuando añadáis este código veréis que la pelota ya bota contra los ladrillos, pero aún no los destruye. Para ellos deberemos llevar la cuenta de qué ladrillos quedan puestos y cuales no. Resolveremos ese problema aprendiendo a usar los **arrays** en el próximo artículo de **escueladebits.com**. También introduciremos la interacción con la raqueta.

¿Lo habéis probado ya? ¿Funciona correctamente? ¿Quieres modificar algo pero no consigues el resultado esperado? No dejes de enviar tus preguntas en los comentarios de los artículos, en la sección contacto, o en la página de Facebook. Nos vemos en los bits.
