---
ID: 398
post_title: Instalando Cyanogenmod en la Magic
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/15/01/2010/instalando-cyanogenmod-en-la-magic/
published: true
post_date: 2010-01-15 13:56:13
---
Nunca me había planteado seriamente modificar la versión de Android que traía mi <strong>HTC Magic de Vodafone</strong> porque estaba a gusto con ella y me gustaba la idea de tener actualizaciones automáticas de Google, pero el otro día revisando las novedades de <strong>la rom <a href="http://www.cyanogenmod.com/">Cyanogenmod</a></strong> me entró el gusanillo y quise probarla.

<img class="aligncenter size-full wp-image-399" title="cyanogenlogo" src="http://www.nukeador.com/wp-content/uploads/2010/01/cyanogenlogo.png" alt="" width="450" height="65" />
<h3><!--more-->¿Qué ofrece?</h3>
<strong><a href="http://www.cyanogenmod.com/">Cyanogenmod</a> es una versión cocinada de Android que incluye muchas de las mejoras de las próximas versiones</strong>, además de acceso completo al sistema (root), algunas de las cosas que me llamaron la atención:
<ul>
	<li><strong>Acceso root al sistema</strong>, para cacherrear todo lo que quiera.</li>
	<li>Posibilidad de <strong>compartir la conexión 3G</strong> mediante usb o convirtiendo el móvil en un punto de acceso wifi.</li>
	<li><strong>Multitouch</strong> portado desde Android 2.0.</li>
	<li>Posibilidad de <strong>compartir archivos por Bluetooth</strong> (sí, son ese tipo de cosas que nadie se explica que no tuvieran los dispositivos Android, ni los iPhones...).</li>
	<li>Portadas algunas de las <strong>aplicaciones de la versión 2.0 de Android</strong> (página principal, tema...).</li>
	<li><strong>Mejoras de rendimiento</strong> (lo explico más adelante).</li>
	<li><strong>Sistema propio de actualización</strong> (hay una aplicación que actualiza comodamente entre versiones de cyanogenmod)</li>
</ul>
El proceso de instalación es bastante sencillo, y en el <a href="http://www.cyanogenmod.com/wiki-page">wiki de Cyanogenmod</a> viene perfectamente explicado. Tras determinar <a href="http://wiki.cyanogenmod.com/index.php/How_to_determine_if_you_have_32A_or_32B">que versión de HTC Magic tenía</a>, seguí los pasos del <a href="http://wiki.cyanogenmod.com/index.php/Full_Update_Guide_-_MT3G/Magic_Firmware_to_CyanogenMod#Non-TMobile_32B_Magics">tutorial para instalar Cyanogenmod en HTC Magic</a> sin olvidar hacer un backup previamente con la utilidad nanbackup que trae el cargador de arranque, de esta forma puedo reinstalar la versión de Android de Vodafone cuando quiera sin problemas.
<h3>Impresiones</h3>
Llevo un par de días trasteando con ella y no puedo estar más contento, la mejora respecto a la versión 1.6 de Vodafone que tenía instalada es bastante grande. Además de las ventajas obvias de tener acceso completo al sistema y poder trastear con él a gusto, compartir la conexión con el portatil... etc para mi la más importante es el <strong>aumento de rendimiento y el incremento de uso de batería</strong> (ayer estuve usando bastante el móvil con música y demás y por la noche  tenía aún el 52% de batería, cosa que antes podría estar en torno al 20%).

<img class="aligncenter size-full wp-image-402 captura" title="Cyanogen 4.2.13 en HTC Magic" src="http://www.nukeador.com/wp-content/uploads/2010/01/CAP201001151225.jpg" alt="Cyanogen 4.2.13 en HTC Magic" width="320" height="480" />

Sobre el rendimiento, ahora puedo marcar una opción llamada "Mantener la página principal en memoria" para evitar lo que me ocurría muchas veces con la 1.6, y es que se quedaba cargando unos segundos cuando salía de alguna aplicación. Además, <strong>Cyanogenmod permite usar la tarjeta SD externa para ampliar la memoria del dispositivo</strong>, de tal forma que cuando se queda corta de memoria usa el espacio en disco para ampliarla.

Personalmente he optado por configurar la opción llamada "Backing Swap", que consiste en que cuando el sistema se ve bajo de memoria primero comprime parte de ella para tener más y cuando aún así necesita más, usa una partición Swap de la tarjeta SD. Para configurarlo, simplemente tuve que crear una partición Swap en la SD (realmente cree también antes una en ext4 por si en un futuro quiero usar la opción de instalar la aplicaciones del sistema ahí en vez de la memoria interna) y seguí las instrucciones del wiki para <a href="http://wiki.cyanogenmod.com/index.php/Compcache#Backing_Swap">configurar el Backing Swap en Cyanogenmod</a>.

En definitiva, si tienes una HTC Magic y estas dudando si conservar la versión 1.6 de Vodafone o instalar otra, <strong>¡instala Cyanogenmod sin dudarlo!</strong>
<strong></strong>

<span style="text-decoration: line-through;"><strong>Actualización: </strong>Hay casos en los que tras instalar Cyanogenmod  el volumen del micrófono está algo más bajo que antes (a mi me ha pasado), la solución está en <a href="http://forum.xda-developers.com/showpost.php?p=4689247&amp;postcount=1">el foro de xda-developers</a>.</span> Parece que con la última versión ya solucionaron esto.<span style="text-decoration: line-through;">
</span>