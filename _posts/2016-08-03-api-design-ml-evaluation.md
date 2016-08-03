---
layout: post
type: link
publish: true
tag: tutorial
title: API design
_url:
  - title: The Little Manual of API Design
    uri: http://www4.in.tum.de/~blanchet/api-design.pdf
    type: fa-file-pdf-o
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
  - title: Evaluating Machine Learning Models
    uri: http://www.oreilly.com/data/free/files/evaluating-machine-learning-models.pdf
    type: fa-file-pdf-o
  - title: Design Patterns Reference Card
    uri: http://www.mcdonaldland.info/files/designpatterns/designpatternscard.pdf
    type: fa-file-pdf-o
---
API Design, methods to evaluate machine leaning (ML) models, and Design Patterns Reference Card.

{% for p in page._url %}
{% if p.heart %}
{% assign heart = p.heart %}
{% else %}
{% assign heart = '' %}
{% endif %}
{% if forloop.index == 1 %}
<span class="date" title="{{specialtitle}}" style="color:#{{specialcolor}}">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span> {{special}}<br/> <a href="{{ p.uri }}" target="_blank" style="line-height:1.5">{{ p.title }}</a> <i class="fa {{ p.type }}" aria-hidden="true"></i> {{ heart }}
{% else %}
<span class="date">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span> <br/> <a href="{{ p.uri }}" target="_blank" style="line-height:1.5">{{ p.title }}</a> <i class="fa {{ p.type }}" aria-hidden="true"></i> {{ heart }}
{% endif %}
{% endfor %}
