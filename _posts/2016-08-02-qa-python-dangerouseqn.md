---
layout: post
type: link
publish: true
tag: ml, paper, python
title: Neural networks, Python
_url:
  - title: Composing Neural Networks for Question Answering
    uri: https://arxiv.org/pdf/1601.01705v4.pdf
    type: fa-file-pdf-o
  - title: How to Make Mistakes in Python
    uri: http://www.oreilly.com/programming/free/files/how-to-make-mistakes-in-python.pdf
    type: fa-file-pdf-o
    heart: <span title="Python Love" style="font-size:larger"><i class="icon-python"></i></span>
  - title: The Most Dangerous Equation
    uri: http://press.princeton.edu/chapters/s8863.pdf
    heart: <span style="color:#19B5FE" title="Fascinating stuff"><i class="fa fa-bolt" aria-hidden="true"></i></span>
---
The paper uses natural language strings to automatically assemble neural networks from a collection of composable modules. Coding violations in Python. The Most Dangerous Equation.

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
