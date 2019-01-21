---
ID: 69
post_title: Linux también es bonito
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/18/06/2006/linux-tambien-es-bonito/
published: true
post_date: 2006-06-18 15:32:34
---
Durante mucho tiempo se ha acusado a los entornos de escritorio GNU/Linux de no ser demasiado atractivos visualmente, pero desde hace años <strong>hay mucha gente trabajando en mejorar</strong> esto. Tanto que <strong>actualmente se superan</strong> y con creces las opciones visuales de otros sistemas operativos.

Ayer me animé, tras leer el <a title="Wiki - Ubuntu" href="https://wiki.ubuntu.com/">wiki de Ubuntu</a>, a instalar <a title="Wikipedia - XGL" href="http://es.wikipedia.org/wiki/Xgl">XGL</a> + <a title="Wikipedia - Compiz" href="http://en.wikipedia.org/wiki/Compiz">Compiz [en]</a> ya que me pareció mil veces mas sencillo que hace unos meses. A continuación paso a explicarlo de un modo que todo el mundo lo pueda entender bajo <a title="Wikipedia - Ubuntu" href="http://es.wikipedia.org/wiki/Ubuntu_Linux">Ubutu</a> y <a title="Wikipedia - Gnome" href="http://es.wikipedia.org/wiki/Gnome">Gnome</a> para simplificarlo más (todo se puede hacer mas fácil y rapido con la consola, pero es para quitar miedo a algunos)

<strong>Actualización (22/09/06): </strong>Hay un artículo más actual sobre la instalación de XGL+Compiz. <a title="Estado de Xgl y compiz" href="http://www.nukeador.com/22/09/2006/estado-de-xgl-y-compiz/">¡Consultalo! </a>
<!--more-->

Lo primero que tenemos que haces es <strong>instalar todos los paquetes necesarios</strong>, lo haremos desde el gestor de paquetes (<em>Sistema - Administración - Gestor de paquetes Synaptic</em>) y buscaremos e instalaremos los siguientes paquetes.

Para la aceleración 3d necesaria y xgl:

<em><a title="Descripción del proceso completo" href="https://wiki.ubuntu.com/BinaryDriverHowto/ATI#head-9b196ef5b0179b5fa80bf8bcc77f63def410c367">xorg-driver-fglrx</a></em> (solo para ATI), <em>nvidia-glx</em> (solo para Nvidia), <em>xserver-xgl</em>

Archivos de compiz:

<em> compiz</em>, <em>compiz-gnome</em>

Ahora con todo instalado vamos a crear una nueva opción para que al arrancar el sistema, nos deje elegir en <em>Opciones - Sesiones </em>arrancar en XGL.

Pulsamos <em>Alt+F2</em> para abrir el diálogo de ejecutar aplicación y escribimos: <em>sudo nautilus </em>con la precaución de seleccionar <em>"Ejecutar en una terminal" </em>nos pedirá la contraseña de root y se nos abrirá el adminisitrador de archivos.

Ahora bajaremos este archivo:

<em><a href="http://www.nukeador.com/./archivos/startxglATI.sh">startxglATI.sh</a></em> (solo para ATI) <em><a href="http://www.nukeador.com/./archivos/startxglNV.sh">startxglNV.sh</a></em> (solo para Nvidia)

Lo copiaremos y pegaremos desde el administrador de archivos ya abierto a la carpeta <em>/usr/bin/</em> , una vez pegado pulsaremos con el secundario sobre el archivo <em>Propiedades</em> y en la pestaña <em>Permisos</em> le daremos permiso de ejecución.

Bajaremos este otro archivo:

<em><a href="http://www.nukeador.com/./archivos/xglATI.desktop">xglATI.desktop</a> </em>(solo para ATI)<em> <a href="http://www.nukeador.com/./archivos/xglNV.desktop">xglNV.desktop</a></em> (solo para Nvidia)

Lo copiaremos y pegaremos desde el administrador de archivos ya abierto a la carpeta /usr/share/xsessions/

Una vez hecho esto, reiniciamos las X (<em>Ctrl+alt+tecla de borrar</em>) y en <em>Opciones - Sesiones</em>, seleccionamos XGL, una vez iniciado el entorno en XGL bajamos el archivo:

<em><a href="http://www.nukeador.com/./archivos/compiz.sh">compiz.sh</a></em>

Le copiamos en nuestra carpeta HOME mismamente, le damos permisos de ejecución como antes y nos dirigimos a "<em>Sistema > Preferencias > Sesiones" </em>y en la pestaña <em>Programas al inicio</em> pulsamos <em>Añadir</em> y escribimos <em>/home/tuusuario/compiz.sh</em> (aquí sustituimos "tuusuario" por tu nombre de usuario).

Ahora al reiniciar las X como antes y entrar en la sesión con XGL deberían activarse los efectos.

PD: El efecto transparecia no viene por defecto en los paquetes de Ubuntu, pero podemos bajarle de <a title="Opacity Plugin" href="http://www.downwithnumbers.com/files/compiz_opacity.tar.gz">aquí</a> le descomprimimos y copiamos el archivo <em>libopacity.so</em> a <em>/usr/lib/compiz/</em> (las transparecias se activa con control + may.izq + rueda_ratón)

Tambien podemos añadir un nuevo repositorio en Synaptic (deb http://www.beerorkid.com/compiz dapper main) y bajar el paquete <em>gset-compiz  </em>al que podremos acceder desde <em>Aplicaciones/Accesorios  </em>y que nos permitira configurar hasta el último detalle de los efectos.