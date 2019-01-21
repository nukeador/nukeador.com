---
ID: 1311
post_title: DRM, Firefox y los usuarios
author: Nukeador
post_excerpt: >
  Firefox implementará un conector para
  que los usuarios que quieran puedan
  activarlo y ver contenido actualmente
  ofrecido con DRM pero sin usar plugins y
  de forma más segura que otros
  navegadores.
layout: post
permalink: >
  https://www.nukeador.com/14/05/2014/drm-firefox-y-los-usuarios/
published: true
post_date: 2014-05-14 22:34:53
---
<em>TL;DR</em>

<em> <a href="https://blog.mozilla.org/press-latam/2014/05/14/drm-y-el-reto-de-servir-a-los-usuarios/">Firefox implementará un conector libre</a> para que los usuarios que quieran puedan activarlo y ver contenido actualmente ofrecido con DRM pero sin usar plugins y de forma más segura que otros navegadores.</em>
<h3>A grandes rasgos</h3>
<ul>
	<li>Los usuarios quieren ver vídeos desde el navegador que actualmente sólo están disponibles con DRM.</li>
	<li>Actualmente se está accediendo a este contenido con plugins como Flash y Silverlight.</li>
	<li>Todos los navegadores menos Firefox han implementado acceso a contenido DRM sin plugins.</li>
	<li>Mozilla se opone al DRM y está trabajando en soluciones alternativas como las marcas de agua (watermarking).</li>
	<li>Se va a desarrollar un conector libre para acceder desde Firefox al módulo de DRM (CDM) qué tendrá que ser descargando de forma independiente.</li>
	<li>No estará activado por defecto.</li>
	<li>Los usuarios tendrán que aceptar su activación, es complemente opcional.</li>
	<li>El código de Firefox seguirá siendo código libre completamente.</li>
	<li>El conector no pasará datos personales, ni identificadores únicos entre sitios, ni acceso al disco o la red al módulo de DRM, al contrario que otros navegadores o los plugins que actualmente estamos usando.</li>
	<li>El objetivo es ofrecer a quien quiera este acceso, que ya se tiene ahora mismo con plugins, usando un estadar nuevo pero de forma que se respete la privacidad de los usuarios.</li>
</ul>
<h3>Qué es DRM y cómo se usa actualmente</h3>
El DRM, o la restricción de derechos digitales, es un sistema para limitar el acceso de los usuarios a contenidos digitales sin consentimiento del autor.

En la esfera web hasta ahora esto se ha estado utilizando sobre todo para el contenido audiovisual (vídeos) por diferentes portales, y ha llegado a los usuarios mediante plugins externos como Adobe Flash o Microsoft Silverlight. Sin estos plugins, es imposible visualizar este tipo de contenido y estos plugins están poco a poco desapareciendo en favor de opciones sólo con tecnologías web.

Desde hace tiempo se propuso la creación de un nuevo estándar web para permitir esto sin el uso de plugins, y la mayoría de navegadores excepto Firefox lo ha implementando de algún modo. Hasta ahora Mozilla no lo había implementado porque cree que el DRM es un error y limita la libertad de los usuarios.

De nuevo nos encontramos con un problema moral: no implementar algo que todos los demás navegadores tienen, forzando así a que los usuarios que no entienden de estos temas migren a otros navegadores que "simplemente funcionan" o implementarlo en contra de lo que creemos que es lo mejor para los usuarios.

De no implementarlo, los usuarios de Firefox tendrían que seguir dependiendo de plugins propietarios externos para ver este contenido, por lo que se ha llegado a la conclusión que hay que implementar una forma para que esto esté disponible sin plugins.
<h3>La solución menos mala</h3>
Se desarrollará un conector libre que comunique Firefox con el módulo DRM de Adobe (CRM), y que este conector (a diferencia de los plugins actuales u otras implementaciones) no pase ningún dato personal al módulo DRM. Ni identificadores únicos entre sitios, ni acceso al disco, ni acceso a la red.

En definitiva, una batalla perdida en la que se ha intentado implementar la solución menos mala para que los usuarios que quieran acceder a este tipo de contenido puedan hacerlo sin plugins y de forma segura. El trabajo ahora es seguir fomentando alternativas al DRM, y educar a los usuarios al respecto.

En Mozilla Hispano: <a href="http://www.mozilla-hispano.org/mozilla-ofrecera-la-opcion-de-reproducir-contenido-con-drm-en-firefox/">Mozilla ofrecerá la opción de reproducir contenido con DRM en Firefox</a>