---
layout: post
type: link
publish: true
tag: tutorial, tools, ml
title: Docker, Deep Learning, Are we there yet?
_url:
  - title: Docker for beginners
    uri: http://prakhar.me/docker-curriculum
  - title: Topics Course on Deep Learning
    uri: http://joanbruna.github.io/stat212b
  - title: Unsupervised Feature Learning and Deep Learning
    uri: http://ufldl.stanford.edu/tutorial/
  - title: Are we there yet?
    uri: http://rodrigob.github.io/are_we_there_yet/build/
---
Introduction to dockers and link to Stat212b from UC Berkeley Topics Course on Deep Learning. There's a tutorial to teach the main ideas of Unsupervised Feature Learning and Deep Learning by Stanford University. Finally, there's link to **Are we there yet?**, a crowd sourced list of known result one some of the “major” visual classification, detection, and pose estimation datasets.

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
