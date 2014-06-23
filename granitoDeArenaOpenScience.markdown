Title: Un granito de arena para el Open Science
Author: Antonio Jesús Sánchez Padial
Date: 2014/06/23
Category: Blog
Tags: Open Science

Hace ya muchos años que tenía la espinita clavada de hacer una contribución a algún proyecto Open Source. Aun recuerdo explorar las repositorios de **SourceForge** en los primeros años 2000, en busca de un proyecto que me hiciera tilín. Pero me parecía una tarea reservada a colosos. El solo hecho de tener que comprender el código de terceros se me antojaba una tarea formidable: era uno de esos programadores que prefería empezarlo todo de cero.

10 años después todo cambió. No puedo identificar el momento exacto, aunque sí algunos textos y autores que me inspiraron. Creo que conocer a la comunidad **Drupal** tuvo algo o mucho que ver. También empezar a leer sobre las *humanidades digitales*. Creo que empecé a comprender el código como otra cosa, como una obra cultural. La verdad que no lo sé muy bien. Pero empecé a leer código de terceros. Primero módulos de Drupal, y después el *core* del proyecto. Mentiría si dijera que que lo llegué a comprender por completo, pero mi mente *evolucionó*.

**Git** y **GitHub** tuvieron mucho que ver también. Y por supuesto las horas en Tyba trabajando en equipo después de haber sido tantos años un lobo solitario.

Hace poco más de un mes me uní al Instituto Nacional de Investigación y Tecnología Agraria y Alimentaria, y una de mis primeras tareas fue hacerme cargo de la parte técnica de nuestras revistas científicas. Usamos una versión modificada de **Open Journal System**.

Así que pasé los primeros días colocando nuestras modificaciones en *commits* independientes de la rama oficial del proyecto. Fue escalofriantemente fácil. Ahora todo nuestro código particular estaba perfectamente diferenciado del código oficial. **¡Podíamos actualizar el sistema de manera indolora a cualquier versión futura!** En las próximas semanas escribiré un tutorial explicando los pasos que seguí para esto, de forma que pueda servir a otros que se enfrenten al mismo problema.

Un poco más tarde, la unidad de publicaciones me comentó que echaba en falta una [funcionalidad en la búsqueda del sistema](https://github.com/pkp/ojs/pull/177). Aunque todavía no sabía manejar la aplicación como usuario, ya sabía como encontrar la clase que controlaba esa búsqueda así que añadí media docena de líneas. 
Creé una nueva rama del proyecto específicamente para dicho *commit*. Aprendí a usar `git cherry-pick`. Y me animé a ofrecer mi código al proyecto original con un **Pull Request**. Me aconsejaron unos cambios, y una vez hechos la nueva opción de búsqueda forma parte de la versión 2.4 de Open Journal System.

Es un pequeña gota de agua en un super proyecto como Open Journal System, en el océano del *software libre*. Pero me siento encantado de saber que puede ser útil para otros usuarios del programa (más de 24.000 revistas en todo el mundo).

En fin, que escribo estas líneas porque sé que este es solo el primer paso, que espero tener muchas más oportunidades para compartir mi *arte* con el mundo, y que si alguien se anima a contribuir su esfuerzo a sus programas favoritos, seguro que todos ganamos.

Os dejo, me voy a domar unos bits.

:wq
