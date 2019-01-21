---
ID: 354
post_title: Vídeo ogv con HTML5 en WordPress
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/06/12/2009/video-ogv-con-html5-en-wordpress/
published: true
post_date: 2009-12-06 18:33:07
---
<p>Recientemente he tenido que desarrollar para <a href="http://www.mozilla-hispano.org/">Mozilla Hispano</a> un <strong>shortcode para Wordpress</strong> que nos permitiese añadir a los artículos <strong>vídeos en <a href="http://es.wikipedia.org/wiki/Theora">formato libre Ogg Theora</a></strong> y que mostrará el vídeo en flash para aquellos navegadores que aún no admitan <strong><a href="https://developer.mozilla.org/Es/Etiquetas_audio_y_video_en_Firefox">la etiqueta vídeo</a> de <a href="http://es.wikipedia.org/wiki/HTML_5">HTML5</a></strong>.</p>
<p>La sintaxis es la siguiente, sólo los atributos ogv y flash son obligatorios:</p>
<p><code>[open-video poster="/ruta/a/imagen.jpg" ogv="/ruta/al/archivo.ogv" mp4="/ruta/al/archivo.mp4" flash="/ruta/al/flash" width="500" height="350" ]</code></p>
<ul>
<li>poster → Imagen opcional para la vista previa.</li>
<li>ogv → Ruta al archivo ogv.</li>
<li>mp4 → Ruta al archivo opcional mp4 para navegadores que admiten video con este formato.</li>
<li>flash → Ruta al flash.</li>
<li>width → Ancho, de no definirse usará 640.</li>
<li>height → Alto, de no definirse usará 510.</li>
</ul>
<p>Para poderlo usar, debereís añadir al archivo <em>functions.php</em> de vuestro tema de Wordpress lo siguiente:</p>
<pre lang="php">
function open_video($atts, $content = null) {
        extract(shortcode_atts(array(
                "width" => '',
                "height" => '',
                "poster" => '',
                "ogv" => '',
                "mp4" => '',
                "flash" => ''
        ), $atts));
        global $post;
        /* Tomamos tamaños o si no tomamos valores por defecto */
		if (empty($width)) $width = "640";
		if (empty($height)) $height = "510";

        $salida = "<video";
		$salida .= " width=\"" . $width . "\" ";
		$salida .= " height=\"" . $height . "\" ";

		if (!empty($poster))
			$salida .= "poster=\"" . $poster . "\" "; 

		$salida .= "controls>";

		$salida .= "<source src=\"" . $ogv . "\" type=\"video/ogg\" />";

		if (!empty($mp4))
			$salida .= "<source src=\"" . $mp4 . "\" type=\"video/mp4\" />";

		$salida .= "<object width=\"" . $width . "\" height=\"" . $height . "\" type=\"application/x-shockwave-flash\"";
		$salida .= " data=\"" . $flash . "\">";
		$salida .= "<param name=\"movie\" value=\"" . $flash . "\" />";
		$salida .=	"

Necesitas el plugin de Flash para ver este vídeo

</object></video>";

		$salida .= "

<small>Descargar vídeo <a href=\"" . $ogv . "\">en formato libre ogv</a>";

		if (!empty($mp4))
			$salida .= " o <a href=\"" . $mp4 . "\">en formato mp4</a>.";

		$salida .= "</small>

";
        return $salida;
}
add_shortcode("open-video", "open_video");
</pre>