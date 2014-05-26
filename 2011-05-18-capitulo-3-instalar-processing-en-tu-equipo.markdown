---
layout: post
title: "capítulo 3 - instalar processing en tu equipo"
date: 2011-05-18 18:00
comments: true
categories: processing 
---
*Este artículo fue escrito para la escuela de bits original en mayo de 2011*

Supongo que os pueda parecer raro comenzar por el capítulo 3; pero al ser los dos primeros capítulos meramente introductorios <strike>(ver hoja de ruta)</strike>, he preferido comenzar por este capítulo de forma que podáis pasar a la acción cuanto antes.

Ha llegado el momento de pasar a la acción, para ello lo primero que tendremos que hacer es conseguir la última versión de **Processing** para nuestro sistema operativo.

<!-- more -->

La descarga se realiza desde la página web [http://processing.org/downloads](http://processing.org/downloads). Los usuarios de **Windows** notarán aquí que tienen que escoger entre dos opciones *Processing* y *Processing without Java*. El segundo es una opción reducida para aquellos que hayan instalado por su cuenta el kit de desarrollo de Java (Java SDK), es decir programadores de Java. Si no sabes de qué va esto simplemente escoge la primera opción.

A continuación os describo el proceso de instalación para cada sistema operativo. Es muy sencillo y es una simple traducción de las instrucciones que se encuentran en inglés en la web de Processing.

## Windows
El fichero descargado es un `ZIP`. Tendrás que descomprimirlo. La manera más fácil es hacer doble click y arrastrar la carpeta que contiene, al sitio que quieras, por ejemplo en *Archivos de Programa*, en el *Escritorio* o en *Mis Documentos*. Para arrancar Processing basta hacer doble clic en el archivo `Processing.exe` incluido en esa carpeta.

Si quieres tambien puedes crear un acceso directo a este fichero y colocarlo en el escritorio. Para ello haz clic con el botón derecho en el fichero `Processing.exe` y selecciona la opción *Crear Acceso Directo*.

Después bastará arrastrar el fichero creado en la carpeta de Processing al escritorio. El programa arrancará del mismo modo haciendo doble clic sobre este acceso directo.

## Mac
La versión para Mac OS es un fichero `.dmg`. Arrastra el icono de Processing a la carpeta de *Aplicaciones*. Si usas un ordenador que no es tuyo y no puedes modificar esa carpeta, simplemente arrastra la aplicación al escritorio. Para empezar haz doble clic en el icono de Processing.

En el momento de escribir estas líneas no tengo acceso a un equipo con Mac OS, por lo que no puedo describir los detalles del proceso de instalación, o ayudar a solucionar algún posible problema con la misma.

## Linux
La versión de Linux es un fichero `.tar.gz`. Descargalo a tu carpeta *home*, luego abre una ventana de terminal, y escribe

	tar xvfz processing-xxxx.tar.gz

Sustituye xxx por lo indicado en el fichero que has descargado, se refiere a la versión de Processing. Con esta instrucción se creara una carpeta llamada *processing-1.0*, o algo similar. Entra en el directorio con la instrucción:

	cd processing-xxxx

y lanza el programa con la instrucción:

	./processing

Con un poco de suerte la ventana principal de **Processing** se habrá desplegado en la pantalla. Puede que hayas tenido algún problema, si la configuración de tu equipo es distinta. En [http://wiki.processing.org/w/Troubleshooting](http://wiki.processing.org/w/Troubleshooting) hay una página dedicada a la resolución de problemas, pero está en inglés.
