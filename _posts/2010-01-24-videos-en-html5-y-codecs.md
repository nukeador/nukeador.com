---
ID: 411
post_title: Vídeos en HTML5 y codecs
author: Nukeador
post_excerpt: '¿Te imaginas poder disfrutar de todo el contenido en internet simplemente usando tu navegador? ¿Sin tener que instalar más aplicaciones, plugins o codecs? Bien, pues ese es uno de los objetivos que pretende hacer frente el nuevo estándar HTML5 con el audio y vídeo en la red. Actualmente, la mayoría de navegadores implementa esta nueva [...]'
layout: post
permalink: >
  http://www.mozilla-hispano.org/videos-en-html5-y-codecs/
published: true
post_date: 2010-01-24 14:00:16
---
<p><a href="http://www.mozilla-hispano.org/wp-content/uploads/Ogg-Theora1.jpg"><img class="alignright size-full wp-image-968" title="Ogg Theora" src="http://www.mozilla-hispano.org/wp-content/uploads/Ogg-Theora1.jpg" alt="" width="150" height="100" /></a>¿Te imaginas poder <strong>disfrutar de todo el contenido en internet simplemente usando tu navegador</strong>? ¿<strong>Sin tener que instalar más aplicaciones</strong>, plugins o codecs? Bien, pues ese es uno de los objetivos que pretende hacer frente el <strong>nuevo estándar HTML5 con el audio y vídeo</strong> en la red.</p>
<p>Actualmente, <strong>la mayoría de navegadores implementa esta nueva etiqueta &lt;video&gt;</strong> que permite mostrar el contenido audiovisual sin necesidad de nada más, sin tener que usar Flash, sin tener que instalar codecs.</p>
<p>La historia no es tan bonita como parece ya que nos encontramos con un gran problema, cuando el organismo responsable (<a href="http://www.w3.org/">W3C</a>) de crear la especificación HTML5 hizo el borrador, especificó que el formato de los vídeos debería ir en <a href="http://es.wikipedia.org/wiki/Theora">Theora</a>, un codec de vídeo libre y que no tiene patentes, pero algunas empresas que componen el W3C se quejaron fuertemente (en especial Apple) ya que tenían <strong>intereses comerciales</strong> en usar sus propios codecs, y al final no se especificó un codec concreto para usar con la etiqueta &lt;video&gt;.</p>
<h3><span id="more-962"></span>¿Qué navegadores la implementan?</h3>
<p>Como comentábamos antes, <strong>la mayoría de navegadores ya implementa esta etiqueta</strong>, pero cada uno ha decidió usar un codec para esta etiqueta, vamos a desglosar:</p>
<ul>
<li>Presto/Opera: HTML5 mediante GStreamer (incluye sólo Ogg/Theora).</li>
<li>WebKit/Chrome: HTML5 mediante ffmpeg (Ogg/Theora y H.264/MP4).</li>
<li><strong>Gecko/Firefox: HTML5 con Ogg/Theora.</strong></li>
<li>WebKit/Epiphany: HTML5 mediante GStreamer (Ogg/Theora garantizado).</li>
<li>WebKit/Safari: HTML5 mediante QuickTime (H.264/MOV/M4V, puede reproducir Ogg/Theora con XiphQT components).</li>
</ul>
<p>Vemos que algunos han optado por el codec libre Ogg/Theora, mientas que otros por el códec <a href="http://es.wikipedia.org/wiki/H.264">H.264</a> patentado por MPEG-LA (<a href="http://www.mpegla.com/main/programs/AVC/Pages/Licensors.aspx">a la que pertenecen Apple y Microsoft</a>) y el cual no se puede usar en un programa que lo use sin pagar a la MPEG-LA, y a partir de 2010 todo <strong>el que lo quiera usar (incluso si cuelgas un vídeo con este codec en tu web) tendrá que <a href="http://www.streaminglearningcenter.com/articles/h264-royalties-what-you-need-to-know.html">pagar</a> una <a href="http://www.streamingmedia.com/article.asp?id=11011">licencia</a> de uso</strong>, lo que significa que no podrás mostrar tus vídeos gratis en este formato.</p>
<p>Apostar por un codec no libre para la web es algo erróneo y rompe el sentido de lo que internet es y ha sido, en palabras de Asa Dotzler:</p>
<blockquote><p>La web no sería lo que es hoy si cada blogger tuviera que pagar por una licencia para publicar imágenes y texto en una página. Los vídeos tampoco tendrían que requerir el pago de licencias.</p></blockquote>
<h3>Portales multimedia</h3>
<p>Una sorpresa nos hemos llevado esta semana en la que <strong><a href="http://youtube-global.blogspot.com/2010/01/-youtube-html5-supported.html">tanto Youtube</a> <a href="http://vimeo.com/blog%3A268">como Vimeo</a> anunciaban que empezarían a usar la etiqueta &lt;video&gt; de HTML5</strong> como alternativa para mostrar sus vídeos en vez de Flash. Poco duró la alegría cuando vimos que <strong>sólo lo implementarán para el codec H.264</strong>, dejando a Theora fuera. Los motivos que dan para no usar el codec libre son que tiene menos calidad y que ya tienen todo en H.264, cosa que no entendemos ya que se demostró que <strong>la calidad de Theora es similar</strong> a la que se ofrece ahora mismo en Youtube en la <strong><a href="http://people.xiph.org/~greg/video/ytcompare/comparison.html">comparativa entre Theora y H.264</a></strong> y que ya hay otros distribuidores de contenido que <a href="http://blog.dailymotion.com/2009/05/27/watch-videowithout-flash/">han optado</a> por los formatos libres como el portal de vídeo <strong>Dailymotion que mostró <a href="http://www.dailymotion.com/openvideodemo/">la potencia de la etiqueta &lt;video&gt; con codecs libres</a></strong>.</p>
<p><strong>Actualización:</strong> La <a href="http://www.fsf.org">Free Software Foundation</a> <a href="http://www.fsf.org/blogs/community/youtube-ogg">pide que votemos</a> en la página de sugerencias de Google, <a href="http://productideas.appspot.com/#9/e=3d60a&amp;t=ogg">por la implementación de Ogg/Theora en Youtube</a>.</p>
<p><strong>Actualización 2:</strong> Han creado un <a href="http://www.facebook.com/group.php?gid=431356585522">grupo en Facebook de apoyo a los formatos libres en Youtube</a>.</p>
<h3>Reflexión</h3>
<p>Si queremos <strong>mantener la web abierta</strong>, debemos <strong>apostar siempre por los formatos libres</strong> que permitan a todo el mundo acceder a la información de forma libre y gratuita, sin poner barreras en el camino y sobre todo sin forzar a creadores de contenido y portales de alojamiento a pagar licencias por patentes.</p>
<p>Google puede permitirse pagar millones de dolares al año por el uso de H.264 en YouTube o su navegador Chrome, y posiblemente Mozilla podría también, pero es una <strong>cuestión de principios el que los navegadores Mozilla apuesten por formatos libres</strong>, por lo que representan, porque es la base de internet y porque el código del navegador debe poderse usar por terceros que no tienen por qué pagar licencias a un tercero. ¿Creéis que Firefox hubiera podido desarrollarse por la comunidad si en su momento hubiera tenido que pagar cifras millonarias para usar tecnologías como HTML, CSS o JavaScript?</p>
<p><strong>Navegadores y portales de contenido deben apostar por Ogg/Theora</strong> como codec para la etiqueta &lt;video&gt;, ya que aporta ventajas para todos (además que es el que tiene implementación en mayor número de navegadores actualmente).</p>
<p>No dejemos que la web avance dependiendo de patentes que frenen la innovación. <strong>¡Sí a los formatos libres, sí a la web abierta!</strong></p>
<p>Otras opiniones dentro del mundo Mozilla (en inglés):</p>
<ul>
<li><a href="http://shaver.off.net/diary/2010/01/23/html5-video-and-codecs/">Mike Shaver &#8211; HTML5 video and codecs</a></li>
<li><a href="http://weblogs.mozillazine.org/roc/archives/2010/01/video_freedom_a.html">Robert O&#8217;Callahan &#8211; Video, Freedom And Mozilla</a></li>
<li><a href="http://www.0xdeadbeef.com/weblog/2010/01/html5-video-and-h-264-what-history-tells-us-and-why-were-standing-with-the-web/">Christopher Blizzard &#8211; HTML5 video and H.264</a></li>
<li><a href="http://weblogs.mozillazine.org/roc/archives/2010/01/activex_all_ove.html">Robert O&#8217;Callahan &#8211; ActiveX all over again</a></li>
</ul>




	<a rel="nofollow" class="thickbox" href="http://delicious.com/post?url=http://www.mozilla-hispano.org/videos-en-html5-y-codecs/&amp;title=V%C3%ADdeos%20en%20HTML5%20y%20codecs&amp;notes=%C2%BFTe%20imaginas%20poder%20disfrutar%20de%20todo%20el%20contenido%20en%20internet%20simplemente%20usando%20tu%20navegador?%20%C2%BFSin%20tener%20que%20instalar%20m%C3%A1s%20aplicaciones,%20plugins%20o%20codecs?%20Bien,%20pues%20ese%20es%20uno%20de%20los%20objetivos%20que%20pretende%20hacer%20frente%20el%20nuevo%20est%C3%A1ndar%20HTML5%20co?TB_iframe=true&amp;height=500&amp;width=900"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/delicious.png" title="del.icio.us" alt="del.icio.us" class="sociable-hovers" /></a>
	<a rel="nofollow" class="thickbox" href="http://www.facebook.com/share.php?u=http://www.mozilla-hispano.org/videos-en-html5-y-codecs/&amp;t=V%C3%ADdeos%20en%20HTML5%20y%20codecs?TB_iframe=true&amp;height=500&amp;width=900"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/facebook.png" title="Facebook" alt="Facebook" class="sociable-hovers" /></a>
	<a rel="nofollow" class="thickbox" href="http://www.google.com/bookmarks/mark?op=edit&amp;bkmk=http://www.mozilla-hispano.org/videos-en-html5-y-codecs/&amp;title=V%C3%ADdeos%20en%20HTML5%20y%20codecs&amp;annotation=%C2%BFTe%20imaginas%20poder%20disfrutar%20de%20todo%20el%20contenido%20en%20internet%20simplemente%20usando%20tu%20navegador?%20%C2%BFSin%20tener%20que%20instalar%20m%C3%A1s%20aplicaciones,%20plugins%20o%20codecs?%20Bien,%20pues%20ese%20es%20uno%20de%20los%20objetivos%20que%20pretende%20hacer%20frente%20el%20nuevo%20est%C3%A1ndar%20HTML5%20co?TB_iframe=true&amp;height=500&amp;width=900"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/googlebookmark.png" title="Google Bookmarks" alt="Google Bookmarks" class="sociable-hovers" /></a>
	<a rel="nofollow" class="thickbox" href="http://barrapunto.com/submit.pl?subj=V%C3%ADdeos%20en%20HTML5%20y%20codecs&amp;story=http://www.mozilla-hispano.org/videos-en-html5-y-codecs/?TB_iframe=true&amp;height=500&amp;width=900"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/barrapunto.png" title="BarraPunto" alt="BarraPunto" class="sociable-hovers" /></a>
	<a rel="nofollow" class="thickbox" href="http://bitacoras.com/anotaciones/http%3A//www.mozilla-hispano.org/videos-en-html5-y-codecs/?TB_iframe=true&amp;height=500&amp;width=900"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/bitacoras.png" title="Bitacoras.com" alt="Bitacoras.com" class="sociable-hovers" /></a>
	<a rel="nofollow"  href="mailto:?subject=V%C3%ADdeos%20en%20HTML5%20y%20codecs&amp;body=http://www.mozilla-hispano.org/videos-en-html5-y-codecs/" title="email"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/email_link.png" title="email" alt="email" class="sociable-hovers" /></a>
	<a rel="nofollow"  href="http://meneame.net/submit.php?url=http://www.mozilla-hispano.org/videos-en-html5-y-codecs/" title="Meneame"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/meneame.png" title="Meneame" alt="Meneame" class="sociable-hovers" /></a>
	<a rel="nofollow"  href="http://twitter.com/home?status=V%C3%ADdeos%20en%20HTML5%20y%20codecs%20-%20http://www.mozilla-hispano.org/videos-en-html5-y-codecs/" title="Twitter"><img src="http://www.mozilla-hispano.org/wp-content/plugins/sociable/images/twitter.png" title="Twitter" alt="Twitter" class="sociable-hovers" /></a>


<br/><br/>

<p>Artículos relacionados:<ul><li><a href='http://www.mozilla-hispano.org/llega-vp8-un-formato-de-video-libre/' rel='bookmark' title='Permanent Link: Llega VP8 un formato de vídeo libre'>Llega VP8 un formato de vídeo libre</a></li>
<li><a href='http://www.mozilla-hispano.org/implementacion-nativa-de-ogg-vorbis-y-theora-en-firefox-31/' rel='bookmark' title='Permanent Link: Implementación nativa de Ogg Vorbis y Theora en Firefox 3.1'>Implementación nativa de Ogg Vorbis y Theora en Firefox 3.1</a></li>
</ul></p>