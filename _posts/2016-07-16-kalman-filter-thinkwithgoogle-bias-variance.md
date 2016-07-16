---
layout: post
type: link
publish: true
tag: tutorial, tools
title: Kalman filters, google dataset website
_url:
  - title: Kalman filters and functional programming
    type: fa-external-link
    uri: http://www.johndcook.com/blog/2016/07/14/kalman-filters-and-functional-programming
    heart: <span><a class="notes" target="_blank" href="https://www.cl.cam.ac.uk/~rmf25/papers/Understanding%20the%20Basis%20of%20the%20Kalman%20Filter.pdf">$notes_1$</a></span>
  - title: Think with Google
    type: fa-external-link
    uri: https://www.thinkwithgoogle.com/data-gallery/
  - title: Understanding the Bias-Variance Tradeoff
    type: fa-external-link
    uri: http://scott.fortmann-roe.com/docs/BiasVariance.html
    heart: <span style="color:red" title="I love it!"><i class="fa fa-heart" aria-hidden="true"></i></span>
---
Rudolf E. Kálmán's Kalman filters are an exciting tool to infers parameters of interest from indirect, inaccurate and uncertain observations. Google launched a portal to access their data! A really good post on Bias-Variance Tradeoff.

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
