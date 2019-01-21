---
ID: 1676
post_title: '¿Se puede vivir en Internet usando únicamente la red Tor? #torweek'
author: Nukeador
post_excerpt: 'La semana pasada me propuse una pregunta y un reto: ¿Se puede vivir usando la red Tor para todas tus conexiones (pc y móvil)?'
layout: post
permalink: >
  https://www.nukeador.com/10/10/2016/se-puede-vivir-en-internet-usando-unicamente-la-red-tor-torweek/
published: true
post_date: 2016-10-10 12:02:37
---
La semana pasada me propuse una pregunta y un reto:

https://twitter.com/nukeador/status/783043278979600384

El objetivo era pasar una semana donde todo mi tráfico a Internet tuviera que pasar por <a href="https://es.wikipedia.org/wiki/Tor_(red_de_anonimato)">la red Tor</a>.

<strong>Actualización (17/2/17):</strong> El experimento pasó de una semana, a un mes, y ya van 4 meses así.
<h3>Pero, ¿qué es Tor?</h3>
Tor o "The Onion Router" es una red de comunicaciones distribuida en la que el tráfico de sus usuarios no revela su identidad (dirección IP) y en la que el tráfico viaja cifrado por todo el circuito.

<strong>¿Cómo lo hace?</strong>

<a href="/wp-content/uploads/2016/10/Funcionamiento_red_tor2.svg_.png"><img class="aligncenter wp-image-1678 size-large" src="/wp-content/uploads/2016/10/Funcionamiento_red_tor2.svg_-1024x408.png" alt="funcionamiento_red_tor2-svg" width="962" height="383" /></a>

El resumen sería: Tu tráfico viaja a través de al menos 3 nodos (entrada, middle, salida) de forma cifrada al menos hasta el nodo de salida, por lo que no te conectas directamente a los sitios sino pasando a través de la red Tor primero.
<h3>¿Por qué es importante?</h3>
Cuando nos conectamos a cualquier servicio en la red, <strong>nuestro tráfico pasa por varios sitios</strong>, entre ellos nuestro operador de Internet, repetidores intermedios y el servidor de destino. Esto conlleva algunos <strong>peligros con nuestra privacidad</strong> no evidentes para la mayoría de la gente:
<ul>
 	<li><strong>Nuestro operador de Internet</strong> puede saber en todo momento a dónde, cuándo y cuánto tiempo nos conectamos (aunque no vea el qué hacemos si la conexión está cifrada - https). No hace falta saber el qué cuando nos conectamos a sitios cuya temática es única (viajes, médicos, aficiones, tendencias políticas...).</li>
 	<li>Nuestro operador sabe quienes somos (nombre, apellidos).</li>
 	<li>Los <strong><a href="https://es.wikipedia.org/wiki/Cable_submarino">repetidores</a> intermedios</strong> pueden (y muchos están) intervenidos por <strong>agencias de espionaje</strong> de muchos países, permitiéndoles ver que alguien con tu ip (identificador único) se conectó a cierto servidor durante X tiempo.</li>
 	<li>Cualquier conexión no segura (http normal) puede ser vista por estos dos primeros agentes, todo lo que transmites a través de ella e incluso modificarnos el contenido sin nosotros saberlo.</li>
 	<li><strong>Los servicios y webs</strong> pueden saber perfectamente el origen de la visita (país, ciudad, operador), y hacerte seguimiento en otras webs que visites que ellos controlen o tengan el mismo sistema de publicidad.</li>
</ul>
Adicionalmente, gracias a diversas técnicas (la mayoría de veces a publicidad compartida y cookies), los servicios web pueden hacerte fingerprinting, esto es, crear una huella única sobre ti que contiene tu ip, otros sitios que has visitado, cookies, resolución de pantalla... y aunque no sepan a quien pertenece esa ip, pueden saber que es la misma persona.

Hay servicios donde damos nuestro nombre real (redes sociales, servicios de correo...) con lo que también pueden identificar esa huella con una persona. Adicionalmente también hay sitios donde damos nuestro teléfono, y esto también abre la puerta a saber muchas cosas más de ti.

Ejemplo: <strong>Si tienes una cuenta de Gmail abierta, Google puede saber tu nombre, teléfono y las web que visitas</strong> que tienen publicidad de empresas que controla google (casi la mayoría). Facebook puede hacer lo mismo con todas las webs que tengan un botón de "Me gusta".

De todo esto hablé en mi charla <a href="https://www.nukeador.com/20/05/2016/el-usuario-al-mando-mozilla-y-la-privacidad-en-la-red/">El usuario al mando y la privacidad en la red</a>. También recomiendo el documental <a href="https://www.youtube.com/watch?v=dFF9sZapRFM">Annonymous: Inside the Dark Web</a>.

<img class="aligncenter size-full wp-image-1687" src="/wp-content/uploads/2016/10/activate.png" alt="activate" width="400" height="370" />
<p style="text-align: center;"><em>¿Te sientes algo incomodo ya con tantos ojos pudiendo ver lo que haces en la red?</em></p>

<h3>¿Cómo protegerse? La #TorWeek</h3>
<img class="aligncenter wp-image-1686 size-medium" src="/wp-content/uploads/2016/10/Tor-logo-2011-flat.svg_-300x181.png" alt="tor-logo-2011-flat-svg" width="300" height="181" />

Por ello esta semana me propuse que todas mis conexiones pasaran a través de la red Tor y analizar si era posible trabajar en el día a día con este uso. Además de usar la red Tor, hay otras medidas importantes para evitar el rastreo de todos estos ojos curiosos.

<strong>Uso de Tor</strong>

La forma más sencilla para usar la red Tor es <strong>usar <a href="https://www.torproject.org/projects/torbrowser.html.en">Tor Browser</a></strong>, ya que automáticamente pasará todas nuestras conexiones por esta red. Para las conexiones del móvil, instalando <strong>la aplicación <a href="https://www.torproject.org/docs/android.html.en">Orbot</a></strong> y usando su opción VPN.

Si quieres un sistema completo, puedes instalar el <a href="http://tails.boum.org/">sistema operativo Tails</a> en un usb y arrancar el ordenador con él.

Pero como yo quería usar mi navegador, cliente de correo y otras aplicaciones tal cual las tenía configuradas tuve que hacer varios ajustes. Si no usas Linux o no tienes conocimientos técnicos, <strong>estas tres opciones anteriores son las que debes usar</strong>. Al final de este artículo explico mi configuración concreta.
<h3>Conclusiones</h3>
Aunque en principio pensé que la <strong>velocidad</strong> de la red no iba a ser suficiente para realizar todas mis tareas con normalidad, la verdad es que he quedado gratamente sorprendido.

https://twitter.com/nukeador/status/783763747152224256

https://twitter.com/nukeador/status/783766071530708994

He podido <strong>usar Internet tanto para trabajo como para ocio sin ningún tipo de problema</strong> mayor, si bien es cierto que:
<ul>
 	<li>Hay veces que Tor te asina un nodo muy lento y tienes que darle renovar.</li>
 	<li>Varias webs que usar Cloudfare te piden completar un captcha antes de entrar por si eres un bot.</li>
</ul>
Hay dos excepciones para las cuales no he usado Tor:
<ul>
 	<li>Streaming de vídeo y música (Netflix y Spotify), aunque sí lo he usado para youtube y otras webs de vídeo.</li>
 	<li>Uso de bittorrent: Desaconsejado por la propia gente de Tor ya que los clientes acaban revelando tu ip real y congestionas mucho la red. Si quieres privacidad aquí, usa una VPN.</li>
</ul>
Cosas a tener siempre en cuenta:
<ul>
 	<li>Usa el sentido común, <strong>no hagas cosas ilegales</strong>.</li>
 	<li>Los sitios <strong>donde inicies sesión sabrán quién eres</strong>, pero no desde donde te conectas.</li>
 	<li><strong>No abras documentos que te bajes directamente</strong>, ya que pueden contener imágenes remotas que detectarán tu ip real.</li>
 	<li><strong>No te conectes a un servicio sin Tor y con Tor a la vez</strong>, ya que es fácil relacionar quien es quien.</li>
 	<li>En páginas que <strong>no usen https, nunca introduzcas datos</strong>. Esto podrían ser vistos por el nodo de salida y todo el camino desde este a la web destino. Recomendación idéntica si no usas Tor.</li>
</ul>
Dado que quería una configuración más general para todas mis app, tuve que instalar algunas cosas adicionales que ahora detallo.
<h3>Configurando el sistema para usar siempre Tor (avanzado)<strong>
</strong></h3>
<em>A continuación viene una explicación más técnica de como configuré mi sistema, posiblemente no apta para público no técnico.</em>

Probé varias opciones más o menos complejas, una de ellas fue configurar el proxy del sistema para que todo saliera por el puerto de tor, lo cual terminé descartando por posibles problemas de privacidad.

Es importante recalcar que <strong>si quieres usar Tor sin usar Tor Browser o Tails, tendrás que tener mucho cuidado</strong> en cómo configuras tu sistema para evitar que tu identidad sea revelada por otros factores:
<ul>
 	<li><strong>DNS Leaks</strong>: De nada sirve conectaros a Tor si cuando pedimos una web las peticiones DNS (lo que traduce que unaweb.com es la IP 5.5.5.5) pasar a nuestro operador de Internet.</li>
 	<li><strong>Cookies, trackers y fingerprint</strong>: De nada sirve tampoco que nuestro navegador esté configurado de forma que los sitios puedan escribir cookies, cargar anuncios que nos siguen por varias web creando una huella única.</li>
 	<li><strong>Inicios de sesión</strong>: Se consciente que si inicias sesión en tu correo o en cualquier web, esta web va a saber que has estado usando el nodo de salida Tor con cierta IP en un momento concreto. Aunque tor rota los circuitos cada 10 minutos por defecto (Tor Browser lo hace por cada dominio) es algo que tienes que tener en cuenta.</li>
</ul>
Mi configuración final fue la siguiente: <strong>Instalación de tor, abrir todas las aplicaciones con proxychains</strong> e instalar varios complementos de privacidad en el navegador.

Instalar tor y proxy chains (Linux):

<code>sudo aptitude install tor proxychains</code>

<strong>Complementos a instalar en el navegador</strong>
<ul>
 	<li><a href="https://addons.mozilla.org/es/firefox/addon/https-everywhere/?src=ss">Https Everywhere</a>: Fuerza la versión https de la mayoría de páginas conocidas. Nota: Nunca usar una web sin https para transmitir datos.</li>
 	<li><a href="https://addons.mozilla.org/es/firefox/addon/self-destructing-cookies/?src=api">Self Destructing Cookies</a>: Borra las cookies de todas las páginas una vez que salimos, para evitar que almacenen datos sobre nosotros y se puedan leer cuando regresemos.</li>
 	<li><a href="https://addons.mozilla.org/es/firefox/addon/ublock-origin/?src=search">Ublock Origin</a>: Bloqueo de publicidad y listas de rastreo.</li>
</ul>
<strong>Actualización (17/2/17):</strong> Un par de complementos más para evitar que nos rastreen por usar el mismo User Agent o tomen datos usando &lt;canvas&gt;
<ul>
 	<li><a href="https://addons.mozilla.org/es/firefox/addon/random-agent-spoofer/">Random Agent Spoofer</a>: Nos asigna un user agent aleatorio cada X tiempo.</li>
 	<li><a href="https://addons.mozilla.org/es/firefox/addon/canvasblocker/">CanvasBlocker</a>: Evita que las webs usen &lt;canvas&gt; sin pedir permiso, ya que se ha demostrado que es posible identificar de forma única a un equipo con esto.</li>
</ul>
Configuraciones adicionales en <code>about:config</code>

<code>privacy.trackingprotection.enabled</code> a <code>true</code>: Activar la protección anti-rastreo de Firefox, evitamos que carguen <a href="https://www.mozilla.org/es-ES/teach/smarton/tracking/">elementos que nos siguen en la red</a>.

<code>network.proxy.socks_remote_dns</code> a <code>true</code>: Nos aseguramos que todas las peticiones dns pasan a través del proxy configurado.

Extra: Desactivar todos los plugins como Flash, Java... etc

<strong>¿Cómo es el uso normal?</strong>

Una vez configurado todo lo anterior, simplemente tenemos que abrir las aplicaciones de esta forma:

<code>proxychains firefox</code>

Por defecto proxychains está configurado para pasar todas las conexiones de la aplicación a través del proxy local de tor (incluidas peticiones DNS). Podemos usarlo para cualquier aplicación que usemos (excepto bittorrent u otras aplicaciones p2p).
<h3>Ayudar al proyecto Tor</h3>
Lo mejor para ayudar la red y el proyecto Tor es <a href="https://www.torproject.org/docs/tor-doc-relay.html.en">levantar un relay</a> (sobre todo de salida) que hará que la velocidad de la red mejore para todos sus usuarios, ya sea en un servidor tuyo o convencer a alguna organización para que lo haga. Si tienes aún preocupaciones sobre esto, te dejo dos enlaces interesantes para aclarar mitos:
<ul>
 	<li><a href="https://blog.daknob.net/running-a-tor-exit-node-for-fun-and-e-mails/">Running a Tor Exit Node for fun and e-mails</a></li>
 	<li><a href="https://boingboing.net/2015/08/04/what-happened-when-the-fbi-sub.htmlhttps://boingboing.net/2015/08/04/what-happened-when-the-fbi-sub.html">What happened when we got subpoenaed over our Tor exit node</a></li>
</ul>
Es triste ver que en España <a href="https://torstatus.blutmagie.de/network_detail.php">sólo hay 7 nodos de salida</a>, comparado con los 75 de Alemania, 85 de Francia o 125 de Holanda y 147 de EEUU.

Cuantos más nodos haya y cuanto más use la gente la red Tor para su navegación habitual, más fácil será asegurar la privacidad de nuestras conexiones en la red.