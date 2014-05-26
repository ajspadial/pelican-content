---
layout: post
title: "por qué octopress en vez de drupal?"
date: 2012-08-30 22:50
comments: true
categories: octopress
---
Durante dos años esta [Escuela de Bits]("http://www.escueladebits.com") ha estado basada en **Drupal 6**, y todo ha ido bastante bien.

El único inconveniente de [Drupal](http://drupal.org), para mí, era lo incómodo de escribir y editar los artículos en la web, especialmente cuando estos incluyen ejemplos de código.

Así que empecé a buscar maneras que me facilitarán estas tareas. Mi primera opción fue la de publicar mediante envíos de correo electrónico. Parecía una buena idea. Drupal tiene un módulo para ello, []() y lo usé en un par de artículos. Todo bastante bien, menos a la hora de incluir código.

En este tiempo empecé a usar **git** con asiduidad, y pensé que sería genial poder gestionar mis artículos con este sistema, así que idée un gestor de contenidos que se conectaría a un repositorio git (por ejemplo usando la API de github, o bitbucket). El sistema se llamaba [horns](). Su arquitectura era extremadamente simple, ya que corría en el navegador usando *Javascript*.

<!-- more -->

Publicar un artículo era tan fácil como hacer *push* al repositorio de git. Había sin embargo un inconvenientes que detecté pero no llegué a solucionar: las págginas construídas al vuelo en el cliente, no serían indexadas en Google. Casi nada.

Y más o menos en ese momento alguién (tal vez [mi hermano](http://surreal.asturnazari.es)) me habló de [Octopress](http://octopress.org). ¡Genial!, Octopress unía mi idea de construir un gestor de contenidos en torno a git, añadida a la generación de código estático - que resolvía los inconvenientes de la relación con Google y otros buscadores. Y encima, estaba especialmente orientado a blogs que ofrecen frecuentemente código a sus lectores.

El ego de *mi proyecto* cedió con facilidad a una solución que reunía las características que había ideado para mi gestor de contenidos. Y la verdad, cierto orgullo de ver que dichas características eran las mismas que buscaban decenas y decenas de blogueros técnicos que se están pasando a **Octopress**.

Sigo trabajando con **Drupal** y me parece una herramienta genial para muchísimos tipos de páginas web, sin embargo creo que esta **Escuela de Bits** ha encontrado la horma de su zapato con **Octopress**.

Así que empiezo una nueva temporada del blog, con nuevos ánimos y ganas de contaros ideas y proyectos, y ayudaros con los vuestros.

Y pronto volverán a abrirse los comentarios en la escuela, así que espero vuestras opiniones. Hasta la próxima entrega de Escuela de Bits.

:wq
