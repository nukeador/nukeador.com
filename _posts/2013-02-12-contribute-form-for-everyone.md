---
ID: 1079
post_title: Contribute form for everyone!
author: Nukeador
post_excerpt: ""
layout: post
permalink: >
  https://www.nukeador.com/12/02/2013/contribute-form-for-everyone/
published: true
post_date: 2013-02-12 13:17:34
---
<a href="http://www.mozilla.org/contribute"><img class="aligncenter size-medium wp-image-1082" alt="contribute" src="http://www.nukeador.com/wp-content/uploads/2013/02/contribute-300x225.png" width="300" height="225" /></a>

In the last months a lot of work has been done on the <a href="http://www.mozilla.org/contribute/">Mozilla.org contribute page</a> to improve its functionality in terms of localization.
<ul>
	<li><strong>Localization</strong>: Having the content in your language was the first step. (You can ask support for your locales filling a bug under mozilla.org L10n blocking <a href="https://bugzilla.mozilla.org/show_bug.cgi?id=755351">bug 755351</a>)</li>
	<li><strong>Local email</strong>: The information filled in the form was sent to the contributor engagement team and also to the person in charge of volunteer involvement in each functional area. Obviously they handle requests in English, so for localized inquiries we needed this emails to be sent to local communities, we can now define an email where to get these inquiries, in our case is the Mozilla Hispano mentors.</li>
	<li><strong>Auto-responses</strong>: Some areas in English had auto-responses defined when a new person sends the form. Having this localized is super import because you can define you own template based on your procedures to on-board volunteers, and you can handle much more people this way giving them important information on how to get involved in a particular area right away.</li>
	<li><strong>Embeddable form</strong>: The last piece was being able to <a href="http://www.mozilla.org/contribute/embed/">embed the form</a> on external sites using an iframe, so we can offer a consistent way to get involved in mozilla not matter where people get to us (Thanks Ricky!). We have already implemented it on <a href="https://www.mozilla-hispano.org/documentacion/Colabora">our contribute page at Mozilla Hispano</a>.</li>
</ul>
Code example to include the form on your site (remember to customize callback url to your site's url)

<code>&lt;iframe width="500" height="550" frameborder="0" src="https://www.mozilla.org/contribute/embed/?callbackurl=http://yousitehere.com" marginheight="0" marginwidth="0"&gt;Loading...&lt;/iframe&gt;</code>

<strong>Why all of this is important?</strong>

Providing a central way to get people involved with Mozilla in their language is very important, keep in mind that for Spanish we are getting more than 100 inquiries per week. We should be able to track and answer everyone.

<strong>How does it work for you?</strong>

<a href="https://www.mozilla-hispano.org/documentacion/Colabora"><img class="aligncenter size-medium wp-image-1083" alt="colabora" src="http://www.nukeador.com/wp-content/uploads/2013/02/colabora-300x221.png" width="300" height="221" /></a>

<strong>Update: In September 2013 <a title="On-boarding rethought" href="http://www.nukeador.com/03/10/2013/on-boarding-rethought/">we modified the procedure based on our experience</a> to be able to handle a big amount of inquires, please check that instead.</strong>

The process for Mozilla Hispano is the following:
<ul>
	<li>Someone uses the form in Spanish (from mozilla.org/contribute or our contribute page)</li>
	<li>We get a notification at our mentor's email alias.</li>
	<li>The person gets an auto-response, with different links (all with information in Spanish) depending on the area of interest. Here it's important to note that <strong>this email tells people to read a few links with information</strong> about how to get involved (area description, link to contribute forum...) and to <strong>answer when they are ready to start</strong> (reply-to header is defined to our mentor's alias).</li>
	<li>It's impossible to handle more than 100 inquiries per week if you have to manually answer everyone, so we wait till the person reads the initial information and answer the auto-response email to assign him a mentor.</li>
	<li>Keep in mind that we tell people in the template <strong>they can contribute to mozilla even if they don't have a lot of time</strong>, we observed that most people didn't answer this first auto-response because they were not sure if they were going to be able to handle it.</li>
	<li>If the person answers, a mentor is assigned and he follows <a href="http://www.nukeador.com/26/07/2012/organising-a-mozilla-community-ii/">our procedure for on boarding new contributors</a>.</li>
</ul>
<strong>Next steps</strong>

In the future we will be able to track inquiries directly from a tracking system at mozilla.org, so we won't have to deal with a lot of emails and shared spreadsheets to track new contributors progress.

Now we are able to embed the form in our language in more places, event pages, reps portal...

We need to get more awareness about <strong>how important on-boarding volunteers is for the future of mozilla</strong>, currently we have to literally beg most of the times for resources to improve and help community builders or wait till someone has free time to help.

<strong>Volunteers are the fuel for moving the project <strong>forward</strong>, give them some love please! ;)</strong>