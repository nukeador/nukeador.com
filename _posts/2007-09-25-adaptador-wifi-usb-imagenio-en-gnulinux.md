---
ID: 138
post_title: >
  Adaptador wifi usb (imagenio) en
  GNU/Linux
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/25/09/2007/adaptador-wifi-usb-imagenio-en-gnulinux/
published: true
post_date: 2007-09-25 20:06:31
---
Recientemente he hecho un pequeño script de instalación para el <a href="http://www.telefonicaonline.com/on/io/es/atencion/soporte_tecnico_y_averias/internet/adsl/accesorios/adaptadores_USB_inalambricos/USB_g_Ideal/USB_g_Ideal.htm">adaptador usb inalámbrico</a> que da telefónica con imagenio.

<img class="centered" src="http://www.telefonicaonline.com/on/io/es/atencion/soporte_tecnico_y_averias/internet/adsl/accesorios/adaptadores_USB_inalambricos/USB_g_Ideal/images/AdaptadorUSBIdeal_g.jpg" alt="AdaptadorUSBIdeal" />

En un principio lo he creado para un amigo que no sabe nada de informática y lo necesitaba instalar sin internet, por lo que este script hace lo siguiente:

- Instala ndiswrapper

- Instala el driver mediante ndiswrapper

- Carga el modulo ndiswrapper y lo añade en /etc/modules para que se arranque al inicio del sistema

<span style="text-decoration: line-through;">Lo he probado en Ubuntu 7.04 y funciona correctamente, es posible que funcione para otras versiones.</span>

<span style="text-decoration: line-through;"><strong>Actualización 16/02/2009</strong>: <a href="http://www.nukeador.com/25/09/2007/adaptador-wifi-usb-imagenio-en-gnulinux/#comment-909">Gracias a Daniel</a>, el script está actualizado para Ubuntu 8.10</span>

<span style="text-decoration: line-through;"><strong>Actualización 6/05/2009</strong>: <a href="http://www.nukeador.com/25/09/2007/adaptador-wifi-usb-imagenio-en-gnulinux/#comment-925">Gracias a Daniel</a>, el script está actualizado para Ubuntu 9.04</span>

<strong>Actualización 20/12/2009</strong>: <a href="http://www.nukeador.com/25/09/2007/adaptador-wifi-usb-imagenio-en-gnulinux/#comment-970">Gracias  a Daniel</a>, el script está actualizado para Ubuntu 9.10

Para instalarlo, descomprimimos el archivo en donde queramos y hacemos doble clic sobre "instalar.sh", le indicamos que queremos "Ejecutar en un terminal", ponemos nuestra contraseña de root y ya está, el script hace todo el proceso.
<p class="download"><a title="Instalador Ideal Technology USB Adapter para Ubuntu" href="http://www.nukeador.com/archivos/ideal_tech_ubuntu_driver.tar.bz2">Descargar instalador</a></p>