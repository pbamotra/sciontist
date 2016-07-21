---
layout: post
type: link
publish: true
tag: ml
title: Tips for training deep networks
_url:
  - title: Practical tips for training deep networks
    uri: http://arxiv.org/pdf/1206.5533v1.pdf
    type: fa-file-pdf-o
  - title: Notes on Big-n Problems
    uri: https://www.cs.ubc.ca/~schmidtm/Documents/2012_Notes_BigN.pdf
    type: fa-file-pdf-o
  - title: The Four Burners Theory
    uri: http://jamesclear.com/four-burners-theory
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
---
Paper by Yoshua Bengio on Practical Recommendations for Gradient-Based Training of Deep Architectures. There's link to Mark Schmidt excellent notes on  on Big-n Problems which serves a good background to optimization problems around us. Finally, there's a link to thought-provoking article on Work-Life Balance by James Clear.

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
