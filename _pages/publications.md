---
title: "Publications"
layout: gridlay
excerpt: "TESLab - Publications"
sitemap: false
permalink: /publications/
---

# Publications

The full list of publications and patents is given below this page, they are also accessible on Prof. Hakan Erturk's <a href="https://scholar.google.com/citations?user=0bWMg2kAAAAJ&hl=en">Google Scholar</a> profile.

# Group highlights

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
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

# Patents

Microfins for Cooling an Ultramobile Device <br />  <em>Z. Li, C.-C. Hsieh, J. Hu, H. Erturk, and G. Chen</em><br /> <a href="https://drive.google.com/open?id=0B1x_zKlyTDidUGZFMldabzBNbEU">US8482922 (2013)</a>

# Full list of publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}