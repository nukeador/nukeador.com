---
ID: 309
post_title: Asegurando nuestros datos y contraseñas
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/11/04/2009/asegurando-nuestros-datos-y-contrasenas/
published: true
post_date: 2009-04-11 02:36:00
---
<img class="alignright" title="Seguridad" src="http://www.iconfinder.net/data/icons/Futurosoft%20Icons%200.5.2/128x128/mimetypes/encrypted.png" alt="" width="128" height="128" />

Una buena forma de asegurar nuestros datos o archivos con contraseñas en almacenarlas cifradas, y para esto mismo no hay método más cómodo y seguro que usar <a href="http://es.wikipedia.org/wiki/TrueCrypt">TrueCrypt</a>.

¿Qué nos permite hacer?
<ul>
	<li>Crear un archivo cifrado que contenga todos los datos que queramos dentro.</li>
	<li>Cifrar completamente una partición, un disco duro entero o dispositivo externo USB (incluso el sistema operativo completo).</li>
	<li>Posibilidad de crear volúmenes ocultos, esto es, que se crean dos partes cifradas, una con una contraseña de pega y otra con la buena. De esta forma, si te forzaran a desvelar la contraseña maestra no podrían saber si lo que están viendo es la parte real o no.</li>
	<li>Posibilidad de usar keyfiles, lo que significa que además de saber la contraseña, tendremos que disponer de un archivo en concreto para abrir el volumen.</li>
	<li>Altos niveles de seguridad usando algoritmos de cifrado muy fuertes.</li>
</ul>
La ventaja de todo esto es que por ejemplo, puedes crear un USB externo cifrado, enchufarle, decirle a TrueCrypt la contraseña  y trabajar con él normalmente.

Si ya te he convencido, pásate por <a href="http://www.genbeta.com/default/truecrypt-50-lo-probamos">el tutorial que hicieron en Genbeta</a> sobre cómo usarlo (bastante fácil para todo tipo de públicos).

Como curiosidad, pongo un posible caso de alta seguridad para datos:
<ul>
	<li>Usaríamos un dispositivo USB externo donde crear el volumen cifrado.</li>
	<li>Crearíamos un volumen oculto para que incluso si nos torturan, daríamos la clave de la parte falsa que contiene otros datos que no sabrían si son los verdaderos.</li>
	<li>Usaríamos la opción keyfile, generando un archivo aleatorio que nos pediría a la hora de abrir el volumen, este archivo lo almacenaríamos en otro UBS que guardaríamos en una ubicación diferente al que contiene los datos.</li>
	<li>Utilizaríamos los algoritmos más potentes que TrueCrypt nos ofrece, aunque perdamos velocidad de escritura.</li>
	<li>Usaríamos una contraseña maestra muy larga con mayúsculas y números.</li>
</ul>
De esta forma para poder acceder a nuestros datos deberíamos saber la contraseña maestra (la buena, no la falsa) y tener el archivo exacto con nosotros (keyfile). Como veis este sistema de seguridad es muy recomendable y altamente seguro, tanto para el uso en casa como en la empresa.

<a href="http://es.wikipedia.org/wiki/TrueCrypt">Más información sobre TrueCrypt en Wikipedia</a>.