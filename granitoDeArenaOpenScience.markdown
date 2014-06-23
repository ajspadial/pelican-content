Title: Un granito de arena para el Open Science
Author: Antonio Jes�s S�nchez Padial
Date: 2014/06/23
Category: Blog
Tags: Open Science

Hace ya muchos a�os que ten�a la espinita clavada de hacer una contribuci�n a alg�n proyecto Open Source. A�n recuerdo explorar las repositorios de **SourceForge** en los primeros a�os 2000, en busca de un proyecto que me hiciera til�n. Pero me parec�a una tarea reservada a colosos. El solo hecho de tener que comprender el c�digo de terceros se me antojaba una tarea formidable: era uno de esos programadores que prefer�a empezarlo todo de cero.

10 a�os despu�s todo cambi�. No puedo identificar el momento exacto, aunque s� algunos textos y autores que me inspiraron. Creo que conocer a la comunidad **Drupal** tuvo algo o mucho que ver. Tambi�n empezar a leer sobre las *humanidades digitales*. Creo que empec� a comprender el c�digo como otra cosa, como una obra cultural. La verdad que no lo s� muy bien. Pero empec� a leer c�digo de terceros. Primero m�dulos de Drupal, y despu�s el *core* del proyecto. Mentir�a si dijera que que lo llegu� a comprender por completo, pero mi mente *evolucion�*.

**Git** y **GitHub** tuvieron mucho que ver tambi�n. Y por supuesto las horas en Tyba trabajando en equipo despu�s de haber sido tantos a�os un lobo solitario.

Hace poco m�s de un mes me un� al Instituto Nacional de Investigaci�n y Tecnolog�a Agraria y Alimentaria, y una de mis primeras tareas fue hacerme cargo de la parte t�cnica de nuestras revistas cient�ficas. Usamos una versi�n modificada de **Open Journal System**.

As� que pas� los primeros d�as colocando nuestras modificaciones en *commits* independientes de la rama oficial del proyecto. Fue escalofriantemente f�cil. Ahora todo nuestro c�digo particular estaba perfectamente diferenciado del c�digo oficial. **�Pod�amos actualizar el sistema de manera indolora a cualquier versi�n futura!** En las pr�ximas semanas escribir� un tutorial explicando los pasos que segu� para esto, de forma que pueda servir a otros que se enfrenten al mismo problema.

Un poco m�s tarde, la unidad de publicaciones me coment� que echaba en falta una [funcionalidad en la b�squeda del sistema](https://github.com/pkp/ojs/pull/177). Aunque todav�a no sab�a manejar la aplicaci�n como usuario, ya sab�a como encontrar la clase que controlaba esa b�squeda as� que a�ad� media docena de l�neas. 
Cre� una nueva rama del proyecto espec�ficamente para dicho *commit*. Aprend� a usar `git cherry-pick`. Y me anim� a ofrecer mi c�digo al proyecto original con un **Pull Request**. Me aconsejaron unos cambios, y una vez hechos la nueva opci�n de b�squeda forma parte de la versi�n 2.4 de Open Journal System.

Es un peque�a gota de agua en un super proyecto como Open Journal System, en el oc�ano del *software libre*. Pero me siento encantado de saber que puede ser �tli para otros usuarios del programa (m�s de 24.000 revistas en todo el mundo).

En fin, que escribo estas l�neas porque s� que este es solo el primer paso, que espero tener muchas m�s oportunidades para compartir mi *arte* con el mundo, y que si alguien se anima a contribuir su esfuerzo a sus programas favoritos, seguro que todos ganamos.

Os dejo, me voy a domar unos bits.

:wq


