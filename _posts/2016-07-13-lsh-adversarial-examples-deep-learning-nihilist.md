---
layout: post
type: link
publish: true
tag: ml, tutorial, life
title: Nearest neighbors, Adversarial examples, lectures on deep learning, guide to meaning
_url:
  - title: Large scale nearest neighbors using LSH
    uri: https://gab41.lab41.org/nearest-neighbors-at-scale-e55a8d02b16b#.spl95fwkm
  - title: Adversarial examples in the physical world
    type: fa-file-pdf-o
    uri: http://arxiv.org/pdf/1607.02533.pdf
    heart: <span style="color:#19B5FE" title="Fascinating stuff"><i class="fa fa-bolt" aria-hidden="true"></i></span>
  - title: Quoc Le’s lectures on deep learning
    uri: http://www.trivedigaurav.com/blog/quoc-les-lectures-on-deep-learning/
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span> <span title="Lectures"><i class="fa fa-television" aria-hidden="true"></i></span>
  - title: A nihilist's guide to meaning
    uri: http://www.meltingasphalt.com/a-nihilists-guide-to-meaning/
---
This post contains links to the nearest neighbors algorithms scaled to retrieve millions of images using Locally Sensitive Hashing. Adversarial examples paper by Kurakin, Goodfellow, and Bengio show how to construct examples that can trick neural networks to perform bad. There's also link to Quoc Le (Goole Brain) lectures on deep learning delivered at Carnegie Mellon University in 2014. Finally we meltingasphalt post on the primordial question - What's my purpose?

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
