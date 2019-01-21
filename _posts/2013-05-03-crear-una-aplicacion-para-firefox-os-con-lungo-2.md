---
ID: 1512
post_title: >
  Crear una aplicación para Firefox OS
  con Lungo
author: Nukeador
post_excerpt: 'En este art&iacute;culo veremos como crear aplicaciones para Firefox OS es un juego de ni&ntilde;os. Si ya sabes crear p&aacute;ginas web, ya tienes todo lo que necesitas para empezar a crear aplicaciones compatibles con Firefox OS.'
layout: post
permalink: >
  https://www.mozilla-hispano.org/crear-una-aplicacion-para-firefox-os-con-lungo/
published: true
post_date: 2013-05-03 19:43:20
---
<p>Crear aplicaciones para Firefox OS es un juego de niños. Si ya sabes crear páginas web, ya tienes todo lo que necesitas para empezar a crear aplicaciones compatibles con Firefox OS.</p>
<p>Hoy vamos a repasar una forma que personalmente creo bastante ágil para crear una aplicación para dispositivos móviles usando el <a href="http://lungo.tapquo.com/">framework de desarrollo Lungo</a>.</p>
<p><iframe style="display: block; margin: auto;" src="https://www.youtube-nocookie.com/embed/ggun8HZce8w?rel=0" height="360" width="480" allowfullscreen="" frameborder="0"></iframe></p>
<p>El código del ejemplo se puede descargar <a href="https://github.com/nukeador/lungo-fxos-boilerplate">desde github</a>.</p>
<p>La novedad para muchos en este desarrollo, es la creación de un archivo manifest con la información de la aplicación:</p>

<div class="wp_syntax"><table><caption><a href="https://github.com/nukeador/lungo-fxos-boilerplate/blob/master/manifest.webapp">/lungo-fxos-boilerplate/blob/master/manifest.webapp</a></caption><tr><td class="line_numbers"><pre>1
2
3
4
5
6
7
8
9
10
11
12
13
</pre></td><td class="code"><pre class="javascript" style="font-family:monospace;"><span style="color: #009900;">&#123;</span>
<span style="color: #3366CC;">&quot;name&quot;</span><span style="color: #339933;">:</span> <span style="color: #3366CC;">&quot;Lungo Boilerplate&quot;</span><span style="color: #339933;">,</span>
<span style="color: #3366CC;">&quot;description&quot;</span><span style="color: #339933;">:</span> <span style="color: #3366CC;">&quot;Lungo Boilerplate para Firefox OS&quot;</span><span style="color: #339933;">,</span>
<span style="color: #3366CC;">&quot;launch_path&quot;</span><span style="color: #339933;">:</span> <span style="color: #3366CC;">&quot;/index.html&quot;</span><span style="color: #339933;">,</span>
<span style="color: #3366CC;">&quot;icons&quot;</span><span style="color: #339933;">:</span> <span style="color: #009900;">&#123;</span>
<span style="color: #3366CC;">&quot;128&quot;</span><span style="color: #339933;">:</span> <span style="color: #3366CC;">&quot;/img/icon.png&quot;</span>
<span style="color: #009900;">&#125;</span><span style="color: #339933;">,</span>
<span style="color: #3366CC;">&quot;developer&quot;</span><span style="color: #339933;">:</span> <span style="color: #009900;">&#123;</span>
<span style="color: #3366CC;">&quot;name&quot;</span><span style="color: #339933;">:</span> <span style="color: #3366CC;">&quot;Nukeador&quot;</span><span style="color: #339933;">,</span>
<span style="color: #3366CC;">&quot;url&quot;</span><span style="color: #339933;">:</span> <span style="color: #3366CC;">&quot;https://www.mozilla-hispano.org/labs/&quot;</span>
<span style="color: #009900;">&#125;</span><span style="color: #339933;">,</span>
<span style="color: #3366CC;">&quot;default_locale&quot;</span><span style="color: #339933;">:</span> <span style="color: #3366CC;">&quot;es&quot;</span>
<span style="color: #009900;">&#125;</span></pre></td></tr></table></div>

<p>El archivo manifest puede tener muchas más cosas, detalladas en <a href="https://marketplace.firefox.com/developers/docs/manifests">la documentación de Marketplace</a>, y que le dirá al dispositivo el icono y nombre de la aplicación a la hora de instalarla.</p>
<p>Para utilizar todas las ventajas que nos ofrece Lungo, simplemente tendremos que añadir los estilos en la cabecera:</p>

<div class="wp_syntax"><table><caption><a href="https://github.com/nukeador/lungo-fxos-boilerplate/blob/master/index.html">/lungo-fxos-boilerplate/blob/master/index.html</a></caption><tr><td class="line_numbers"><pre>1
2
3
4
5
</pre></td><td class="code"><pre class="html5" style="font-family:monospace;"><span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">link</span> <span style="color: #000066;">rel</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;stylesheet&quot;</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;components/lungo/lungo.css&quot;</span><span style="color: #66cc66;">/</span>&gt;</span>
<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">link</span> <span style="color: #000066;">rel</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;stylesheet&quot;</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;components/lungo/lungo.icon.css&quot;</span><span style="color: #66cc66;">/</span>&gt;</span>
<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">link</span> <span style="color: #000066;">rel</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;stylesheet&quot;</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;components/lungo/lungo.icon.brand.css&quot;</span><span style="color: #66cc66;">/</span>&gt;</span>
<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">link</span> <span style="color: #000066;">rel</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;stylesheet&quot;</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;components/lungo/lungo.css&quot;</span><span style="color: #66cc66;">/</span>&gt;</span>
<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">link</span> <span style="color: #000066;">rel</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;stylesheet&quot;</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;components/lungo/theme.lungo.css&quot;</span><span style="color: #66cc66;">/</span>&gt;</span></pre></td></tr></table></div>

<p>Y las librerías js antes del cierre del body:</p>

<div class="wp_syntax"><table><caption><a href="https://github.com/nukeador/lungo-fxos-boilerplate/blob/master/index.html">/lungo-fxos-boilerplate/blob/master/index.html</a></caption><tr><td class="line_numbers"><pre>1
2
</pre></td><td class="code"><pre class="html5" style="font-family:monospace;"><span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">script</span> <span style="color: #000066;">src</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;components/quojs/quo.js&quot;</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">script</span>&gt;</span>
<span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">script</span> <span style="color: #000066;">src</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;components/lungo/lungo.js&quot;</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">script</span>&gt;</span></pre></td></tr></table></div>

<p>Con un poco de html definiendo sections y articles tendremos montada la interfaz completa de nuestra aplicación:</p>

<div class="wp_syntax"><table><caption><a href="https://github.com/nukeador/lungo-fxos-boilerplate/blob/master/index.html">/lungo-fxos-boilerplate/blob/master/index.html</a></caption><tr><td class="line_numbers"><pre>1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
</pre></td><td class="code"><pre class="html5" style="font-family:monospace;">    <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">section</span> <span style="color: #000066;">id</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;main&quot;</span> data-transition<span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;slide&quot;</span>&gt;</span>
&nbsp;
        <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">header</span> data-<span style="color: #000066;">title</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;Inicio&quot;</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">nav</span> <span style="color: #000066;">class</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;right&quot;</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">a</span> <span style="color: #000066;">id</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;install&quot;</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;#&quot;</span> data-icon<span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;plus&quot;</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">a</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">nav</span>&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">header</span>&gt;</span>
&nbsp;
        <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">article</span> <span style="color: #000066;">id</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;main-article&quot;</span> <span style="color: #000066;">class</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;active list&quot;</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">ul</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">li</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">strong</span>&gt;</span>Título<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">strong</span>&gt;</span>
                    <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">br</span> <span style="color: #66cc66;">/</span>&gt;</span>
                    Este es mi texto<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">li</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">ul</span>&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">article</span>&gt;</span>
&nbsp;
        <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">article</span> <span style="color: #000066;">id</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;article2&quot;</span> <span style="color: #000066;">class</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;list indented&quot;</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">ul</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">li</span>&gt;</span>Este es el texto 2<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">li</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">ul</span>&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">article</span>&gt;</span>
&nbsp;
        <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">footer</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">nav</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">a</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;#main-article&quot;</span> data-icon<span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;home&quot;</span> <span style="color: #000066;">class</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;active&quot;</span> data-router<span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;article&quot;</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">a</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">a</span> <span style="color: #000066;">href</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;#article2&quot;</span> data-icon<span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;folder&quot;</span> data-router<span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;article&quot;</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">a</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">nav</span>&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">footer</span>&gt;</span>
    <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">section</span>&gt;</span></pre></td></tr></table></div>

<p>Cabe destacar el uso que hace Lungo de los data-atributtes que nos permitirán definir muchos comportamientos, iconos, imágenes, destino de los enlaces o títulos. <a href="http://lungo.tapquo.com/howto/prototype/">La documentación de Lungo</a> es muy extensa y descriptiva al respecto de lo que se puede hacer.</p>
<p>Adicionalmente vemos la inclusión de una librería llamada <a href="https://github.com/nukeador/lungo-fxos-boilerplate/blob/master/components/base.js">base.js</a></p>

<div class="wp_syntax"><table><caption><a href="https://github.com/nukeador/lungo-fxos-boilerplate/blob/master/index.html">/lungo-fxos-boilerplate/blob/master/index.html</a></caption><tr><td class="line_numbers"><pre>1
</pre></td><td class="code"><pre class="html5" style="font-family:monospace;"><span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">script</span> <span style="color: #000066;">src</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;components/base.js&quot;</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">script</span>&gt;</span></pre></td></tr></table></div>

<p>Que nos permitirá que se invoque la instalación de la aplicación desde el elemento con id #install. Esto es muy útil por ejemplo si alojamos la aplicación web en nuestro servidor, la gente usa la aplicación desde nuestro dominio myapp.midominio.com y quiere instalarla en su dispositivo (ya sea Firefox OS, Firefox para Android o Firefox para escritorio). En próximos artículos veremos como usar el caché de aplicación para que esta no requiera conexión a la red.</p>
<p>Si queréis ampliar sobre Lungo, os recomiendo dar un vistazo al <a href="https://www.youtube.com/watch?v=EwmJ88Nq600">extenso hangout</a> que realizaron con la gente de Desarrolloweb.com.</p>
<p>Enlaces:</p>
<ul>
<li><a href="https://addons.mozilla.org/es/firefox/addon/firefox-os-simulator/">Firefox OS Simulator</a></li>
<li><a href="https://github.com/nukeador/lungo-fxos-boilerplate">Código del ejemplo</a></li>
<li><a href="https://marketplace.firefox.com/developers/">Documentación para desarrolladores de Marketplace</a></li>
<li><a href="http://lungo.tapquo.com/">Web de Lungo</a></li>
</ul>
<div class='yarpp-related-rss'>
<p>Artículos relacionados:</p><ul>
<li><a href="https://www.mozilla-hispano.org/creando-una-aplicacion-de-pago-para-firefox-os/" rel="bookmark" title="Crear una aplicación de pago para Firefox OS">Crear una aplicación de pago para Firefox OS </a></li>
<li><a href="https://www.mozilla-hispano.org/aplicaciones-para-firefox-os-con-angularjs/" rel="bookmark" title="Crear aplicaciones para Firefox OS utilizando AngularJS">Crear aplicaciones para Firefox OS utilizando AngularJS </a></li>
<li><a href="https://www.mozilla-hispano.org/aplicacion-con-el-modulo-de-caja-flexible-de-css3/" rel="bookmark" title="Diseño de una aplicación con el módulo de caja flexible de CSS3">Diseño de una aplicación con el módulo de caja flexible de CSS3 </a></li>
</ul>
</div>