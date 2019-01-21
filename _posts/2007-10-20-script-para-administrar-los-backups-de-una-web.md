---
ID: 141
post_title: >
  Script para administrar los backups de
  una web
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/20/10/2007/script-para-administrar-los-backups-de-una-web/
published: true
post_date: 2007-10-20 20:42:56
---
<p>He creado un bash script que permite, mediante ssh, administrar las copias de seguridad de la base de datos y archivos de una web muy fácilmente y que en combinación con tareas programadas cron puede ser muy potente.</p>
<p>¿Qué nos permite hacer este script?</p>
<p><strong>Base de datos</strong></p>
<ul>
<li>Hacer un backup de la base de datos y guardarla comprimida en el servidor (admin_server.sh -b)</li>
<li>Hacer un backup de la base de datos y sincronizar descargándola a la carpeta local de backups (admin_server.sh -c)</li>
<li>Sincronizar los backups de la base de datos descargándola a la carpeta local de backups (admin_server.sh -s)</li>
</ul>
<p><strong>Archivos</strong></p>
<ul>
<li>Descargar todos los cambios de los archivos del servidor de forma incremental (admin_server.sh -d)</li>
<li>Enviar los cambios de la carpeta local al servidor (por seguridad no se enviarán los cambios a los archivos borrados) (admin_server.sh -e)</li>
</ul>
<p>El script puede usarse de forma interactiva si ejecutamos solo admin_server.sh, con un menú numérico con las opciones o mediante los argumentos descritos anteriormente (ideal para usar en tareas programadas cron).</p>
<p>En el archivo encontrareis un archivo de texto llamado Instrucciones con toda esta información.</p>
<p class="download"><a href="/archivos/admin_server_scripts.tar.bz2">Descargar admin_server_scripts.tar.bz2</a></p>
<p>El script está bajo licencia <a title="GPL v3" href="http://www.gnu.org/licenses/gpl.txt" hreflang="en">GPL v3 o superior</a>, por lo que puede ser modificado fácilmente para hacer backups de otro tipo de servidores.</p><p>Tip: Crea tus tareas programadas cron con <a title="¿Conocias crontab y gnome-schedule?" href="http://tuxpepino.wordpress.com/2007/05/16/%c2%bfconocias-crontab-y-gnome-schedule/">gnome-schedule</a> ;)</p>