---
ID: 110
post_title: ¿Telefonica censura internet?
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/27/03/2007/telefonica-censura-internet/
published: true
post_date: 2007-03-27 11:48:59
---
<p>Me ha llegado hace poco un correo comentado que <strong>Telefónica está capando la entrada a webs de P2P</strong> como las siguientes:</p>
<p><code><br />
http://www.gamestorrents.com<br />
http://www.btparadise.com/torrents.php<br />
http://www.newpct.com<br />
http://www.todocvcd.com/<br />
http://www.divxtotal.com<br />
http://www.estrenosdtl.com<br />
http://www.emwreloaded.com/main.php<br />
http://xbtt.animersion.net/index.php</code></p>
<p>Si tenéis telefónica (terra aun no las capa) podréis comprobar que no os entra, pero con otra compañía si.</p>
<p><strong>¿Solución?</strong></p>
<p>De momento cambiar las DNS por <a href="http://www.bandaancha.st/toolsdns.php">otras</a> o usar las de <a href="http://www.opendns.com/start/">OpenDNS</a>:</p>
<p><code>208.67.222.222<br />
208.67.220.220</code></p>
<p>En windows lo podeís hacer en <em>Inicio - Configuración - Panel de control - Conexiones de red</em>. Clic derecho en la conexión, propiedades, tcp ip, propiedades, asignar las 2 dns. </p>
<p>En linux podéis cambiarlas desde el Network Manager, a mano o en Ubuntu, <em>Sistema - Administración - Red</em>, <em>Nombres de dominio (DNS)</em></p>
<p>Tenéis más información y quejas en <a href="http://foros.internautas.org/viewtopic.php?t=7574">el foro de internautas.org</a>.</p>
<p>Yo personalmente voy a llamar al 1004 para dejarles las cosas claras y enviaré un par de correos para informar a los conocidos.</p>
<p><!--more--></p>
<p><strong><br />
Actualización: </strong></p>
<p>Acabo de llamar y me mandan al 902 (de pago) por lo que he encontrado <a href="http://wiki.nomasnumeros900.com/Acceso_a_Internet/ADSL/Televisi%C3%B3n#Telef.C3.B3nica">un wiki</a> que te da los números locales a los que corresponde (91 707 74 60), como tengo las llamadas a fijos nacionales gratis, mejor que 6 cent. el minuto sí que es. </p>
<p>Allí me dicen que darán parte, incluso me dicen que si estaría dispuesto a que me cobren si el problema es mio... tras quedar en que me llamarán, he perdido conexión durante un rato (supongo que estaban haciendo pruebas con mi línea, pero vete a saber).</p>
<p>Veremos en que queda la cosa.</p>
<div class="info"><strong>Más soluciones</strong>
<p>Otra solución es (aparte de usar las DNS de OpenDNS) montarte un cache de DNS, para que tu propio pc recuerde que nombre corresponde a que ip sin tener que andar consultando al DNS. </p>
<p>Para ello he instalado el paquete dnsmasq y como DNS primario he puesto mi maquina local (127.0.0.1) y luego los 2 de OpenDNS. Como instalarlo para sistemas basados en Debian lo tenéis en <a href="http://www.guia-ubuntu.org/index.php?title=Servidor_DNS-Cache">un artículo de la guia-ubuntu</a>. Este procedimiento es interesante tanto para si el servidor DNS falla, como para mejorar la velocidad.</p></div>
<p><strong>Actualización (27/03/07 19:18)</strong></p>
<p>Desde <a href="http://www.theefrit.com/blog/2007/03/27/cuando-se-caen-los-dns-telefonica-censura/">theefrit.com</a> dan una posible explicación al problema con las DNS, parece ser que todos los dominios pertenecen a <a href="http://www.enom.com/registrynews.asp">eNom INC</a>, y los DNS de telefónica están sincronizando mal con ellos.</p>
<p>Podéis comprobarlo con el resto de dominios de la siguiente forma:</p>
<p><code>whois newpct.com | grep 'Whois Server'<br />
Whois Server Version 2.0<br />
Whois Server: whois.enom.com</code></p>
<p>En el caso de mocosoft,com me devuelve directnic en vez de eNom, más aún, este dominio, nukeador.com me devuelve eNom y con las DNS de telefónica se entra perfectamente.</p>
<p>No se como funcionan las sincronizaciones de DNS exactamente, pero ¿es posible que a unos de eNom si y a otro no?</p>
<p><strong>Actualización (27/03/2007 22:07)</strong></p>
<p>Aunque parece que los servidores DNS de telefónica ya resuelven los dominios anteriormente comentados, TheEfrit nos vuelve a dar <a href="http://www.theefrit.com/blog/2007/03/27/cuando-se-caen-los-dns-telefonica-censura/#comment-1649">una explicación técnica de lo que sucedía</a>. Desgraciadamente no podremos saber a ciencia cierta si era un error o intencionado, ¿confiamos en la buena voluntad de las ISP?</p>
<p>Yo de momento me quedaré con las DNS de OpenDNS y mi DNS Cache local.</p>