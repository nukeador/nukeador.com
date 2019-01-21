---
ID: 135
post_title: Nuevo monitor y suavizado de fuentes
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/11/09/2007/nuevo-monitor-y-suavizado-de-fuentes/
published: true
post_date: 2007-09-11 18:58:12
---
<p>Hoy mismo ha llegado mi nuevo monitor de 19" panorámico (<a href="http://accessories.euro.dell.com/sna/productdetail.aspx?c=es&l=es&s=dhs&cs=esdhs1&sku=100803">Dell SE198WFP</a>) que por el precio que tiene es muy rentable y una gozada para películas y juegos.</p>
<p><a href="/images/nuevo_monitor.jpg" rel="lightbox"><img class="centered" src="/images/nuevo_monitor_small.jpg" alt="" /></a></p>
<p>Uno de los temas que me ha gustado investigar primero es el tema de el suavizado de tipografías, ya que soy muy maniático a la hora de que los textos se lean perfectamente en pantalla. En el caso de los TFT hay unos paquetes para ubuntu/debian que nos permitirán mejorar notablemente la legibilidad de nuestros textos, ya que usando simplemente la opción "Suavizado de subpíxel" en el panel de Tipografías no me terminaba de convencer</p>
<p>Las instrucciones que doy a continuación las he sacado del <a href="http://ubuntuforums.org/showthread.php?t=343670">foro de Ubuntu</a></p>
<p>Primero tenemos que añadir el repositorio donde se encuentran las librerías actualizadas, lo haremos desde <em>Sistema - Administración - Orígenes del software</em> y añadiremos este:</p>
<p><code>deb http://www.telemail.fi/mlind/ubuntu feisty fonts</code></p>
<p>Aceptamos y recargamos los repositorios cuando nos lo pida. Ahora tendremos que instalar (actualizar) los siguientes paquetes desde synaptic:</p>
<p><code>libfreetype6 libcairo2 libxft2</code></p>
<p>O más rápido:</p>
<p><code>sudo aptitude install libfreetype6 libcairo2 libxft2</code></p>
<p>Reconfiguramos las fuentes:</p>
<p><code>sudo dpkg-reconfigure fontconfig-config</code></p>
<p>(Elegimos Nativo, Siempre, Bitmapped fonts no)</p>
<p><code>sudo dpkg-reconfigure fontconfig</code></p>
<p>Ahora solo queda reiniciar las X (ctrl+alt+backspace) y disfrutar de la mejora de las fuentes</p>