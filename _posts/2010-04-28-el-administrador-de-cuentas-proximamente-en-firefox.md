---
ID: 511
post_title: >
  El administrador de cuentas
  próximamente en Firefox
author: Nukeador
post_excerpt: 'Si aún no lo conocéis, Account Manager (o administrador de cuentas) es un proyecto que se inició como experimento en Mozilla Labs y que tiene como objetivo que sea el navegador quién gestione la identidad de los usuarios y los registre, inicie sesión o la cierre con las webs de forma transparente. Se acaba de [...]'
layout: post
permalink: >
  http://www.mozilla-hispano.org/el-administrador-de-cuentas-proximamente-en-firefox/
published: true
post_date: 2010-04-28 11:55:36
---
<p>Si aún no lo conocéis, <a href="http://www.mozilla.com/firefox/accountmanager/">Account Manager</a> (o administrador de cuentas) es un proyecto que se inició como experimento en <a href="http://labs.mozilla.org/">Mozilla Labs</a> y que tiene como objetivo que sea <strong>el navegador quién gestione la identidad de los usuarios</strong> y los registre, inicie sesión o la cierre con las webs de forma transparente.</p>
<p><img class="aligncenter size-full wp-image-1393" title="Administrador de cuentas" src="http://www.mozilla-hispano.org/wp-content/uploads/admin-cuentas4.png" alt="" width="717" height="72" /></p>
<p>Se acaba de publicar una <a href="http://www.mozilla.com/firefox/accountmanager/">versión alpha de la extensión</a> y se ha anunciado que pronto <strong>la veremos integrada en nuestro navegador</strong> favorito. Pero ¿cómo funciona el administrador de cuentas?</p>
<p><span id="more-1387"></span></p>
<h3>Objetivos</h3>
<ul>
<li><strong>Crear un protocolo</strong> que las webs puedan usar para definir cómo administran sus cuentas y sesiones de forma que el navegador pueda entender. Esto es, que si yo tengo una web en la que se pueden registrar usuarios, pueda decir al navegador cómo se pueden registrar, iniciar o cerrar sesión para que lo gestione. <a href="https://wiki.mozilla.org/Labs/Weave/Identity/Account_Manager/Spec/Latest">Leer la última especificación técnica</a>.</li>
<li><strong>Crear una extensión</strong> para implementar este protocolo en Firefox.</li>
</ul>
<h3>¿Cómo funciona?</h3>
<p>Veámonoslo con unos ejemplos prácticos:</p>
<h4>Conexión simple</h4>
<p>Juan visita continuamente páginas que requieren iniciar sesión como usuario y aunque tiene guardadas todas sus contraseñas para que el navegador las recuerde, <strong>está cansado de tener que buscar el formulario de inicio de sesión</strong> y recordar dónde está en cada sitio.</p>
<p>El administrador de cuentas le <strong>proporciona un botón para iniciar sesión con un solo clic</strong> en todas estas páginas y si selecciona la opción &#8220;mantenerme siempre conectado&#8221;, nunca más tendrá que lidiar con pantallas de inicio de sesión.</p>
<p><a href="http://www.mozilla-hispano.org/wp-content/uploads/admin-cuentas2.png"><img class="aligncenter size-medium wp-image-1390" title="Inicio de sesión" src="http://www.mozilla-hispano.org/wp-content/uploads/admin-cuentas2-300x189.png" alt="" width="300" height="189" /></a></p>
<h4>Conexión múltiple</h4>
<p>Puede que Juan y Pedro usen la misma sesión en un equipo y no quieran o sepan crear varias cuentas en el sistema (como sería recomendable), por lo que <strong>cada uno tiene un perfil creado en el administrador de cuentas</strong>, pudiendo usar uno u otro en las páginas web donde requieran su identidad.</p>
<p><a href="http://www.mozilla-hispano.org/wp-content/uploads/admin-cuentas-1.png"><img class="aligncenter size-medium wp-image-1389" title="Administrador de cuentas" src="http://www.mozilla-hispano.org/wp-content/uploads/admin-cuentas-1-300x291.png" alt="" width="300" height="291" /></a></p>
<h4>Registro automático y cambio de contraseña</h4>
<p>Pedro visita habitualmente una web que le comenta que si se crea una cuenta de usuario podrá disfrutar de nuevas y mejores opciones, por lo que hace clic en el botón &#8220;Conectar&#8221;.  Firefox le presentará un resumen con los datos personales (previamente definidos) que se enviarán al sitio y, una vez confirmados, la cuenta (con una contraseña aleatoria) se creará.</p>
<p><a href="http://www.mozilla-hispano.org/wp-content/uploads/admin-cuentas3.png"><img class="aligncenter size-medium wp-image-1391" title="Registro de usuarios" src="http://www.mozilla-hispano.org/wp-content/uploads/admin-cuentas3-300x272.png" alt="" width="300" height="272" /></a></p>
<h4>Cambio de contraseña maestra</h4>
<p>Paula ha perdido su portatil en un bar hace unos días y está preocupada por sus datos personales y contraseñas. Dado que tiene un navegador sincronizado con el pc de sobremesa, abre el administrador de cuentas en este último y con una sola acción, cambia la contraseña de todas las webs donde está registrada.</p>
<h3>Tengo una web, ¿cómo lo implemento para mis usuarios?</h3>
<p>Tendrás que crear un documento JSON que el navegador pueda leer automáticamente con la información sobre los métodos que tu web implementa, por ejemplo para iniciar sesión:</p>
<p><code><br />
{<br />
"methods": {<br />
"username-password-form": {<br />
"connect": {<br />
"method": "POST",<br />
"path": "/accounts/LoginAuth",<br />
"params": {<br />
"username": "Email",<br />
"password": "Passwd"<br />
}<br />
}<br />
}<br />
}<br />
}<br />
</code></p>
<p>Recuerda implementar en el archivo json al menos los métodos para inicio y cierre de sesión, lee <a href="https://wiki.mozilla.org/Labs/Weave/Identity/Account_Manager/Spec/Latest#Appendix_A:_Account_Management_Control_Document_Example">la documentación al respecto</a>.</p>
<p>Este archivo lo llamaremos desde un archivo <em>host-meta</em> dentro de la carpeta <em>.well-known/</em> quedando accesible de la forma <em>http://www.tuweb.com/.well-known/host-meta </em><a href="https://wiki.mozilla.org/Labs/Weave/Identity/Account_Manager/Spec/Latest#Appendix_B:_Host-meta_example">Ver ejemplo de host-meta</a>.<em><br />
</em></p>
<p>Para que el navegador pueda saber si el usuario ha iniciado o no sesión, deberás también modificar el código de tu aplicación donde se guarda la cookie de sesión para que también envíe una cabecera HTTP con el estado de la sesión:</p>
<p><em>X-Account-Management-Status: active; name=&#8221;Joe User&#8221; </em></p>
<p><a href="https://wiki.mozilla.org/Labs/Weave/Identity/Account_Manager/Spec/Latest#Determining_the_Account_Session_Status">Ver documentación al respecto</a>.</p>




	<a rel="nofollow" class="thickbox" href="http://delicious.com/post?url=http://www.mozilla-hispano.org/el-administrador-de-cuentas-proximamente-en-firefox/&amp;title=El%20administrador%20de%20cuentas%20pr%C3%B3ximamente%20en%20Firefox&amp;notes=Si%20a%C3%BAn%20no%20lo%20conoc%C3%A9is,%20Account%20Manager%20(o%20administrador%20de%20cuentas)%20es%20un%20proyecto%20que%20se%20inici%C3%B3%20como%20experimento%20en%20Mozilla%20Labs%20y%20que%20tiene%20como%20objetivo%20que%20sea%20el%20navegador%20qui%C3%A9n%20gestione%20la%20identidad%20de%20los%20usuarios%20y%20los%20registre,%20inicie%20se?TB_iframe=true&amp;height=500&amp;width=900"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/delicious.png" title="del.icio.us" alt="del.icio.us" class="sociable-hovers" /></a>
	<a rel="nofollow" class="thickbox" href="http://www.facebook.com/share.php?u=http://www.mozilla-hispano.org/el-administrador-de-cuentas-proximamente-en-firefox/&amp;t=El%20administrador%20de%20cuentas%20pr%C3%B3ximamente%20en%20Firefox?TB_iframe=true&amp;height=500&amp;width=900"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/facebook.png" title="Facebook" alt="Facebook" class="sociable-hovers" /></a>
	<a rel="nofollow" class="thickbox" href="http://www.google.com/bookmarks/mark?op=edit&amp;bkmk=http://www.mozilla-hispano.org/el-administrador-de-cuentas-proximamente-en-firefox/&amp;title=El%20administrador%20de%20cuentas%20pr%C3%B3ximamente%20en%20Firefox&amp;annotation=Si%20a%C3%BAn%20no%20lo%20conoc%C3%A9is,%20Account%20Manager%20(o%20administrador%20de%20cuentas)%20es%20un%20proyecto%20que%20se%20inici%C3%B3%20como%20experimento%20en%20Mozilla%20Labs%20y%20que%20tiene%20como%20objetivo%20que%20sea%20el%20navegador%20qui%C3%A9n%20gestione%20la%20identidad%20de%20los%20usuarios%20y%20los%20registre,%20inicie%20se?TB_iframe=true&amp;height=500&amp;width=900"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/googlebookmark.png" title="Google Bookmarks" alt="Google Bookmarks" class="sociable-hovers" /></a>
	<a rel="nofollow" class="thickbox" href="http://barrapunto.com/submit.pl?subj=El%20administrador%20de%20cuentas%20pr%C3%B3ximamente%20en%20Firefox&amp;story=http://www.mozilla-hispano.org/el-administrador-de-cuentas-proximamente-en-firefox/?TB_iframe=true&amp;height=500&amp;width=900"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/barrapunto.png" title="BarraPunto" alt="BarraPunto" class="sociable-hovers" /></a>
	<a rel="nofollow" class="thickbox" href="http://bitacoras.com/anotaciones/http%3A//www.mozilla-hispano.org/el-administrador-de-cuentas-proximamente-en-firefox/?TB_iframe=true&amp;height=500&amp;width=900"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/bitacoras.png" title="Bitacoras.com" alt="Bitacoras.com" class="sociable-hovers" /></a>
	<a rel="nofollow"  href="mailto:?subject=El%20administrador%20de%20cuentas%20pr%C3%B3ximamente%20en%20Firefox&amp;body=http://www.mozilla-hispano.org/el-administrador-de-cuentas-proximamente-en-firefox/" title="email"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/email_link.png" title="email" alt="email" class="sociable-hovers" /></a>
	<a rel="nofollow"  href="http://meneame.net/submit.php?url=http://www.mozilla-hispano.org/el-administrador-de-cuentas-proximamente-en-firefox/" title="Meneame"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/meneame.png" title="Meneame" alt="Meneame" class="sociable-hovers" /></a>
	<a rel="nofollow"  href="http://twitter.com/home?status=El%20administrador%20de%20cuentas%20pr%C3%B3ximamente%20en%20Firefox%20-%20http://www.mozilla-hispano.org/el-administrador-de-cuentas-proximamente-en-firefox/" title="Twitter"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/twitter.png" title="Twitter" alt="Twitter" class="sociable-hovers" /></a>


<br/><br/>

<p>Artículos relacionados:<ul><li><a href='http://www.mozilla-hispano.org/firefox-de-64-bits-proximamente-en-windows-mac-os-x-y-linux/' rel='bookmark' title='Permanent Link: Firefox de 64 bits próximamente en Windows, Mac OS X y Linux'>Firefox de 64 bits próximamente en Windows, Mac OS X y Linux</a></li>
</ul></p>