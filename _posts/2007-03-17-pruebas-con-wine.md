---
ID: 106
post_title: Pruebas con wine
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/17/03/2007/pruebas-con-wine/
published: true
post_date: 2007-03-17 20:22:46
---
Tras un reciente problema con mi antiguo disco duro, tuve que salvar todos los datos a uno nuevo (el cual, espero que no me falle también). Como había bajado recientemente la nueva versión preliminar del próximo Ubuntu 7.04 me animé a instalarlo para usarlo como sistema en producción. Una de las ventajas que tuve fue que como tengo una partición para el directorio <em>/home</em>, no me costo nada instalar la nueva Ubuntu en la otra partición y decirle que usara el <em>/home</em> que tenía antes, con mis datos y configuraciones.

Una de las cosas que también he probado es la nueva versión de <a href="http://es.wikipedia.org/wiki/Wine">wine</a>, la API que nos permite ejecutar programas de Windows en GNU/Linux.

Como tenía muchas ganas de usar el cliente de bittorrent µTorrent, y aun no está disponible para Linux me dispuse a ejecutarlo con wine.

<img src="http://upload.wikimedia.org/wikipedia/en/thumb/3/37/WINE-Logo.png/48px-WINE-Logo.png" border=0 alt="Wine" /> <strong>Instalamos Wine</strong>

Lo primero añadimos el repositorio de wine (desde <em>Sistema - Administración - Orígenes del software</em>, Software de terceros):

<code>deb http://wine.budgetdedicated.com/apt edgy main</code>

Y posteriormente desde Synaptic o "Añadir y quitar" instalamos wine.

Antes de nada lo que hice fue bajar el <a href="http://www.deviantart.com/download/18777943/">tema para windows Clearlook</a> y aplicárselo a wine para que se vean los programas bien y no con un estilo windows 98 horrible. Lo único que tenemos que hacer es decirle desde <em>"Desktop Integration"</em> del Wine Configurator (<em>Sistema - Preferencias - Wine Configurator</em>) que quieres instalar un tema y elegir el archivo <em>.msstyles</em> que viene en el tema.

<img src="http://upload.wikimedia.org/wikipedia/en/6/6c/%CE%9CTorrent_icon.png" border=0 alt="µTorrent" /> <strong>Instalamos µTorrent </strong>

Una vez hecho esto bajamos el <a href="http://www.utorrent.com/download.php">µTorrent</a> y <a href="http://www.utorrent.com/download/langpacks/dl.php?build=488">el archivo de idioma</a> y lo metemos en una carpeta llamada utorrent que crearemos en nuestra carpeta personal.

¡Y ya está! Ahora podremos ejecutarlo con un simple doble clic (yo tuve que renombrar el ejecutable y quitarle el .exe del nombre) e incluso podemos configurar nuestros archivos .torrent para que se abran por defecto con él.

<a href="/images/utorrent-ubuntu.jpg" rel="lightbox"><img src="/images/utorrent-ubuntu-mini.jpg" border=0 alt="µTorrent en Ubuntu" /></a>

También he estado trasteando con esta nueva versión de wine y el juego <a href="http://www.wow-europe.com/es/">World Of Warcraft</a>, de momento no he conseguido mejores resultados que con <a href="http://es.wikipedia.org/wiki/Cedega">Cedega</a> pero todo se andará.