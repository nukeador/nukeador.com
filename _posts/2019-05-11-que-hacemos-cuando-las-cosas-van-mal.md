---
ID: 1859
post_title: Qué hacemos cuando las cosas van mal
author: Nukeador
post_excerpt: >
  Siempre nos esforzamos para que Firefox
  proporcione una gran experiencia de uso.
  El fin de semana pasado fallamos, y lo
  lamentamos.
layout: post
permalink: >
  https://www.mozilla-hispano.org/que-hacemos-cuando-las-cosas-van-mal/
published: true
post_date: 2019-05-11 01:15:16
---

<figure class="wp-block-image"><img src="https://www.mozilla-hispano.org/wp-content/uploads/Logo2-1024x563.png" alt="" class="wp-image-42000" srcset="https://www.mozilla-hispano.org/wp-content/uploads/Logo2-1024x563.png 1024w, https://www.mozilla-hispano.org/wp-content/uploads/Logo2-300x165.png 300w, https://www.mozilla-hispano.org/wp-content/uploads/Logo2-130x72.png 130w, https://www.mozilla-hispano.org/wp-content/uploads/Logo2.png 1400w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>



<p><em>Esta es una traducción del </em><a href="https://blog.mozilla.org/blog/2019/05/09/what-we-do-when-things-go-wrong/"><em>artículo original</em></a><em> realizado por Joe Hildebrand</em></p>



<p>Siempre nos esforzamos para que Firefox proporcione una gran experiencia de uso. El fin de semana pasado fallamos, y lo lamentamos. </p>



<p>Un error por nuestra parte impidió la instalación de nuevos complementos e impidió que funcionaran los complementos existentes. Ahora que hemos podido restaurar esta funcionalidad para la mayoría de los usuarios de Firefox, queremos explicar un poco sobre lo que sucedió y decirte qué otras cosas haremos.</p>



<p>Los complementos son una característica importante de Firefox. Te permiten personalizar tu navegador y agregar funcionalidades valiosas a tu experiencia en la web. Sabemos lo importante que es esto, por lo que en los últimos años hemos dedicado mucho tiempo a encontrar formas de hacer que los complementos sean más y más seguros. Sin embargo, debido a que los complementos son tan poderosos, también hemos trabajado duro para construir e implementar sistemas para protegerte de complementos maliciosos. El problema fue un error de implementación en uno de esos sistemas, cuya medida de seguridad era que los complementos se deshabilitaran. Aunque creemos que el diseño básico de nuestro sistema de complementos es sólido, vamos a seguir trabajando para refinar estos sistemas para que no surjan problemas similares en el futuro. </p>



<p>Para solucionar este problema lo más rápido posible, utilizamos nuestro sistema de &#171;<a href="https://support.mozilla.org/kb/shield">Estudios</a>&#187; para implementar la solución inicial, que requiere que los usuarios tengan la opción de <a href="https://www.mozilla.org/privacy/firefox/">telemetría</a> activa.  Algunos usuarios que habían optado por dejar de utilizar <strong>Telemetría</strong> optaron por volver a participar para obtener la solución inicial lo antes posible. Como anunciamos en <a href="https://www.mozilla-hispano.org/actualizacion-sobre-los-complementos-en-firefox/">el blog de complementos de Firefox</a>, ya no es necesario tener estudios activos para recibir actualizaciones; por favor, verifica que las configuraciones de Firefox coincidan con tus preferencias personales antes de que volvamos a habilitar los Estudios, lo que ocurrirá en algún momento después de las 16:00 del 13 de mayo de 2019. Con el fin de respetar al máximo las posibles elecciones de nuestros usuarios, por nuestra configuración actual, eliminaremos todos los datos de telemetría y estudios generados por nuestros usuarios recopilados entre el 4 y 11 de mayo (más específicamente entre las 2019-05-04T11:00:00 y 2019-05-11T11:00:00Z). </p>



<p>Nuestro CTO, Eric Rescorla, detalla más sobre lo que sucedió técnicamente <a href="https://hacks.mozilla.org/2019/05/technical-details-on-the-recent-firefox-add-on-outage/">en este post</a> (en). </p>



<p>Nos gustaría extender nuestro agradecimiento a las personas que  trabajaron arduamente para abordar este problema, incluidos los  aproximadamente cien miembros de la comunidad y empleados que localizan contenido y responden preguntas en <a href="https://support.mozilla.org/">https://support.mozilla.org/</a>, Twitter y Reddit. </p>



<p>Hay muchos más detalles que compartiremos como parte de un post mortem más largo que haremos público, incluidos detalles sobre cómo  solucionamos este problema y por qué elegimos este enfoque. Mereces un informe completo, pero no queríamos esperar hasta que se terminara el proceso para contarte lo que sabíamos hasta ahora. Te hemos decepcionado y lo que sucedió puede haber afectado un poco tu confianza en nosotros, pero esperamos que nos brindes la oportunidad de recuperarla. </p>