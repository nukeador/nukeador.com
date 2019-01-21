---
ID: 324
post_title: Privacidad y navegadores (I)
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/16/05/2009/privacidad-y-navegadores-i/
published: true
post_date: 2009-05-16 21:24:10
---
<a href="http://www.flickr.com/photos/bekathwia/2414194397/"><img class="alignright" title="Privacidad" src="http://farm3.static.flickr.com/2106/2414194397_9a484b1d75_m.jpg" alt="" width="240" height="180" /></a>

Muchas veces saltan a la palestra, noticias sobre la privacidad en los navegadores actuales, y más concretamente en Firefox, que la mayoría de las veces son falsas alarmas, desinformación malintencionada o simple paranoia. En el caso que me quiero centrar hoy, se trata de un problema compartido por todos los navegadores y que es generado por el simple hecho de que los enlaces que visitamos se marcan de otro color para que el usuario pueda identificarlos.

Son varios los blogs y sitios de noticias que me he encontrado ya enlazando a la web <a href="http://www.startpanic.com/">startpanic.com</a>, una web que dice detectar los sitios que has visitado. Hasta cierto punto es verdad, con la particularidad que la web tiene que tener a priori una lista de sitios que quiere ver si has visitado o no. En el caso de esta web, tiene una lista de miles de sitios famosos, que posteriormente si ve que cambian de color gracias a la propiedad css :visited (osea, que los has visitado), los analiza en busca de todos los enlaces que tenga y ve si los has visitado también.

<span id="comment-3"><span id="cid-4179542">Este es un proceso lento y costoso para el navegador, por eso notareis que incluso parece colgarle. Esto es algo conocido, hay un bug abierto en Bugzilla (<a title="https://bugzilla.mozilla.org/show_bug.cgi?id=147777" rel="nofollow" href="https://bugzilla.mozilla.org/show_bug.cgi?id=147777">#147777</a>) dónde se explica todo el problema. Pero la solución puede ser fácil:</span></span>
<ol>
	<li><span id="comment-3"><span id="cid-4179542">Desactivar el cambio de color para todos los enlaces visitados.</span></span></li>
	<li><span id="comment-3"><span id="cid-4179542">Desactivar el cambio de color para los enlaces visitados que no pertenezcan a la página que estas visitando actualmente.</span></span></li>
	<li><span id="comment-3"><span id="cid-4179542">Usar el modo de navegación privada que aplica automáticamente el punto 1.</span></span></li>
</ol>
El primer punto se puede hacer accediendo en Firefox desde la barra de dirección a <em>about:config</em>, buscar la clave <span id="comment-3"><span id="cid-4179542"><em>layout.css.visited_links_enabled</em> y fijar su valor a <em>false</em>.</span></span>

<span><span>El segundo punto es inviable actualmente porque la cantidad de recursos que necesitaría para hacer esta comprobación en cada página que visites haría la navegación extremadamente lenta.</span></span>

<span><span>Y el tercer y último punto estará disponible en la próxima versión de <a href="http://www.mozilla.com/es-ES/firefox/all-beta.html">Firefox 3.5</a>.</span></span>

<span><span>En este momento estas son las únicas soluciones que se pueden aplicar para este problema de privacidad y el propio W3C ya avisa en <a href="http://www.w3.org/TR/CSS2/selector.html#link-pseudo-classes">la especificación de la pseudo-clase :visited</a> sobre este problema. La pregunta final es: ¿Deberíamos sacrificar la posibilidad de identificar los enlaces visitados a cambio de solucionar este problema o deberían ser los usuarios preocupados por la privacidad los que aplicaran alguna de las soluciones propuestas?</span></span>

<span><span><a href="http://sharovatov.wordpress.com/2009/04/21/startpaniccom-and-visited-links-privacy-issue/">Información adicional en el blog de Sharovatov</a> (en inglés).
</span></span>