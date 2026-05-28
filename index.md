---
layout: default
---



# Welcome to Frustrated Citizen

A platform that questions systems, explains reality, and talks about the issues ordinary people face every day.

### Latest Articles:

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a> 
      <br>
      <small><em>Published on {{ post.date | date: "%B %d, %Y" }}</em></small>
    </li>
  {% endfor %}
</ul>
