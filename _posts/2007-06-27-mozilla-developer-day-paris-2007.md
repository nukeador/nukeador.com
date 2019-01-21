---
ID: 130
post_title: Mozilla Developer Day (París 2007)
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/27/06/2007/mozilla-developer-day-paris-2007/
published: true
post_date: 2007-06-27 14:26:24
---
<img src="/images/paris2007.jpg" style="float: right" alt="Paris 2007" />

Este fin de semana he estado en el Mozilla Developer Day de París donde se ha hablado de muchas cosas interesantes sobre desarrollo XUL y sobre el Mozilla Developer Center.

El viernes tuve la oportunidad de visitar un poco la ciudad con Henrik Skupin (whimboo del equipo alemán) y con Adrian (equipo polaco) durante toda la tarde, nos tuvimos que dar prisa para visitar en 5 horas todo lo que queríamos ver, pero el metro nos ayudó bastante. Primero visitamos la oficina de Mozilla Europe y luego ya comenzamos nuestro tour por París: Notre Dame, Torre Eiffel, Arco del Triunfo, Plaza de la Concordia y finalmente las afueras del Museo del Louvre.

El mismo viernes por la noche asistimos a la cena con la gente de Mozilla en el restaurante Dalva donde pudimos seguir conversando entre los colaboradores.

Las conferencias el sábado en el Club Confair comenzaron a las 10y allí pude hablar con mucha gente interesante como Eric Shepherd (líder del <a href="http://developer.mozilla.org/" title="Mozilla Developer Center">MDC</a>), Tristan Nitot (presidente de <a href="http://www.mozilla-europe.org/" title="Mozilla Europe">Mozilla Europe</a>), y demás colaboradores y desarrolladores de distintos países.

El sábado por la noche cenamos en un restaurante español llamado "La Bodega" donde había espectáculo musical y discoteca donde lo pasamos genial.
<p class="info">Podéis ver <a href="http://www.flickr.com/photos/nukeador/sets/72157600467251591/" title="París 2007">mis fotos en flickr</a> del fin de semana y también <a href="http://www.flickr.com/photos/tags/mozdevdayparis07/" title="Mozilla Developer Day París 2007">todas las fotos del evento</a> que han ido subiendo tanto a flickr como <a href="http://picasaweb.google.com/benoit.leseul/MozillaDevDayParis/" title="Fotos de Benoit en picasa">a picasa</a>.</p>
A continuación intentaré hacer un resumen sobre todo lo que se trató en las charlas del sábado.

<!--more-->

<a href="http://en.wikipedia.org/wiki/Mike_Shaver" title="Mike Shaver en Wikipedia">Mike Shaver</a> llevó la organización de todas las charlas dando paso a todos los participantes y dió la charla de bienvenida así como la mesa redonda para ver que queríamos tratar y cuando.

<a href="http://www.flickr.com/photos/nukeador/613804536/" title="Mike Shaver"><img src="/images/parisdevday07_1.jpg" style="float: right" alt="Mike Shaver" /></a>

La primer charla fue a cargo de Neil Deakin quien habló sobre el desarrollo de la nueva versión de XUL (1.9) y sobre el futuro de la misma, nuevos widgets, menús... etc. Podéis leer un pequeño resumen en la primera parte de <a href="http://docs.google.com/View?docid=dtmwnwg_2p6bgpw" title="Developer Day Summary">este documento</a>.

Posteriormente se habló sobre las herramientas para los desarrolladores de XUL, ya que hay diferentes públicos se necesitan herramientas que hagan fácil el desarrollo. Por ejemplo desde <a href="http://www.mozpad.org/" title="Mozpad.org">mozpad.org</a> están desarrollando un IDE para XUL. Se apuntó que debería tenerse en cuenta que se pueda especificar en las aplicaciones que cadenas pueden ser traducidas. Se resaltó la importancia de tener una buena documentación en el <a href="http://developer.mozilla.org/es/" title="Mozilla Developer Center">MDC</a>.

Después de la comida varias personas mostraron sus aplicaciones en XUL, entre ellas:
<ul>
	<li>Paul Rouget: <a href="http://blog.mozbox.org/tag/codeeditor" class="external text" title="http://blog.mozbox.org/tag/codeeditor" rel="nofollow">Codeeditor</a> un IDE para XUL basado en scintilla (coloración sintáctica, code folding, autocompletado...)</li>
	<li>Nicolas Froidure: <a href="http://bbcomposer.elitwork.com/" class="external text" title="http://bbcomposer.elitwork.com" rel="nofollow">BBComposer</a> una extensión para editar cualquier cuadro de texto con XHTML, BBCode o Mediawiki.</li>
	<li>John Resig (creador de <a href="http://jquery.com/" title="JQuery">JQuery</a>): <a href="http://ejohn.org/blog/fuel-02-progress/" title="FUEL">FUEL</a>, la API en javascript que facilitará mucho las cosas a los desarrolladores de extensiones a la hora de acceder al toolkit y a la aplicación simplificando el uso de XUL DOM y eventos dentro del chrome.
Por ejemplo para añadir un nuevo marcador ahora es tan sencillo como:Application.bookmarks.add("Mozilla", <a href="http://mozilla.org/" class="moz-txt-link-rfc2396E">"http://mozilla.org/"</a>);
FUEL 0.2 esta disponible ya en el trunk de Firefox 3.0a4.</li>
	<li>David Teller: <a href="http://www.openberg.org/" class="external text" title="http://www.openberg.org" rel="nofollow">OpenBerg Lector</a>, un lector de e-books con muchas opciones, como marca páginas, notas y organizador de libros.</li>
	<li>Jan Odvarko: <a href="http://www.allpeers.com/" class="external text" title="http://www.allpeers.com" rel="nofollow">AllPeers</a>, la extensión para Firefox que permite compartir ficheros con tus contactos</li>
	<li>Allan Beaufour: <a href="http://www.joost.com/" class="external text" title="http://www.joost.com" rel="nofollow">Joost</a>, televisión gratuita a la carta usando la plataforma Mozilla. (Pude hablar con una persona de Joost que me aseguró que la versión para GNU/Linux se publicará pronto, ya que él había probado la versión en desarrollo y funcionaba muy bien :D)</li>
	<li> Daniel Glazman: El creador de <a href="http://www.nvu.com/" title="NVU">NVU</a> presentó <a href="https://addons.mozilla.org/fr/firefox/addon/4650" class="external text" title="https://addons.mozilla.org/fr/firefox/addon/4650" rel="nofollow">FullerScreen</a>, una extensión que permite una verdadera pantalla completa en Firefox y además permite visualizar pases de diapositivas partiendo de un documento HTML estándar.</li>
	<li>Ben Bucksch: <a href="http://www.tomtom.com/home/" class="external text" title="http://www.tomtom.com/home/" rel="nofollow">TomTom</a>, la aplicación para administrar tus dispositivos GPS TomTom ahora está basado en XUL.</li>
</ul>
<a id="mdc"></a>La siguiente charla fue sobre el <a href="http://developer.mozilla.org/es/" title="Mozilla Developer Center">Mozilla Developer Center</a> y su traducción. <a href="http://www.bitstampede.com/">Eric Shepherd</a> centró la charla en forma de mesa redonda donde los colaboradores pudimos exponer nuestros problemas, ideas y compartir con el resto la forma que nuestro equipo trabajaba:

<a href="http://www.flickr.com/photos/nukeador/613825058/" title="Eric Shepherd"><img src="/images/parisdevday07_2.jpg" style="float: right" alt="Eric Shepherd" /></a>
<ul>
	<li>13 traducciones</li>
	<li>Nuevo breadcrumbs, nueva versión de MediaWiki</li>
	<li>Se está trabajando en un sistema de búsqueda nuevo</li>
	<li>Meta: aumentar la audiencia</li>
	<li> Retos: falta de gente, tasa de abandonos por cansancio (siempre hay algo para traducir en el MDC y es difícil llegar a sincronizar con el wiki inglés)</li>
	<li>Problema: sincronización entre la versión inglesa y las localizadas</li>
	<li>Idea: Mostrar una nota si la versión inglesa si es más actual que la traducida</li>
	<li>Aplicar las mejoras en las traducciones en el artículo original</li>
	<li>Problema: Asegurar la calidad de la documentación</li>
	<li>Jornadas MDC (fines de semana trabajando para la comunidad)</li>
	<li>El equipo francés tiene una lista con los artículos más importantes basándose en la lista de artículos más visitados en el wiki inglés.</li>
	<li>Crear artículos destacados, mostrar cuanta gente colabora...</li>
	<li> gerv: Ranking entre wikis basado en las traducciones de las páginas más visitadas</li>
	<li>Por mi parte apunté que para que el bot japones y la nueva plantilla que avisa que la traducción esta obsoleta funcionen, todas las páginas deben tener los enlaces interwiki apuntando a los otros wikis.</li>
	<li>Colaborar con las universidades que enseñen idiomas (créditos por las traducciones) - pero: es necesario verificar el trabajo para dar los créditos.</li>
	<li> ¿Cómo animar a la creación?</li>
	<li> Hay usuarios que no saben que pueden editar y quieren agradecérnoslo</li>
	<li>Roles de la Wikipedia: "policía", "bibliotecarios"... etc.</li>
	<li>No podemos forzar a los usuarios a traducir algo, pero se les pueden proponer temas.</li>
	<li>Los problemas de sincronización pueden causar abandonos por cansancio.</li>
	<li> Se deberían bloquear las páginas originales durante la traducción.</li>
	<li>Número de visitas + última edición = informar a los usuarios si es un buen momento para comenzar un traducción (si no ha cambiado en mucho tiempo: sí)</li>
	<li> Comparar los cambios en los párrafos del wiki inglés para intentar ver los cambios en los artículos traducidos.</li>
	<li>¿Qué hacer con los artículos con licencias que no permiten su modificación? Elaborar una lista con ellos para que se pongan en contacto con el autor.</li>
	<li>Colaborar entre traductores de diversos países compartiendo ideas. Yo ya <a href="http://groups.google.com/group/mozilla.dev.mdc/browse_thread/thread/35ca6d9c85df67d3/486000a2d4e78cd6#486000a2d4e78cd6" title="Spanish Team Summary">he enviado mis impresiones</a> a la lista de correo del MDC.</li>
</ul>
Si queréis colaborar con el MDC, podéis suscribiros a <a href="https://lists.mozilla.org/listinfo/dev-mdc-es" title="MDC-ES List">la lista del MDC en español</a> y leer los <a href="http://developer.mozilla.org/es/docs/MDC:Primeros_Pasos" title="MDC: Primeros Pasos">primeros pasos</a> en el wiki.

Y eso fue todo. Un fin de semana muy interesante donde he aprendido un montón de cosas y que me ha animado más a seguir colaborando con Mozilla.