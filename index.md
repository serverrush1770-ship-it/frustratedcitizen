---
layout: home
title: Frustrated Citizen
subtitle: Questioning broken systems and explaining reality.
cover-img: "https://serverrush1770-ship-it.github.io/frustratedcitizen/7a0e659f-5156-4daa-b41c-dcf9f4e30f46.jfif"
---

<br>
<h1 style="text-align: center;">Welcome to Frustrated Citizen</h1>
<p style="font-size: 1.25rem; text-align: center; max-width: 800px; margin: 0 auto;">A platform that questions systems, explains reality, and talks about the issues ordinary people face every day.</p>

<style>
  /* Hide the default boring text list from Jekyll */
  .posts-list, .pagination { display: none !important; }

  /* Topic Cards Styling */
  .topics { padding: 40px 0px 50px 0px; }
  .card-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 20px; }
  .card { background: white; padding: 25px; border-radius: 8px; box-shadow: 0 4px 15px rgba(0,0,0,0.08); border-top: 4px solid #333; text-align: center; height: 100%; }
  .card-icon { font-size: 2.5rem; margin-bottom: 10px; }
  .card h3 { margin-top: 0; font-size: 1.2rem; color: #111; }
  .card p { font-size: 0.95rem; color: #555; margin-bottom: 0; }
  .card-link { text-decoration: none !important; color: inherit !important; display: block; transition: transform 0.2s; }
  .card-link:hover { transform: translateY(-5px); }

  /* Visual Image Grid for Latest 3 Articles */
  .article-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 20px; margin-top: 20px; }
  .article-card { background: white; border-radius: 8px; overflow: hidden; box-shadow: 0 4px 15px rgba(0,0,0,0.08); transition: transform 0.2s; }
  .article-card:hover { transform: translateY(-5px); }
  .article-img { width: 100%; height: 180px; object-fit: cover; border-bottom: 3px solid #333; }
  .article-content { padding: 15px; text-align: center; }
  .article-title { margin: 0 0 10px 0; font-size: 1.1rem; color: #111; font-weight: bold; line-height: 1.3;}
  .article-date { font-size: 0.85rem; color: #777; margin: 0; }
</style>

<section class="topics">
  <div class="card-container">
    <a href="/frustratedcitizen/current-affairs" class="card-link"><div class="card"><div class="card-icon">📰</div><h3>Current Affairs</h3><p>Breaking down important news and public policies.</p></div></a>
    <a href="/frustratedcitizen/ai" class="card-link"><div class="card"><div class="card-icon">🤖</div><h3>Artificial Intelligence</h3><p>Understanding how AI is changing society and jobs.</p></div></a>
    <a href="/frustratedcitizen/economy" class="card-link"><div class="card"><div class="card-icon">📉</div><h3>Economy & Markets</h3><p>Simple explanations of economic issues affecting citizens.</p></div></a>
    <a href="/frustratedcitizen/education" class="card-link"><div class="card"><div class="card-icon">🎓</div><h3>Education</h3><p>Discussing student struggles and shifting systems.</p></div></a>
  </div>
</section>

<br><br>
<h2 style="text-align: center; border-bottom: 2px solid #333; padding-bottom: 10px; max-width: 300px; margin: 0 auto;">Latest Articles</h2>

<div class="article-grid">
  {% for post in site.posts limit:3 %}
  <div class="article-card">
    <a href="{{ post.url | prepend: site.baseurl }}" class="card-link">
      {% if post.thumbnail-img %}
        <img src="{{ post.thumbnail-img }}" alt="{{ post.title }}" class="article-img">
      {% else %}
        <img src="https://serverrush1770-ship-it.github.io/frustratedcitizen/7a0e659f-5156-4daa-b41c-dcf9f4e30f46.jfif" alt="{{ post.title }}" class="article-img">
      {% endif %}
      <div class="article-content">
        <h3 class="article-title">{{ post.title }}</h3>
        <p class="article-date">{{ post.date | date: "%B %-d, %Y" }}</p>
      </div>
    </a>
  </div>
  {% endfor %}
</div>
