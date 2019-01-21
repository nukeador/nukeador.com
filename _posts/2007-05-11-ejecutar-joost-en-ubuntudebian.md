---
ID: 126
post_title: Ejecutar Joost en Ubuntu/Debian
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/11/05/2007/ejecutar-joost-en-ubuntudebian/
published: true
post_date: 2007-05-11 23:40:38
---
¿Qué es Joost?  Joost una nueva forma de ver la televisión por Internet a la carta, ver lo que quieras, cuando quieras. Decenas de canales a tu disposición. ¡Y gratis!
<p style="text-align: center"><img src="/images/joost.jpg" title="Joost Logo" alt="Joost Logo" /></p>
<p style="text-align: left">Desgraciadamente aun no han publicado en cliente para Linux (aunque está basado en XULRunner como Mozilla), por lo que tendremos que tirar de Wine para instalarlo, el único problema es que necesitamos un wine parcheado, podemos <a href="http://ubuntuforums.org/showthread.php?t=438543">parchear el código fuente como indican en ubuntuforums</a> o bajar directamente un Wine ya parcheado.</p>
<p class="download"><a href="http://doktorseven.miskie.net/files/wine_0.9.36~winehq0~ubuntu~7.04-3_i386.deb" title="Wine parcheado para Joost">Descargar Wine con los parches para Joost (paquete .deb)</a></p>
Lo instalamos con un doble clic y una vez instalado debemos modificar un par de cosas para que funciona bien. Pulsamos <em>alt+f2</em>, escribimos <em>winecfg</em> y aceptamos.

Asegúrate que aparece "Windows XP" en la opción desplegable de la primera pantalla, sino selecciónalo. En la pestaña "Audio" debe estar seleccionada solo la opción OSS Driver y la opción "Aceleración Hardware" a emulación junto con "Emulación de manejador". En la pestaña "Gráficos" debes tener la opción "Emular un escritorio virtual" y con valores 800 x 600.

Ahora instalamos Joost abriendo el .exe con wine o desde la línea de comandos:

<em>wine JoostSetup-FriendsEdition-0.10.2.exe</em>

Para ejecutarlo nos vamos a la carpeta donde lo hayamos instado, en mi caso:

<em>cd .wine/drive_c/Archivos\ de\ programa/Joost/</em>

Y lo ejecutamos así:

<em>wine xulrunner/tvprunner.exe application.ini  </em>
<p style="text-align: center"><a href="/images/joost-wine.jpg" title="Joost en Ubuntu bajo wine" rel="lightbox"><img src="/images/joost-wine-small.jpg" title="Joost Wine" alt="Joost Wine" height="234" width="300" /></a></p>
Fácil, sencillo y para toda la familia :D

Opcionalmente nos podemos crear un archivo para ejecutarlo, <em>Crear documento - Archivo vacío</em> y ponemos:

<em>wine $HOME/.wine/drive_c/Archivos\ de\ programa/Joost/xulrunner/tvprunner.exe $HOME/.wine/drive_c/Archivos\ de\ programa/Joost/application.ini </em>

Guardamos, cerramos, secundario sobre el archivo, <em>Propiedades - Permisos</em>, "Permitir ejecutar".

Ya podremos abrir Joost desde el archivo indicándole ejecutar al intentar abrirle.