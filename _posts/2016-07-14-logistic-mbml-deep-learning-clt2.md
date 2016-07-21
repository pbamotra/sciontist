---
layout: post
type: link
publish: true
tag: ml, tutorial
title: Logistic regression, model-based ML, tutorial deep learning, central limit theorem
_url:
  - title: Statistical interpretation of logit regression
    uri: https://ayearofai.com/rohan-6-follow-up-statistical-interpretation-of-logistic-regression-e78de3b4d938#.173dkkbrv
    heart: <span><a class="notes" target="_blank" href="http://karlrosaen.com/ml/notebooks/logistic-regression-why-sigmoid/">$notes_1$</a></span>
  - title: An Introduction to model-based machine learning
    uri: https://blog.dominodatalab.com/an-introduction-to-model-based-machine-learning/
  - title: Introduction to deep learning for image recognition
    type: fa-git
    uri: https://github.com/rouseguy/scipyUS2016_dl-image
  - title: Central Limit Theorem - Part 2
    uri: http://www.jeannicholashould.com/the-theorem-every-data-scientist-should-know-2.html
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
---
This post contains links to a detailed and lucid explanation on the inside-out working of logistic regression. There are also tutorials on model-based machine learning which I came across during spring 2016 in my probabilistic graphical models class with Prof. Erix Xing and Prof. Matt Gormley. The links also cover a introductory tutorial on deep learning for image recognition tasks which is borrowed from the SciPy US 2016 resources. The final link is continuation of a previous post of CLT. This is a must read. Enjoy.

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
