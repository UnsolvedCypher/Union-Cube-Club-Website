---
title: Delegate Biographies
layout: page
permalink: /biographies/
---

Delegate Biographies
====================

{% for delegate in site.delegates %}

{{ delegate.name}} ({{ delegate.location }})
--------------------------------------------

<div class="row">
    <div class="col-md-10">
        {% if delegate.useblack %}
            <p class="well delegatebioblack" style="background-color: #{{ delegate.color }};">
        {% else %}
            <p class="well delegatebio" style="background-color: #{{ delegate.color }};">
            
        {% endif %}
                {{ delegate.description }}
            </p>
    </div>
    <div class="col-md-2" style="text-align:center;">
        <img src="../img/{{ delegate.name | remove: ' ' }}.jpg" height="128" width="128" alt="{{ delegate.name }}">
        <h3>
            <a href="https://www.worldcubeassociation.org/results/p.php?i={{ delegate.wca }}">
                [{{ delegate.wca }}]
            </a>
        </h3>
    </div>
</div>

{% endfor %}