---
layout: post
type: link
tag: ml
publish: true
title: Intro to neural networks, generative models, generative adversial nets
_url:
  - title: Hacker's guide to Neural Networks
    type: fa-external-link
    uri: http://karpathy.github.io/neuralnets/
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
  - title: Generative Models
    type: fa-external-link
    uri: https://openai.com/blog/generative-models/
  - title: Generative Adversarial Nets
    type: fa-file-pdf-o
    uri: http://arxiv.org/pdf/1406.2661v1.pdf
    heart: <span style="color:#19B5FE" title="Fascinating stuff"><i class="fa fa-bolt" aria-hidden="true"></i></span>
---
This post contains links to the content on short intro to neural networks by Andrej Karpathy, openAI's beautiful blog post on generative models, and Ian J. Goodfellow's paper on generative adversial networks. Pretty cool stuff.

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
