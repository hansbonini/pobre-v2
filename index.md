---
layout: default
---
{% assign posts = site.noticias | sort: 'date' %}
{% for post in posts reversed %}
<div class="container">
  <div class="row">
    <!-- Título da Notícia -->
    <div class="col-12">   
      <h2>{{ post.title }}</h2>
    <div>
  </div>
  <div class="row">
    <div class="col-3">
      <span>Por: {{ post.author }}</span>
    </div>
    <div class="col-5">
    </div>
    <div class="col-4">
      <span>Em: {{ post.date | date: "%d/%m/%Y" }} às {{ post.date | date: "%H:%M:%S" }}</span>
    </div>
  </div>
  <div class="row">
    <!-- Título da Notícia -->
    <div class="col-12">   
      <hr />
    <div>
  </div>
  <div class="row">
    <div class="col-12">
      {{ post.content }}
    </div>
  </div>
</div>
{% endfor %}
