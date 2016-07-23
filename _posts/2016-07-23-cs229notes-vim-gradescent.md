---
layout: post
type: link
publish: true
tag: tools, tutorial
title: Machine learning notes, Vim, Gradient descent
_url:
  - title: Stanford Machine Learning notes
    uri: http://www.holehouse.org/mlclass/
  - title: Vim commands visualized
    uri: http://vimgifs.com/
    type: fa-file-pdf-o
  - title: The Branchistochrone curve
    uri: http://fermatslibrary.com/s/brachistochrone-curve-the-problem-of-quickest-descent
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
