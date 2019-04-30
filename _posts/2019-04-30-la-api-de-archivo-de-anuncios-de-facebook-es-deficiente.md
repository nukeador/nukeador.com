---
ID: 1853
post_title: >
  La API de archivo de anuncios de
  Facebook es deficiente
author: Nukeador
post_excerpt: 'La herramienta de Facebook cumple  solo con dos de los cinco est&aacute;ndares m&iacute;nimos de los expertos. Esa es una  calificaci&oacute;n reprobatoria.'
layout: post
permalink: >
  https://www.mozilla-hispano.org/la-api-de-archivo-de-anuncios-de-facebook-es-deficiente/
published: true
post_date: 2019-04-30 14:13:32
---

<p>Esta es una traducción del <a href="https://blog.mozilla.org/blog/2019/04/29/facebooks-ad-archive-api-is-inadequate/">artículo original</a> realizado por Mozilla</p>



<h2><em>La herramienta de Facebook cumple solo con dos de los cinco estándares mínimos de los expertos. Esto es un claro fallo.</em> </h2>



<p>Facebook se <a href="https://blog.mozilla.org/blog/2019/02/13/facebook-answers-mozillas-call-to-deliver-open-ad-api-ahead-of-eu-election/">comprometió</a> en febrero a lanzar una API de archivo de anuncios para que la publicidad política en la plataforma sea más transparente. La compañía finalmente <a href="https://newsroom.fb.com/news/2019/03/a-better-way-to-learn-about-ads/">lanzó esta API</a> a fines de marzo, y hemos estado haciendo una revisión para determinar si está a la altura. </p>



<p> Si bien apreciamos que Facebook cumpla con su compromiso de hacer público la API de archivo de anuncios, la forma en la que ha realizado  la API deja mucho que desear. La Comisión Europea también insinuó esto en su análisis de la <a href="https://ec.europa.eu/newsroom/dae/document.cfm?doc_id=58806">semana pasada</a> cuando dijo que &#171;son necesarias más mejoras técnicas&#187;. </p>



<p>Es un hecho que la API no proporciona los datos necesarios. Y está diseñada de manera que dificulta el importante trabajo de los investigadores, que informan al público y a los responsables de formular políticas sobre la naturaleza y las consecuencias de la información falsa. </p>



<p> El mes pasado, Mozilla y más de sesenta investigadores <a href="https://www.mozilla-hispano.org/facebook-y-google-asi-es-como-deberia-ser-un-api-eficaz-de-archivo-anuncios/">publicaron cinco pautas</a> que esperamos que la API de Facebook cumpla. La API de Facebook no cumple con tres de estas cinco pautas. Es demasiado pronto para determinar si cumple con las otras dos pautas. A continuación se muestra nuestro análisis: </p>



<p> <strong>[1]</strong> <img src="https://s.w.org/images/core/emoji/11.2.0/72x72/274c.png" alt="❌" class="wp-smiley" style="height: 1em; max-height: 1em;" /> </p>



<p><strong>Pauta de los investigadores</strong>: una API abierta y funcional debe tener contenido publicitario político completo. </p>



<p><strong>API de Facebook</strong>: es imposible determinar si la API de Facebook es completa, ya que requiere que uses palabras clave para buscar en la base de datos. No te proporciona todos los datos de anuncios o te permite filtrarlos utilizando criterios o filtros específicos, como lo hacen casi todas las demás bases de datos en línea. Y como no puedes descargar datos en masa y los anuncios en la API no reciben un identificador único, Facebook hace imposible obtener una imagen completa de todos los anuncios que se ejecutan en su plataforma (que es <a href="https://www.facebook.com/ads/library">exactamente lo contrario de lo que dicen estar haciendo</a> ). </p>



<hr class="wp-block-separator"/>



<p> <strong>[2] <img src="https://s.w.org/images/core/emoji/11.2.0/72x72/274c.png" alt="❌" class="wp-smiley" style="height: 1em; max-height: 1em;" /></strong> </p>



<p> <strong>Pauta de los investigadores</strong>: Una API abierta y funcional debe proporcionar el contenido del anuncio y la información sobre los criterios de selección. </p>



<p> <strong>API de Facebook</strong>: La API no proporciona información sobre los criterios de segmentación, por lo que los investigadores no tienen forma de decirle a la audiencia que los anunciantes están pagando para llegar a ellos. La API tampoco proporciona datos de participación (por ejemplo, clics, me gusta y acciones compartidas), lo que significa que los investigadores no pueden ver cómo interactúan los usuarios con un anuncio. Los datos de segmentación y participación son importantes porque les permite a los investigadores ver qué tipos de usuarios trata de influir un anunciante y si sus intentos tuvieron éxito o no. </p>



<hr class="wp-block-separator"/>



<p> <strong>[3]</strong> </p>



<p><strong>Pauta de los investigadores</strong>: una API abierta y funcional debe tener acceso a datos actualizados e históricos. </p>



<p> <strong>API de Facebook</strong>: los datos de los anuncios estarán disponibles en el archivo durante siete años, lo que en realidad es bastante bueno. Debido a que la API es nueva y aún no se ha completado correctamente, todavía no podemos evaluar si está actualizada, si se solucionarán los errores o si Facebook admitirá estudios a largo plazo. </p>



<hr class="wp-block-separator"/>



<p> <strong>[4]</strong> </p>



<p> <strong>Pauta de los investigadores</strong>: Una API abierta y funcional debe ser accesible y compartir con el público en general. </p>



<p> <strong>API de Facebook</strong>: estos datos ahora están disponibles como parte del estándar GraphAPI de Facebook y se rigen por los Términos de servicio de los desarrolladores de Facebook. Es demasiado pronto para determinar qué restricciones exactas creará esto para la disponibilidad pública y la divulgación de datos. </p>



<hr class="wp-block-separator"/>



<p> <strong>[5] <img src="https://s.w.org/images/core/emoji/11.2.0/72x72/274c.png" alt="❌" class="wp-smiley" style="height: 1em; max-height: 1em;" /></strong> </p>



<p> <strong>Pauta de los investigadores</strong>: Una API funcional y abierta debe potenciar, no limitar, la investigación y el análisis. </p>



<p> <strong>API de Facebook</strong>: el diseño de la API actual impone enormes limitaciones a los investigadores, en lugar de permitirles descubrir lo que realmente está sucediendo en la plataforma. Las limitaciones en cada una de estas categorías, junto con los límites de la tasa de búsqueda, significa que los investigadores pueden tardar meses en evaluar los anuncios en una determinada región o en un determinado tema. </p>



<p> No es demasiado tarde para que Facebook arregle su API. Esperamos que actúen pronto. Y esperamos que organismos como la Comisión Europea examinen cuidadosamente las deficiencias de la herramienta. </p>



<p>Mozilla también realizará un análisis de la API de anuncios de Google cuando se publique en las próximas semanas. Debido a que la API del archivo de anuncios de Facebook no permite que los investigadores hagan su trabajo antes de las próximas elecciones al Parlamento Europeo, esperamos que Google intensifique y entregue una API que permita esta importante investigación. </p>