---
title: "WCSNG Lab - Research"
layout: textlay
excerpt: "WCSNG Lab -- Research"
sitemap: false
permalink: communication
---
<a href="{{ site.url }}{{ site.baseurl }}/research"><img src="{{ site.url }}{{ site.baseurl }}/images/back.png" class="img-responsive" width="4%" /> </a>

# Wireless Communications
####  This page contains papers related to `Wireless Communications`. Go back to other <a href="{{ site.url }}{{ site.baseurl }}/research"> <b>Research</b></a> categories or see full list of <a href="{{ site.url }}{{ site.baseurl }}/publications"> <b>Publications</b></a>.


<p> &nbsp; </p>
{% assign number_printed = 0 %}
{% for publi in site.data.publist %}
{% if publi.tag1=='communication' or publi.tag2=='communication'  %}

{% assign even_odd = number_printed | modulo: 2 %}


{% if even_odd == 0 %}
<div class="row">
{% endif %}


<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="60%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>


{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}


{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>