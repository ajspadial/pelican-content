Category: Blog
Author: Antonio Jesus Sanchez Padial
Title: Crear un blog con octopress
Date: 2012-07-11 20:06
Tags: blog 
Category: Blog
Author: Antonio Jesus Sanchez Padial

En este primer artículo de la nueva (*otra vez*) **Escuela de Bits**, describo los pasos necesarios para montar un sitio como este usando [Octopress][octopress1].

El sitio web de octopress cuenta con instrucciones más detalladas para cada uno de estos apartados, aunque están inglés.

<!-- more -->

## Instalar octopress
*Instrucciones del sitio original: [Octopress Setup](http://octopress.org/docs/setup/)*

En mi instalación ya tenía instalado `git` y `ruby`, por lo que he ignorado esa parte de las instrucciones.

1. Ir a github y **forkear** el proyecto [octopress][octopress]

2. **Clona** el proyecto forkado en tu equipo. Si lo clonas en una carpeta de dropbox (o similar) lo tendrás disponible desde cualquier equipo.

		git clone git://github.com/YOUR_USER/octopress.git octopress

3. **Instala** el tema por defecto de Octopress

		cd octopress
		rake install

## Alojar el blog octopress en github.com

*Instrucciones del sitio original: [Deploying Github Pages](http://octopress.org/docs/deploying/github/)*

1. Crear el **repositorio de destino** en github.com, en mi caso https://github.com/ajspadial/ajspadial.github.com

2. **Configurar octopress** para acceder a este respositorio

		rake setup_github_pages

	Cuando nos pregunta la *read/write url for your repository* hay que responder en el siguiente formato, gracias [Alder101][alder101]:

		git@github.com:ajspadial/ajspadial.github.com.git

## Configurar nuestro blog

*Instrucciones del sitio original: [Configuring Octopress](http://octopress.org/docs/configuring/)*

1. Acceder al fichero **_config.yml** y cambiar los campos oportunos, seguramente *url*, *title*, *subtitle* y *author*

2. La segunda parte del archivo de configuración corresponde a los parámetros por de **Jekyll** sistema sobre el que funciona Octopress. Puedo dejar los valores por defecto, por el momento.


3. Por último, en la tercera sección del fichero podemos configurar algunos parámetros de aplicaciones de terceros, como Twitter, etc.

Puedo dejar los valores por defecto, por el momento.

4. No olvides **actualizar** los cambios

		rake generate
		rake deploy

## Crear nuestro primer contenido

*Instrucciones del sitio original: [Blogging Basics](http://octopress.org/docs/blogging/)*

1. Octopress nos ofrece un comando para **crear posts**

		rake new_post["title"]

	Lo que crea un fichero en la carpeta `source/_posts` nombrado según el formato `yyyy-mm-dd-TITLE.mardown`.

2. **Editar** el fichero. En principio es suficiente respetar la cabecera, pero podemos añadir etiquetas en el apartado tags.

	Detrás de la cabecera escribimos el contenido del artículo usando la sintaxis [markdown][markdown]

3. Una vez completada la edición, publicaremos el post con los comandos:

		rake generate
		rake deploy

	Y actualizaremos
		
		git add .
		git commit -m "Nuevo artículo"
		git push origin source

:wq

[octopress1]: http://octopress.org
[octopress]: https://github.com/imathis/octopress "Octopress source at github.com"
[alder101]: https://github.com/imathis/octopress/issues/301
[markdown]: http://daringfireball.net/projects/markdown/syntax
