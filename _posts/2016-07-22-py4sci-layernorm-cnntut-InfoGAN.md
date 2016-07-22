---
layout: post
type: link
publish: true
tag: ml, python, tutorial
title: Python 3, Layer Normalization, CNN, InfoGAN
_url:
  - title: Python 3 for Scientists
    uri: http://python-3-for-scientists.readthedocs.io/en/latest/
  - title: Layer Normalization
    uri: http://arxiv.org/pdf/1607.06450.pdf
    type: fa-file-pdf-o
  - title: A Beginner's Guide To Understanding CNNs
    uri: https://adeshpande3.github.io/adeshpande3.github.io/A-Beginner's-Guide-To-Understanding-Convolutional-Neural-Networks/
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
  - title: InfoGAN - Representation Learning in GANs
    uri: https://arxiv.org/pdf/1606.03657v1.pdf
    type: fa-file-pdf-o
---


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
