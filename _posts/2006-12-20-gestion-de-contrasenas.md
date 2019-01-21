---
ID: 91
post_title: Gestión de contraseñas
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/20/12/2006/gestion-de-contrasenas/
published: true
post_date: 2006-12-20 21:00:52
---
Hace poco saltó la alarma cuando en muchos sitios se hablaba sobre el "<a title="Kriptopolis - Robo de contraseñas en Firefox" href="http://www.kriptopolis.org/robo-de-contrasenas-en-firefox">Robo de contraseñas en Firefox</a>"

Otros sitios leyeron la noticia y dieron una interpretación distinta, y como bien sabemos, la información se degrada poco a poco, por lo que no quiero ni saber que puede haber llegado a entender un usuario común.

Actualmente y tras la salida de <a title="Bugs arreglados en Firefox 2.0.0.1" href="http://www.mozilla.org/projects/security/known-vulnerabilities.html#firefox2.0.0.1">Firefox 2.0.0.1</a> mucho han vuelto a retomar el tema al no verlo arreglado, este hecho me hizo sentir curiosidad sobre el alcance real del bug y porqué aun estaba sin resolver, por lo que me dirigí a <a title="Cross-Site Forms + Password Manager = Security Failure" href="https://bugzilla.mozilla.org/show_bug.cgi?id=360493">Bugzilla</a> para leerlo.

Bien, voy a intentar hacer un resumen de todo lo que allí se comenta hasta ahora (que es bastante), además de <a title="Recuerda una contraseña y usa cientos" href="http://www.nukeador.com/20/12/2006/gestion-de-contrasenas/#pwdhash">una recomendación</a> al final para poder tener una contraseña en cada sitio y solo recordar una.

<!--more-->

Pongamos que entramos a la página <em>http://www.pagina1.com, </em>en ella tenemos un nombre de usuario y contraseña y le decimos a Firefox que los recuerde y así siempre que entremos nos lo rellene sin tener que memorizarlos.

Pues bien, el bug solo puede darse en una situación muy específica:
<ul>
	<li>Entramos normalmente a <em>http://www.pagina1.com</em></li>
	<li>La página ha sido modificada para que un formulario oculto nos pida nombre de usuario y contraseña y este los mande a <em>http://www.pagina2.com</em></li>
	<li>Como anteriormente dijimos a Firefox que guardara estos datos y al ver que el formulario está en <em>http://www.pagina1.com </em>(donde lo habíamos guardado), Firefox rellena los datos y permite enviarlos.</li>
</ul>
De esta forma nuestros datos (solo los guardados para esa página, no es resto) serían trasmitidos a otra página automáticamente y sin nuestro consentimiento.

Pero, un momento, <strong>¿otra web puede robarme mis contraseñas de <em>http://www.pagina1.com</em>?</strong>

No, ya que el formulario oculto debe estar situado en <em>http://www.pagina1.com</em> y Firefox solo rellenará los datos para ese dominio que es donde lo guardamos y solo con los datos de <em>http://www.pagina1.com</em> no de otra página.

<strong>¿Cómo modifican <em>http://www.pagina1.com</em> para que exista un formulario oculto? </strong>

Evidentemente no lo va ha hacer el autor, ya que es estúpido que intente robarte contraseñas que usas en su sitio de esta forma si lo puede hacer mirando la base de datos de usuarios guardando las contraseñas sin encriptar.

En este caso solo podría hacerse en sitios como foros y comentarios, donde un usuario externo pueda insertar código html para introducir el formulario oculto. Pero, <strong>¡ojo!</strong>, la mayoría de webs seguras no permiten que un usuario normal introduzca html en comentarios ya que podría comprometer la seguridad de la web totalmente, no solo esto.

<strong>¿Y si hacemos que Firefox compruebe si el formulario se envía a una web externa?</strong>

Pues conseguiríamos que todas las webs que tiene un servidor diferente para el inicio de sesión y otro para almacenar los datos no funcionaran con el gestor de contraseñas.

<em>Ej: http://pages.google.com/ para iniciar sesión y http://usuario.googlepages.com/ para mostrar las páginas</em>

<strong>¿Qué ocurre si <em>http://www.pagina1.com</em> es una web que sirve webs a usuarios del tipo <em>http://www.pagina1.com/usuario/ </em>?</strong>

Bien, en este caso podría explotarse el bug desde una página de usuario y conseguir la contraseña del dominio padre <em>http://www.pagina1.com</em>, lo que nos lleva a la siguiente pregunta:

<strong>¿Y si Firefox comprobara la URL exacta desde donde se guardó para evitar el problema anterior? </strong>

Pues de nuevo encontraríamos problemas en las páginas como muchos wikis que tras intentar editar uan web que requiere registro te redirigen para que lo hagas a (por ejemplo)

<em> http://en.wikipedia.org/w/index.php?title=Special:Userlogin&returnto=Main_Page</em>

Por lo que si guardaramos los datos para esta url completa, en el resto de página o en la portada no funcionarían y tendríamos que guardarlo para cada url completa y si cambiamos de contraseña imaginad que lío...

<strong>¡Dios mio! Entonces es peor el remedio que la enfermedad, ¿qué nos queda por hacer?</strong>

Bien, como este problema solo puede explotarse insertando un formulario en la propia web (o como hemos visto desde un subdominio), los administradores de dichas páginas deberían evitar que sus usuarios puedan insertar html simulando formularios en comentarios.

Las páginas que tienen alojadas webs de usuarios deberían filtrar el uso de inputs del tipo type="password"

<strong>Conclusión: </strong>

Personalmente pienso que TODOS los programas gestores de contraseñas son inseguros por diseño, y como no se va a eliminar el gestor de contraseñas en Firefox (ya que es algo muy demandado) ni en ningún otro navegador, el problema recae en que desde las páginas web se evite que terceras personas les inserten formularios con envío de contraseñas.

<a id="pwdhash"> </a><strong>¿Como evitar que el robo de una contraseña comprometa otras webs con la misma contraseña?</strong>

La respuesta simple es, usa una contraseña distinta para cada web, así si una se ve comprometida no el resto.

Esto es inviable cuando se está registrado en muchas páginas, por lo que se ha ideado un sistema para tener una contraseña diferente en cada web (además una contraseña sólida) y solo tener que recordar una.

¿Como es esto posible?

Pues con <a title="Pwdhash - Firefox Addons" href="https://addons.mozilla.org/firefox/1033/">PwdHash</a>, una extensión para <a title="Mozilla Firefox" href="http://www.mozilla-europe.org/es/products/firefox/">Firefox</a> que, a partir de una única contraseña, generará una clave diferente para cada web que visitamos. Usa una función que genera una salida dependiendo de la entrada, pero que mediante esos datos de salida no se puede conseguir la entrada.

De esta forma, usando nuestra contraseña “maestra?? y el nombre de dominio de la página a la que accedemos, creará un hash que será el que se envíe como contraseña. Para hacerlo, podemos escribir nuestra contraseña con @@ delante o pulsar F2 antes de escribirla, así de fácil.

Si nos encontramos en un pc sin la extensión instalada (en un cyber) podemos generarla desde <a href="https://www.pwdhash.com/">https://www.pwdhash.com/</a>.

Espero que todo este rollo haya servido para aclarar algo, si encontráis algo erróneo no dudéis en comentármelo, puede que no me haya percatado de algún punto.

<strong>Actulización (21/12/06 18:47): </strong>En un<a title="Washingtonpost - New Firefox Version Fixes 8 Security Holes" href="http://blog.washingtonpost.com/securityfix/2006/12/new_firefox_version_fixes_8_se.html"> blog del washintong post</a> aseguran que un miembro del equipo de seguridad de Mozilla ha comunicado que se va a modificar el gestor de contraseñas para que recoja más información, no citan fuente así que no puedo asegurarlo, supongo que añadirán que se guarde aparte del dominio del formulario, la página a donde se envía, pero como he comentado en el análisis, la situación no cambiaría demasiado.