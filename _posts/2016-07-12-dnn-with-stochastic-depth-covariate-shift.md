---
layout: post
type: link
publish: true
tag: ml
title: DNNs with stochastic depth, batch normalization, covariate shift correction
_url:
  - title: Deep Networks with Stochastic Depth
    type: fa-file-pdf-o
    uri: https://arxiv.org/pdf/1603.09382v2.pdf
    heart: <span><a class="notes" target="_blank" href="https://gab41.lab41.org/lab41-reading-group-deep-networks-with-stochastic-depth-564321956729">$notes_1$</a></span>
  - title: Batch Normalization
    type: fa-file-pdf-o
    uri: http://arxiv.org/pdf/1502.03167v3.pdf
    heart: <span><a class="notes" target="_blank" href="https://gab41.lab41.org/batch-normalization-what-the-hey-d480039a9e3b">$notes_1$</a>&nbsp;<a class="notes" target="_blank" href="http://blog.smola.org/post/4110255196/real-simple-covariate-shift-correction">$notes_2$</a></span>
  - title: Friendship and natural selection
    uri: http://www.pnas.org/content/111/Supplement_3/10796.long
    heart: <span style="color:#19B5FE" title="Fascinating stuff"><i class="fa fa-bolt" aria-hidden="true"></i></span>
  - title: Altair - statistical <i>viz lib</i> for Python
    type: fa-git
    uri: https://github.com/ellisonbg/altair
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span> <span title="Visualisation!"><i class="fa fa-eye" aria-hidden="true"></i></span>
---
This post contains links to the latest advances on deep networks in terms of stochastic depth that behaves like dropouts, but the whole layer is dropped stochastically. Batch normalization by Ioffe and Szegedy is yet another popular concept when it comes to DNNs. The discussion in the batch normalization links is about covariate shift correction which is a simple yet very effective technique in networks containing a lot of layers.

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
