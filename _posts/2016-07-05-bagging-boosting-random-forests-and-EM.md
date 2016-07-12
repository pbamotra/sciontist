---
layout: post
type: link
publish: true
title: Bagging, Boosting, Random forests, and EM
_url:
  - title: Bagging, Boosting, and Random forests
    type: fa-git
    uri: https://github.com/rasbt/python-machine-learning-book/blob/master/faq/bagging-boosting-rf.md
  - title: The EM Algorithm
    type: fa-file-pdf-o
    uri: https://www.cs.utah.edu/~piyush/teaching/EM_algorithm.pdf
tag: tutorial
---
This post contains links to the content on Bagging, Boosting, Random forests, and the EM algorithm.

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
