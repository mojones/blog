---
title: Blog
---
This is a minimal Jekyll blog for `preliminarywork.com/blog/`. Add new entries as Markdown files in `_posts/`.

## Posts

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <div class="post-list-date">{{ post.date | date: "%-d %B %Y" }}</div>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
