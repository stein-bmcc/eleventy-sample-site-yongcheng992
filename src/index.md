---
title: Home
layout: base.njk
tags: navItem
---
# {{title}}

My Home Page!
This is the home page. Replace this with your text.

<div class="projects">
    <div class="project"></div>
</div>

## photos
<ul>
{% for page in collections.photo %}
<li>
    <a href="{{ page.url }}"> {{ page.data.title }}</a>
</li>
{% endfor %}
</ul>

<a href="blah.html">My page</a>

## design

<main class="design cards">
    <h2 class="cards_header">Graphic Design Projects</h2>
    {%- for page in collections.design %}
    <div class="pjcard">
      <div class="card_img">
          <a href="{{page.url}}"><img src="/images/{{page.data.postImg}}" alt="{{page.data.postImgAlt}}"></a></div>
      <div class="card_text">
        <h3><a href="{{page.url}}">{{page.data.title}}</a></h3>
        <p>{{page.data.description}}<p>
      </div>
    </div> 
    </div>
    {%- endfor %}
</main>