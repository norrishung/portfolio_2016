---
layout: default
permalink: 'writing/'
title: Writing
---
<div class="blog">
    <header>
        <h1>Writing</h1>
    </header>
    <ul>
        {% for post in site.categories.writing %}
        <li>
            <h3><a href="{{ post.url }}">{{post.title}}</a></h3>
            <p>{{ post.description }}</p>
        </li>

        {% endfor %}
    </ul>
</div>
