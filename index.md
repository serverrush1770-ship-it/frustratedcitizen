---
layout: home
title: Frustrated Citizen
subtitle: Questioning broken systems and explaining reality.
header-img: "https://serverrush1770-ship-it.github.io/frustratedcitizen/7a0e659f-5156-4daa-b41c-dcf9f4e30f46.jfif"
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
