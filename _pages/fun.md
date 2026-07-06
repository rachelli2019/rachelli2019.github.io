---
title: "Fun"
permalink: /fun/
author_profile: true
---

{% include base_path %}

A few things I enjoy outside of research:

- Baking. I post some of my bakes on [@bakedbyrach.li](https://www.instagram.com/bakedbyrach.li/).
- Trying new restaurants and cafes.
- Board games and puzzle-y strategy games.
- Running and staying active.

I like projects that are a little meticulous, a little creative, and best when shared with other people.

## Baking

<section class="fun-section">
  <div class="fun-section__intro">
    <p>A small corner for bakes, experiments, and desserts worth repeating.</p>
    <a class="fun-section__link" href="https://www.instagram.com/bakedbyrach.li/">Follow @bakedbyrach.li</a>
  </div>

  {% if site.data.baking_gallery and site.data.baking_gallery.size > 0 %}
    <div class="baking-grid" aria-label="Baking gallery">
      {% for item in site.data.baking_gallery %}
        <figure class="baking-card">
          <img
            src="{{ item.image | prepend: '/images/' | prepend: base_path }}"
            alt="{{ item.alt | default: item.title }}"
            loading="lazy"
          >
          {% if item.title or item.caption %}
            <figcaption class="baking-card__caption">
              {% if item.title %}
                <span class="baking-card__title">{{ item.title }}</span>
              {% endif %}
              {% if item.caption %}
                <span class="baking-card__text">{{ item.caption }}</span>
              {% endif %}
            </figcaption>
          {% endif %}
        </figure>
      {% endfor %}
    </div>
  {% endif %}
</section>
