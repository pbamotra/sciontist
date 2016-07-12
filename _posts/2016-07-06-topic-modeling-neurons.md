---
layout: post
type: link
publish: true
datespecial: ''
specialcolor: 029142
specialtitle: Eid Mubarrak
title: Topic modeling, Neurons, and stuff to ponder
_url:
  - title: Five minute introduction to topic modeling
    type: fa-external-link
    uri: http://www.kdnuggets.com/2016/07/text-mining-101-topic-modeling.html
  - title: Probabilistic topic modeling - David M. Blei
    type: fa-file-pdf-o
    uri: http://www.cs.columbia.edu/~blei/papers/Blei2012.pdf
  - title: Neurons gone wild
    type: fa-external-link
    uri: http://www.meltingasphalt.com/neurons-gone-wild/
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
tag: tutorial
---
This post contains links to the content on topic modeling and the Melting Asphalt's Neurons gone wild.

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
