---
ID: 710
post_title: >
  Activar aceleración gráfica en Firefox
  bajo Ubuntu
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/16/05/2011/activar-aceleracion-grafica-en-firefox-bajo-ubuntu/
published: true
post_date: 2011-05-16 12:07:48
---
La última versión de Ubuntu (11.04) instala por defecto una versión de los drivers de Nvidia y ATI que dan algunos problemas para que la aceleración por hardware funcione bien en Firefox 4 y posteriores.

A continuación resumo los pasos para instalar la última versión de los drivers y forzar la aceleración por hardware en Firefox.

<strong>Nota: La versión más actualizada de esta guía estará siempre en <a href="http://www.mozilla-hispano.org/documentacion/Activar_aceleraci%C3%B3n_gr%C3%A1fica_en_Firefox">este artículo del wiki de Mozilla Hispano</a>.</strong>

<h3>Nvidia</h3>
Deinstalamos cualquier versión actual de los drivers:
<code>sudo apt-get purge nvidia*</code>
Editamos el archivo /etc/modprobe.d/blacklist.conf y evitamos que carguen los drivers libres:
<code>gksu gedit /etc/modprobe.d/blacklist.conf</code>
Añadimos al final del archivo y guardamos:
<code>blacklist amd76x_edac
blacklist vga16fb
blacklist nouveau
blacklist rivafb
blacklist nvidiafb
blacklist rivatv</code>

Instalamos los últimos drivers disponibles en el repositorio
<code>sudo apt-get install nvidia-glx-185</code>

Puedes escribir sólo <em>sudo apt-get install nvidia-glx-</em> y dar al tabulador para que liste todos los disponibles e instalar el número más alto que veas.

Si el módulo no se ha cargado automáticamente puedes hacerlo a mano:

<code>sudo modprobe nvidia</code>

Genera el archivo de configuración:

<code>sudo nvidia-xconfig</code>

Reinicia el equipo para comprobar que todo carga correctamente.

Fuente: <a href="http://ubuntuguide.net/install-nvidia-graphical-driver-in-ubuntu-lucid-10-04">Ubuntuguide.net</a>
<h3>ATI</h3>
El proceso tiene algo más de miga, pero es sencillo, podéis leerlo en <a href="http://www.ubuntizandoelplaneta.com/2011/04/nuevos-driver-amd-catalyst-114-y.html">este blog</a>.
<h3>Configuración de Firefox</h3>
Escribe en la barra de direcciones <em>about:config</em> y acepta el mensaje de advertencia. Usando la caja de filtro busca y marca haciendo doble clic como <em>True</em> las siguientes opciones:

<code>webgl.force-enabled</code>

Quizá tengas que forzar a que Firefox no ponga tu driver en la lista negra, simplemente añade la variable a tu sesión (es posible que necesites cerrar y abrir sesión):

<code>echo -e "#Forzar Firefox a usar aceleracion\nMOZ_GLX_IGNORE_BLACKLIST=1" >> ~/.profile</code>

Reinicia Firefox y comprueba accediendo a <em>about:support</em> que en la parte inferior aparece:

<blockquote>Ventanas aceleradas mediante GPU 1/1 OpenGL</blockquote>

Fuente: <a href="https://wiki.mozilla.org/Blocklisting/Blocked_Graphics_Drivers#How_to_force-enable_blocked_graphics_features">Mozilla Wiki</a>