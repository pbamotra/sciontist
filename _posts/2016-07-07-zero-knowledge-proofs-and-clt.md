---
layout: post
type: link
tag: paper
title: Zero knowledge proofs and Central Limit Theorem
_url:
  - title: Zero Knowledge Proofs — A Primer
    type: fa-external-link
    uri: https://jeremykun.com/2016/07/05/zero-knowledge-proofs-a-primer/
    heart: <span style="color:#19B5FE" title="Fascinating stuff"><i class="fa fa-bolt" aria-hidden="true"></i></span>
  - title: Central Limit Theorem - It's sexy, so know it!
    type: fa-external-link
    uri: http://www.jeannicholashould.com/the-theorem-every-data-scientist-should-know.html
---
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
