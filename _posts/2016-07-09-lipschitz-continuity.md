---
layout: post
type: link
tag: ml, calculus
title: Lipschitz continuity
_url:
  - title: Lipschitz continuity
    type: fa-file-pdf-o
    uri: http://www.springer.com/cda/content/document/cda_downloaddocument/9783540008903-c1.pdf
    heart: <span style="color:#8bc34a" title="Simple and Best!"><i class="fa fa-thumbs-o-up" aria-hidden="true"></i></span>
---
This post contains links to the content on Lipschitz continuity.

{% for p in page._url %}
{% if p.heart %}
{% assign heart = p.heart %}
{% else %}
{% assign heart = '' %}
{% endif %}
{% if forloop.index == 1 %}
<span class="date" title="{{specialtitle}}" style="color:#{{specialcolor}}">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span> {{special}}<br/> <a href="{{ p.uri }}" target="_blank" style="line-height:1.5">{{ p.title }}</a> {{ heart }} <i class="fa {{ p.type }}" aria-hidden="true"></i>
{% else %}
<span class="date">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span> <br/> <a href="{{ p.uri }}" target="_blank" style="line-height:1.5">{{ p.title }}</a> {{ heart }} <i class="fa {{ p.type }}" aria-hidden="true"></i>
{% endif %}
{% endfor %}
