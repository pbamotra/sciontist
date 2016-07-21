---
layout: post
type: link
publish: true
tag: tutorial, ml
title: Probabilistic Filters - Cuckoo and Bloom, Unreasonable Effectiveness of Counting
_url:
  - title: Probabilistic Filters By Example
    uri: https://bdupras.github.io/filter-tutorial
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
  - title: Unreasonable Effectiveness of Counting
    uri: https://medium.com/@plusepsilon/unreasonable-effectiveness-of-counting-cf18d15f5a43#.c0mgkwtyq
  - title: Number plate recognition with Tensorflow
    uri: https://matthewearl.github.io/2016/05/06/cnn-anpr/
---
Probabilistic Filters discussion on Cuckoo filters introduced by researchers at Carnegie Mellon and the traditional Bloom filters. There's discussion on effective use of counting in ML algorithms which is essential in algorithms like Naive Bayes. Finally, there is an application of CNNs to recognize number plates on vehicles using Tensorflow.

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
