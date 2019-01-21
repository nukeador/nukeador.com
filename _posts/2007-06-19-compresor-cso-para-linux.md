---
ID: 129
post_title: Compresor CSO para Linux
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/19/06/2007/compresor-cso-para-linux/
published: true
post_date: 2007-06-19 15:59:21
---
<img src="/images/gambas.png" style="float: right" alt="Gambas" />

Hace unos días me animé a probar <a href="http://es.wikipedia.org/wiki/Gambas">Gambas</a> (no, no es que me fuera al bar de la esquina a por una ración, si no el lenguaje de programación :P). Es muy similar a Visual Basic pero para GNU/Linux.

Y haciendo unos ejemplos me lié a crear una interfaz gráfica para el compresor de ISOs para la PSP <a href="http://psp.ducseb.info/4.html">ciso</a>, que aunque ya tenía versión para Linux, solo era mediante terminal.

Lo que hace este programa es <strong>comprimir las ISOs en formato CSO</strong> que ocupa bastante menos en la tarjeta de memoria. Con esta sencilla interfaz será mucho más fácil para la gente que le gustan las aplicaciones gráficas comprimir o descomprimir a CSO sus ISO's para la PSP en GNU/Linux.
<p style="text-align: center"><a href="/images/conv_ciso.jpg" rel="lightbox"><img src="/images/conv_ciso_small.jpg" title="Conversor CISO" alt="Conversor CISO" border="0" height="199" width="200" /></a></p>
Para poder usar el programa tenéis que tener instalado el interprete de gambas2 en vuestro sistema. En la misma carpeta del programa tenéis un instalador para Ubuntu de gambas2, simplemente tenéis que hacer doble clic sobre <em>instalar_gambas2_ubuntu </em>y decirle que lo ejecute en un terminal. Una vez instalado podéis ejecutar el programa desde el ejecutable <em>Conversor_Ciso.</em>
<p class="download"><a href="/archivos/conv_ciso/Conversor_CISO-0.0.1.tar.gz">Descargar Conversor CISO</a></p>
En el tar.gz se incluye: El compresor ciso (<em>ciso</em>), el instalador de gambas2 (<em>instalar_gambas2_ubuntu</em>) para Ubuntu y el programa gráfico Conversor CISO (<em>Conversor_Ciso</em>).

El programa tiene licencia <a href="http://www.es.gnu.org/modules/content/index.php?id=8">GPL</a>, si lo deseas, puedes <a href="/archivos/conv_ciso/Conversor_CISO-src-0.0.1.tar.gz" title="Código fuente - Conversor CISO">descargar su código fuente</a>, donde están los archivo fuente del proyecto en gambas2 y <a href="http://nuovext.pwsp.net/" title="Iconos Nouvext">los iconos</a> usados, así como los binarios.

El <a href="http://ducseb.power-heberg.com/ducsebsoft/telechargement/cso-dax/linux/cso-dax_compressor_0.34_linux.zip">código fuente del compresor ciso</a> está su página oficial.

Esta es la primera versión, por lo que es posible que tenga algún fallo, <strong>agradeceré cualquier mejora o sugerencia</strong>.

<small>PD: Si no usas Ubuntu o Debian, los paquetes que debes instalar para ejecutar esta aplicación son <em>gambas2-runtime</em> y <em>gambas2-gb-gtk</em></small>