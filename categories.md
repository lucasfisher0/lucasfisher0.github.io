---
layout: post
title: Categories
permalink: /cat/
---

<div id="category-switch-container">


  Page rendered with the <select id="skin-switch" onselect="test" style="overflow: auto;">
    {%- for category in site.categories %}
    <option value="{{ category | first }}">{{ category | first }}</option>
    {%- endfor %}
  </select> skin of Minima theme. {{ site.categories.length }}
  <i class="fa-regular fa-bell"></i>
</div>

<br/>
<select size="3" style="overflow: auto;">
  <option>Not Started</option>
  <option>In Progess</option>
  <option>Completed</option>
</select>

<script>
  const selectElement = document.querySelector(".ice-cream");
  const result = document.querySelector(".result");

  selectElement.addEventListener("change", (event) => {
    result.textContent = `You like ${event.target.value}`;
  });

</script>

<ul>
{% for category in site.categories %}
  <li><a name="{{ category | first }}">{{ category | first }}</a>
    <ul>
    {% for post in category.last %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>