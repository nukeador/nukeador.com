---
ID: 103
post_title: Instalador de Beryl para ATI
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/22/02/2007/instalador-de-beryl-para-ati/
published: true
post_date: 2007-02-22 01:38:13
---
<p> <strong>Actualización: </strong>Estas instrucciones sirven para Ubuntu 6.10, a partir de la versión 7.04 la instalación de los controladores de ATI puede hacerse fácilmente desde el menú <em>Sistema - Administración - Gestor de controladores restringidos, </em>aunque con los controladores libres que vienen por defecto admiten aixgl y beryl.</p>
<p>Tras pasearme por el <a href="http://wiki.beryl-project.org/wiki/">wiki de Beryl</a> me tope con un <a href="http://wiki.beryl-project.org/wiki/Install_Beryl_on_Ubuntu_Edgy_with_nVidia#Automatic_installation">script para autoinstalar Beryl en Ubuntu con una gráfica de Nvidia</a>, me pareció tan buena idea que los usuarios más noveles pudieran instalar Beryl con un solo clic que me lancé a modificarlo para que funcionara con las gráficas ATI usando el servidor XGL.</p>
<p>El resultado lo he subido a una nueva página del wiki: <a href="http://wiki.beryl-project.org/wiki/Install_Beryl_on_Ubuntu_Edgy_with_XGL_and_ATI">Install Beryl on Ubuntu Edgy with XGL and ATI</a></p>
<p>Es una primera versión que he probado varias veces en mi pc y me ha funcionado, pero al ser una versión "beta" no deberías instalarla en equipos que se necesiten para trabajar, usadla bajo vuestra responsabilidad.</p>
<p>En resumen y para los que no quieran complicarse:</p>
<p><big><u><strong>Autoinstalador de Beryl para ATI</strong></u></big></p>
<p>Bajamos <a href="/archivos/install-ati.sh">este instalador</a>, lo guardamos en el escritorio mismamente y le damos permisos de ejecución (secundario sobre él, propiedades, permisos, permitir ejecutar el archivo).</p>
<p>Luego solo tenemos que dar alt+f2, nos aparecerá el dialogo de ejecutar aplicación, marcamos la opción de ejecutar en un terminal y en el cuadro de texto escribimos la ruta al archivo bajado precedido de "sudo", en mi caso:</p>
<p><code>sudo /home/nuke/Desktop/install-ati.sh</code></p>
<p>Debes sustituir nuke por el nombre de tu usuario.</p>
<p>Pulsamos ejecutar y nos pedirá la contraseña de administrador. El script se ejecutará y bajará e instalará los drivers de ATI, xgl y beryl.</p>
<p>No cerréis la ventana del terminal hasta que finalice el proceso, una vez finalizado es recomendable borrar el archivo del escritorio y obligatoriamente necesitamos reiniciar.</p>