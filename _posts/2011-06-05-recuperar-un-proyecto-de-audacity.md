---
ID: 754
post_title: Recuperar un proyecto de Audacity
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/05/06/2011/recuperar-un-proyecto-de-audacity/
published: true
post_date: 2011-06-05 22:28:46
---
<img class="alignright size-full wp-image-755" title="NEW_AudacityTransMediaWiki" src="http://www.nukeador.com/wp-content/uploads/2011/06/NEW_AudacityTransMediaWiki.png" alt="" width="155" height="135" />Puede que tengas la mala suerte de que el archivo de un proyecto en Audacity (.aup) se haya corrompido, pero que la carpeta con los datos nombre_data siga intacta.

En este caso también puede que tengas la mala suerte de usar Audacity 1.3 y no 1.2, por lo que las <a href="http://wiki.audacityteam.org/index.php?title=CrashRecovery">instrucciones de recuperación de la página de Audacity</a> no te valgan porque la forma de nombrar los archivos no es consecutiva.

Tras investigar, la única forma de recuperarlo es:
<ul>
	<li>Ordenar los archivos por fecha.</li>
	<li>Renombrar basándose en la fecha de más antiguo a más nuevo con el formato b001.au b002.au</li>
	<li>Utilizar una herramienta para unir los trozos y generar un archivo wav.</li>
</ul>
En detalle y para una grabación en mono y usando linux:

Nos creamos una carpeta y hacemos una copia exacta del directorio con los archivos .au

<code>mkdir recovery
cd recovery
cp -a /ruta_a_los_datos/miproyecto_data/e00/d03/ .</code>

Ordenamos por fecha y renombramos uno a uno siguiendo el patrón:

<code>n=1; ls -tr | while read i; do mv "$i" "b$(printf %03u $n).au"; n=$((n+1)); done</code>

Usando la <a href="http://www.mesw.de/audacity/recovery/">herramienta en python para la recuperación de Audacity</a>, le decimos la carpeta en la que hemos renombrado y le dejamos que nos genere un .wav

<em>Nota 1: Quizá necesites instalar el paquete python-wxgtk2.8 (cambia 2.8 por la última versión que haya disponible) para ejecutar la herramienta de recuperación en python.</em>
<em> Nota 2: Es posible que tengas que hacer el proceso con varias carpetas dentro de miproyecto_data.</em>

Y ya estaría, hemos recuperado algo que ya creíamos perdido :D<em>
</em>