---
ID: 94
post_title: Autopackage
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/15/01/2007/autopackage/
published: true
post_date: 2007-01-15 00:11:51
---
Hace tiempo que leí algo sobre <a href="http://es.wikipedia.org/wiki/Autopackage" title="Wikipedia - Autopackage">autopackage</a>, pero no ha sido hasta ayer cuando al ir a la web de <a href="http://amsn-project.net/index.php" title="Amsn">Amsn</a> para ver si había algún paquete <abbr title="Un paquete para Ubuntu/Debian">deb</abbr> de su última versión, me encontré como descarga por defecto el formato .package

<div style="text-align: center"><img src="http://autopackage.org/gfx/logo_large.png" alt="Autopackage logo" /></div>

Básicamente consiste en <strong>un ejecutable compatible con todas las distribuciones de linux</strong>, esto es, que no necesitarás bajar un deb para Ubuntu/Debian, un rpm para Suse o Mandriva... o incluso bajar un tar.gz con los binarios. 

Simplemente bajaríamos el .package y le daríamos doble clic para instalar, si es la primera vez que instalamos un archivo de este tipo, se nos bajarán las librerías de autopackage y a continuación comenzaría el asistente gráfico que instalará el programa tanto sin permisos de administrador para un solo usuario (en el home) o con ellos para todos (en el /urs).

La ventaja, es que en el .package <strong>se pueden incluir todas las dependencias</strong> o sino autopackage las descargará (si es que no las tenemos ya instaladas y no están incluidas). Esto es importante para las instalaciones sin red.

<div style="text-align: center"><a href="http://upload.wikimedia.org/wikipedia/commons/f/f8/Autopackage_screenshot.png" rel="lightbox[autopackage]"><img src="http://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/Autopackage_screenshot.png/250px-Autopackage_screenshot.png" alt="Autopackage logo" /></a></div>

También incluye una utilidad centralizada para ver y/o desinstalar los programas que hayamos instalado por este método.

<div style="text-align: center"><a href="http://lwn.net/images/ns/autopackage.manager.png" rel="lightbox[autopackage]"><img src="http://lwn.net/images/ns/autopackage.manager.png" width="300" height="200" alt="Autopackage Manager" /></a></div>

Otra buena forma de instalar cosas fácilmente en Linux.