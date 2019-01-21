---
ID: 112
post_title: MySQL desde OpenOffice
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/29/03/2007/mysql-desde-openoffice/
published: true
post_date: 2007-03-29 18:38:04
---
<div style="margin: auto; text-align: center"><img src="http://www.methodlab.ru/technology/img/mysql.gif" alt="MySQL DataBase" /></div>

Es interesante tener a nuestro alcance el mayor numero de utilidades posible para realizar una misma tarea, y en este caso vamos a hablar de las bondades de el <strong>gestor de bases de datos <a href="http://es.wikipedia.org/wiki/OpenOffice.org_Base">OpenOffice Base</a></strong>. Este a falta de tener que envidiar algo a su homónimo privativo (MS Access), es más bien todo lo contrario, porque <strong>acepta gran multitud de bases de datos</strong>. Adabas D, ADO, Microsoft Access, MySQL... o cualquier otra usando los conectores ODBC y JDBC (por ejemplo Oracle a partir de OO 2.2).

De lo que vamos a hablar, es de la <strong>gestión de una base de datos MySQL</strong> (montada en nuestro servidor o remota) <strong>mediante Base</strong>, lo cual está orientado no a un administrador, ya que existen otras herramientas como <a href="http://es.wikipedia.org/wiki/OpenOffice.org_Base">MySQL Query Browser</a> sino a una persona de a pie que tenga que insertar datos en una base de datos de una oficina, casa... etc acostumbrada a usar programas de gestión de bases de datos sin saber sintaxis SQL.

Para ello necesitamos el <a href="http://es.openoffice.org/programa/index.html">OpenOffice</a>, <a href="http://www.java.com/es/download/manual.jsp">Java JRE</a> y el <a href="http://dev.mysql.com/downloads/connector/j/5.0.html">conector JDBC para Mysql</a>. En GNU/Linux lo más probable es que ya tengáis OpenOffice instalado, solo tendréis que instalar el paquete <em>sun-java5-jre</em> y <em>libmysql-java</em>.

Abriremos OpenOffice y en <em>Herramientas - Opciones - Java</em> configuraremos como predeterminado el de Sun. Reiniciamos OpenOffice y en el mismo menú anterior, damos Agregar y seleccionamos el conector JDBC (un archivo .jar). Si instalaste el conector desde los repositorios no te hará falta seleccionarlo.

Ahora <strong>podremos conectar desde Base a una base de datos MySQL local o remota</strong>, teniendo la precaución de seleccionar la conexión a MySQL mediante JDBC.

Vía // <a href="http://ardentice.wordpress.com/2007/03/28/conectando-openofficeorg-a-mysql/">Memoria Compartida</a>