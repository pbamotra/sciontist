---
layout: post
type: link
publish: true
tag: ml, tutorial
title: Q Learning, Tensorflow, Generative Adversial Networks
_url:
  - title: Empirical Risk for Non-convex Losses
    uri: http://arxiv.org/pdf/1607.06534v2.pdf
    type: fa-file-pdf-o
  - title: Skynet Salesman
    uri: http://multithreaded.stitchfix.com/blog/2016/07/21/skynet-salesman/
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
  - title: Generative Adversarial Nets in TensorFlow
    uri: http://blog.evjang.com/2016/06/generative-adversarial-nets-in.html
---

[Stitchfix] In QQ learning, the aim is to learn a QQ function which gives the expected future reward (think score) given the current state (pixels from Pac-Man) if a particular action (up, down, etc.) is taken.
The paper discusses exploiting problem structure to learn a noisy linear classifier with non-convex loss.
[Evjang] The tutorial is on implementing Ian Goodfellow's Generative Adversarial Nets paper in TensorFlow.
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
