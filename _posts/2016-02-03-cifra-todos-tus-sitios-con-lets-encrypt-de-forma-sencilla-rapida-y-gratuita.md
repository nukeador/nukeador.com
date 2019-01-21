---
ID: 1554
post_title: 'Cifra todos tus sitios con Let&#8217;s Encrypt de forma sencilla, rápida y gratuita'
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/03/02/2016/cifra-todos-tus-sitios-con-lets-encrypt-de-forma-sencilla-rapida-y-gratuita/
published: true
post_date: 2016-02-03 23:48:54
---
Que la comunicación entre los usuarios y los sitios web viaje de forma segura, cifrada y no pueda ser interceptada por terceros debería ser algo obligatorio para todos los sitios.

Hasta hace muy poco el proceso para que los dueños de una página web para obtuvieran un certificado para cifrar sus webs (el famoso https) era un proceso, lento tedioso y en muchas ocasiones caro.
<p style="text-align: center;"><img class="aligncenter size-full wp-image-1559" src="https://www.nukeador.com/wp-content/uploads/2016/02/letsencrypt-logo-horizontal.png" alt="letsencrypt-logo-horizontal" width="339" height="81" /></p>
Hace unos meses se lanzó el proyecto <a href="https://letsencrypt.org/">Let's Encrypt</a>, el cuál Mozilla fue uno de los propulsores, cuyo objetivo es proporcionar a todo el mundo certificados para cifrar nuestros sitios web de forma <strong>gratuita y automática</strong>.

Si os fijáis este mismo blog usa ya https para todas las páginas, pero ¿cómo lo podéis hacer en vuestras webs?

<strong>Actualización (4/7/2016): </strong>El script de gestión de certificados ahora se llama <a href="https://certbot.eff.org/">certbot</a> y es mantenido por la EFF, toda la documentación actualizada <a href="https://certbot.eff.org/">en su web</a>. <span style="text-decoration: underline;">Las instrucciones a continuación están obsoletas</span>.

<a href="https://letsencrypt.org/howitworks/">La documentación de Let's Encrypt</a> es muy clara, pero voy a resumir.

En vuestro servidor como root bajamos letsencrypt si vuestro sistema no lo tiene aún y lo ejecutamos para que instale dependencias:
<pre>$ git clone https://github.com/letsencrypt/letsencrypt
$ cd letsencrypt
$ ./letsencrypt-auto --help
</pre>
Vamos a generar nuestro certificado, podemos generarlo e instalarlo de forma automática si usamos apache como dice la documentación, pero en mi caso como uso Nginx y el plugin aún no va fino he optado por hacerlo a mano, decirle que simplemente me genere nuevos certificados y que use un archivo en la raíz de la web para verificar que soy el propietario:
<pre>$ ./letsencrypt-auto certonly --webroot -w /var/www/nukeador.com/ -d nukeador.com -d www.nukeador.com
</pre>
<strong>Y ya está</strong>, tendremos nuestro certificado para el dominio <em>nukeador.com</em> y <em>www.nukeador.com</em> en la carpeta <em>/etc/letsencrypt/live/nukeador.com/</em> que podremos enlazar en la configuración de nuestro servidor web (si usáramos el plugin de apache esto lo haría él solo).

Posteriormente debemos programar una tarea diaria en el cron para que intente renovar el certificado si ha caducado (por defecto duran 3 meses) y recargar el servidor web para que lo tome. Simplemente lo puse en el cron como <em>@daily /ruta/al/script</em>
<pre>/root/letsencrypt/letsencrypt-auto certonly --keep-until-expiring --webroot -w /var/www/nukeador.com/ -d nukeador.com -d www.nukeador.com
service nginx reload
</pre>
Como veis es un proceso que cuesta 5 minutos y que nos tendremos que olvidar para siempre de renovaciones, pagos y dolores de cabeza.

¡Cifremos todas las web para asegurarnos que nuestra información y la de nuestros visitantes viaja segura!