---
layout: default
title: Essays
description: >-
  A reverse-chronological feed of long-form essays on the economics of
  physical systems — energy, agriculture, logistics, and infrastructure.
seo:
  type: Blog
---

<style>
  /* A single column, sized for reading. Nothing else. */
  .feed-wrap { max-width: 42rem; margin: 0 auto; }
  .feed-intro { margin: 0 0 3rem; padding-bottom: 2rem; border-bottom: 1px solid #e8e8e8; }
  .feed-intro h1 { margin: 0 0 .5rem; font-size: 2rem; line-height: 1.2; }
  .feed-intro p { margin: 0; color: #555; font-size: 1.05rem; line-height: 1.6; }
  .feed { list-style: none; margin: 0; padding: 0; }
  .feed-item { margin: 0 0 3.25rem; padding: 0; }
  .feed-meta { display: block; margin-bottom: .35rem; font-size: .8rem; letter-spacing: .06em;
               text-transform: uppercase; color: #767676; }
  .feed-title { margin: 0 0 .6rem; font-size: 1.5rem; line-height: 1.25; }
  .feed-title a { color: inherit; text-decoration: none; }
  .feed-title a:hover { text-decoration: underline; }
  .feed-excerpt { margin: 0 0 .6rem; color: #333; line-height: 1.65; }
  .feed-more { font-size: .9rem; }
  .feed-empty { color: #767676; font-style: italic; }
  .feed-foot { margin-top: 3rem; padding-top: 1.5rem; border-top: 1px solid #e8e8e8;
               font-size: .9rem; color: #767676; }
</style>

<div class="feed-wrap">

  <header class="feed-intro">
    <h1>{{ site.title }}</h1>
    <p>{{ site.tagline }}</p>
  </header>

  <ul class="feed">
    {%- for post in site.posts -%}
    <li class="feed-item">
      <article>
        <span class="feed-meta">
          <time datetime="{{ post.date | date_to_xmlschema }}">
            {{ post.date | date: site.minima.date_format | default: "%B %-d, %Y" }}
          </time>
          {%- if post.categories.size > 0 %} · {{ post.categories | join: " · " }}{% endif -%}
        </span>

        <h2 class="feed-title">
          <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>

        <div class="feed-excerpt">
          {{ post.description | default: post.excerpt | strip_html | truncatewords: 55 }}
        </div>

        <p class="feed-more">
          <a href="{{ post.url | relative_url }}">Read the full essay &rarr;</a>
        </p>
      </article>
    </li>
    {%- else -%}
    <li class="feed-empty">No essays published yet.</li>
    {%- endfor -%}
  </ul>

  <footer class="feed-foot">
    <p>
      Full text of every essay is available to automated readers.
      Machine-readable index:
      <a href="{{ '/feed.xml' | relative_url }}">Atom feed</a> ·
      <a href="{{ '/sitemap.xml' | relative_url }}">sitemap</a> ·
      <a href="{{ '/robots.txt' | relative_url }}">robots.txt</a>
    </p>
  </footer>

</div>
