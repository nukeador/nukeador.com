---
ID: 158
post_title: Ya llegó el portatil
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/26/01/2008/ya-llego-el-portatil/
published: true
post_date: 2008-01-26 14:03:55
---
<p> Tras una semana de espera, hoy llegó mi <a href="http://www1.euro.dell.com/content/products/productdetails.aspx/inspnnb_1525?c=es&amp;cs=esdhs1&amp;l=es&amp;s=dhs">Dell Inspiron 1525</a> que he comprado gracias al crédito del <a href="http://www.planavanza.es/LineasEstrategicas/AreasDeActuacion/CiudadaniaDigital/EquipamientoConectividad/PrestamoUniverPROY1.htm?rGuid=%7BA7D80B83-1AC8-4774-90F0-A8B5CD3BE758%7D">plan avanza</a>.</p>

<p><a href="/images/inspiron1.jpg" rel="lightbox[insp]"><img src="/images/inspiron1_small.jpg" alt="Inspiron 1525" /></a><a href="/images/inspiron2.jpg" rel="lightbox[insp]"><img src="/images/inspiron2_small.jpg" alt="Inspiron 1525" /></a><a href="/images/inspiron3.jpg" rel="lightbox[insp]"><img src="/images/inspiron3_small.jpg" alt="Inspiron 1525" /></a></p>

<p>Me aseguré bien antes de pedirlo que no tuviera problemas para hacerlo funcionar con mi Ubuntu Linux, ya que al poder personalizarlo le puse una pantalla WXGA+ (1440x900), batería de 9 celdas (unas 5 horas de autonomía) y cambie la tarjeta inalámbrica por una intel que sabía que funcionaría perfectamente.</p>

<p>¿Resultado? Que sin dejar que arrancara <a href="http://badvista.fsf.org/">el sistema operativo que venia preinstalado</a>, metí mi cd de Ubuntu y todo funcionó a la perfección, de momento no he encontrado nada que no funcionara.</p>

<p><strong>Editado:</strong> El micro digital no funcionaba en un principio, pero ya lo hace tras instalar <a href="http://linux.dell.com/files/ubuntu/linux-backports-modules-2.6.22-14-generic_2.6.22-14.50_i386.deb">los modulos que proporciona Dell</a> y seleccionar en el control de volumen, Editar > Preferencias, marcar "Digital input source" y luego seleccionar "Digital Mic 1" en la pestaña Opciones.</p>

<p><strong>Actualización para Ubuntu 8.04:</strong> En esta nueva versión no hay que instalar nada a mayores para que funcione el sonido, por lo que si actualizaste deberás desinstalarlo de la forma que detallan en <a href="http://linux.dell.com/wiki/index.php/Ubuntu_8.04/Issues/No_Sound">el wiki de Dell</a></p>

<p>Una cosa que he descubierto es la utilidad <a href="http://www.ubuntugeek.com/unison-file-synchronization-tool.html">Unison</a> para sincronizar carpetas entre el pc de sobremesa y el portatil. Simplemente hay que instalar los paquetes <a href="apt://ssh">ssh</a> y <a href="apt://unison-gtk">unison-gtk</a> en ambos equipos y podremos desde por ejemplo el sobremesa sincronizar datos con el portatil en ambos sentidos cuando lo necesitemos.</p>

<p>En mi caso el archivo para sincronizar perfiles que se me ha creado es el siguiente:</p>

<p><code># Unison preferences file<br />root = /home/nuke/<br />root = ssh://192.168.1.4//home/nuke/<br />path= .mozilla<br />path= .thunderbird<br />path= .purple<br />path= .liferea_1.4<br />ignore = Name {cache,*~}<br />ignore = Name {Cache,*~}</code></p>

<p>Así puedo tener mis datos siempre conmigo :)</p>