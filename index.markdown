---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Projects
---

<h1>Projects</h1>

<div class="projects-grid" style="display:grid;gap:1rem;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));">
  {% for p in site.data.projects %}
  <a href="{{ p.demo | default: p.url }}" style="text-decoration:none;border:1px solid #ddd;border-radius:12px;padding:16px;display:block;">
    {% if p.image %}
    <img src="{{ p.image }}" alt="{{ p.name }}" style="width:100%;border-radius:8px;margin-bottom:8px;">
    {% endif %}
    <h3 style="margin:0;">{{ p.name }}</h3>
    <p style="color:#555;">{{ p.description }}</p>
  </a>
  {% endfor %}
</div>
