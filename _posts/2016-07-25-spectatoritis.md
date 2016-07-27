---
layout: post
type: link
publish: true
tag: life, wow
title: The Rise of Spectatoritis
_url:
  - title: The Rise of Spectatoritis
    uri: http://www.artofmanliness.com/2011/08/28/viewers-vs-doers-the-rise-of-spectatoritis/
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
---
Viewers vs. Doers

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
