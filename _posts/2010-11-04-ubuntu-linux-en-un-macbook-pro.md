---
ID: 629
post_title: Ubuntu Linux en un MacBook Pro
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/04/11/2010/ubuntu-linux-en-un-macbook-pro/
published: true
post_date: 2010-11-04 02:21:54
---
<a href="http://www.nukeador.com/wp-content/uploads/2010/11/ubuntu-mbp.jpg"><img class="aligncenter size-full wp-image-630" title="ubuntu-mbp" src="http://www.nukeador.com/wp-content/uploads/2010/11/ubuntu-mbp.jpg" alt="" width="600" height="452" /></a>

Os detallo algunas consideraciones para tener bien instalado Ubuntu en un MacBook Pro compartiendo espacio con OSX:
<ul>
	<li><a href="https://help.ubuntu.com/community/MactelSupportTeam/AppleIntelInstallation">Seguir la guía oficial de Ubuntu para instalaciones en un Macbook</a>.</li>
	<li><a href="https://help.ubuntu.com/community/MacBookPro6-2/Maverick">Aplicar las optimizaciones pertinentes</a> (en mi caso MBP 6.2 y Ubuntu 10.10)</li>
</ul>
Además he aplicado algunas cosas a mayores para hacerlo todo más fácil.
<h3>Particiones y carpetas</h3>
El tamaño de la partición para Ubuntu que cree fue de 20 Gb.

Para montar automáticamente el disco de OSX, crear la carpeta /media/osx y añadir en el /etc/fstab

<code>/dev/sda2   /media/osx  hfsplus  rw,user,auto,uid=501,gid=20    0  0</code>

Además, para poder escribir con el usuario por defecto de Ubuntu hay que:
<ul>
	<li>Desde OSX desactivar el journaling del disco principal: sudo diskutil disableJournal /dev/disk0s2</li>
	<li>Seguir estos <a href="http://toplessvampires.com/blog/2010/10/changing-ubuntu-uid-pemissions-to-501-for-mac-os-x-dual-booting-method-2/">pasos para cambiar el uid y guid</a> del usuario de Ubuntu.</li>
</ul>
En el home del usuario de Ubuntu borrar todas las carpetas y crear enlaces a las carpetas en el disco de osx (sustituir nuke por tu usuario):
<code>
ln -s /media/osx/Users/nuke/Downloads/ Descargas</code>

<code>ln -s /media/osx/Users/nuke/Documents/ Documentos</code>

<code>ln -s /media/osx/Users/nuke/Pictures/ Imágenes</code>

<code>ln -s /media/osx/Users/nuke/Music/ Música</code>

<code>ln -s /media/osx/Users/nuke/Web/ Web</code>

<code> </code>

<code>ln -s /media/osx/Users/nuke/Movies/ Videos</code>

<code> </code>

<code>ln -s /media/osx/Users/nuke/.fonts/ .fonts</code>

<code>ln -s /media/osx/Users/nuke/Library/Application\ Support/Firefox/ .mozilla/firefox</code>

<code> </code>

<code>ln -s /media/osx/Users/nuke/Library/Thunderbird/ .thunderbird</code>

(Podemos ampliar la lista a todas las carpetas que nos interesen)
<h3>Ventiladores</h3>
Para que los ventiladores no hagan ruido y se comporten más o menos como en OSX, estos son los valores para mi /etc/macfanctl.conf

<code># Config file for macfanctl daemon
#
# Note: 0 &lt; temp_X_floor &lt; temp_X_ceiling
#       0 &lt; fan_min &lt; 6200 </code>

<code>fan_min: 2000</code>

<code>temp_avg_floor: 55 #45
temp_avg_ceiling: 65 #55</code>

<code>temp_TC0P_floor: 55 #50
temp_TC0P_ceiling: 65 #58</code>

<code> </code>

<code>temp_TG0P_floor: 55 #50
temp_TG0P_ceiling: 65 #58</code>

<code> </code>

<code># log_level values:
#   0: Startup / Exit logging only
#   1: Basic temp / fan logging
#   2: Log all sensors</code>

<code> </code>

<code>log_level: 0</code>
<h3>Resumen</h3>
Con estos sencillos pasos, tanto Ubuntu como OSX usarán las mismas carpetas para guardar y trabajar con archivos e incluso podremos tener las configuraciones de algunos programas (Firefox y Thunderbird) iguales en ambos sistemas.