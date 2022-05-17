---
title: "Luciana Lab - Publications"
layout: gridlay
excerpt: "Luciana Lab - Publications."
sitemap: false
permalink: /publications
---

## Highlights

{% assign number_printed = 0 %}
{% for publication in site.data.publications %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publication.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class=".well-lg">
  <pubtit>{{ publication.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/publications/{{ publication.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publication.description }}</p>
  <p><em>{{ publication.authors }}</em></p>
  <p><strong><a href="{{ publication.link.url }}">{{ publication.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publication.news1 }}</strong></p>
  <p> {{ publication.news2 }}</p>
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

## Full list of publications

{% for publication in site.data.publications %}

  {{ publication.title }} <br />
  <em>{{ publication.authors }} </em><br /><a href="{{ publication.link.url }}">{{ publication.link.display }}</a>

{% endfor %}
