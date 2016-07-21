---
layout: post
type: link
publish: true
tag: tutorial, tools
title: Jupyterlab, bitbucket git, tools for thought
_url:
  - title: JupyterLab - computational environment for Jupyter
    type: fa-git
    uri: https://github.com/jupyter/jupyterlab
  - title: Bitbucket - Becoming a git guru
    uri: https://www.atlassian.com/git/tutorials
  - title: Tools for thought
    uri: https://acko.net/files/gltalks/toolsforthought
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
---
Jupyter has launched Jupyter labs which is in-browser computational environment. Looks like a full-fledged code editor to me. Terminal included! There a link to awesome and simple tutorial on git usage by atlassian. Finally there's an extraordinarily beautiful presentation by Steven Wittens on MathBox -
Tools for Thought Graphical Algebra and Fourier Analysis.

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
