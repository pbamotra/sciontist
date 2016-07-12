---
layout: post
type: link
publish: false
tag: ml
title: DNNs with stochastic depth, batch normalization, covariate shift correction
_url:
  - title: Deep Networks with Stochastic Depth
    type: fa-file-pdf-o
    uri: https://arxiv.org/pdf/1603.09382v2.pdf
  - title: Batch Normalization:
    type: fa-file-pdf-o
    uri: http://arxiv.org/pdf/1502.03167v3.pdf
---
This post contains links to the latest advances on deep networks in terms of stochastic depth that behaves like dropouts, but the whole layer is dropped stochastically. Batch normalization by Ioffe and Szegedy is yet another popular concept when it comes to DNNs. The discussion in the batch normalization links is about covariate shift correction which is a simple yet very effective technique in networks containing a lot of layers.

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