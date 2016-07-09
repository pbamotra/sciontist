---
layout: post
type: link
tag: ml, calculus
title: Lipschitz continuity
_url:
  - title: Lipschitz continuity
    type: fa-file-pdf-o
    uri: http://www.springer.com/cda/content/document/cda_downloaddocument/9783540008903-c1.pdf
    heart: <span style="color:#f9a825" title="Simple and Best!"><i class="fa fa-thumbs-o-up" aria-hidden="true"></i></span>
  - title: Pittsburghese - To be, or not to be
    type: fa-external-link
    uri: http://theglassblock.com/2016/07/07/pittsburghese-expertise-dropping-to-be/
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
---
This post contains links to the content on Lipschitz continuity from chapter 12.1 through 12.3 of Applied Mathematics: Body and Soul Volume 1 and mentions of the Pittsburghese dialect that doesn’t use the construction “to be” across the board!

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