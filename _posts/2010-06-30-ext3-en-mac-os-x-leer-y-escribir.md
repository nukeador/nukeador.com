---
ID: 554
post_title: 'Ext3 en Mac OS X: Leer y escribir'
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/30/06/2010/ext3-en-mac-os-x-leer-y-escribir/
published: true
post_date: 2010-06-30 22:39:34
---
Entrada rápida para no olvidar lo que me ha costado días encontrar.

Si necesitas acceder a un disco duro con particiones en formato ext2 o ext3 (típicos de GNU/Linux) necesitarás:
<ul>
	<li>Instalar <a href="http://code.google.com/p/macfuse">MacFUSE</a>.</li>
	<li> Instalar <a href="http://sourceforge.net/projects/fuse-ext2">fuse-ext2</a>.</li>
</ul>
Crear una carpeta para la particion en /Volumes:

<code><em>sudo mkdir /Volumes/midisco</em></code>

Montar la partición (puedes ver cómo se llama con <em>disktool -l</em>)

<code><em>sudo /usr/local/bin/fuse-ext2 /dev/nombredeldisco /Volumes/midisco/ -o force</em>
</code>

Si como a mi esto os lo montaba y no os dejaba escribir, tendréis que modificar un archivo de fuse-ext2, por lo que lo abrimos con un editor de textos y buscamos la función Mount().

<code><em>sudo vim /System/Library/Filesystems/fuse-ext2.fs/fuse-ext2.util</em></code>

La función Mount() debería tener lo siguiente:

<code>OPTIONS="auto_xattr,defer_permissions,rw+"</code>

Expulsad y volved a montar el disco.

<em><span style="color: #999999;">Fuentes: <a href="http://www.ericwingate.com/2009/09/27/mounting-ext3-in-snow-leopard/">ericwingate.com</a> y <a href="http://www.gearhack.com/Forums/DisplayComments.php?file=Computer/Mac%20OS/Read.Write_EXT2.EXT3_Volumes_on_Mac_OS_X">gearhack.com</a></span></em>