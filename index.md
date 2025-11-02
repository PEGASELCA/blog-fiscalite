---
layout: home
author_profile: true
title: "Bienvenue sur le blog fiscalité"
header:
  overlay_image: "/assets/images/sci-ir-vs-is.png"
  overlay_filter: 0.4
  caption: "Infographies et lives partagés sur notre page Facebook"
---

Bienvenue ! Ce blog reprend et approfondit les contenus que nous publions chaque jour sur notre page Facebook **Fiscalité Immo Facile**. Vous y trouverez les infographies, carrousels et sessions live réorganisés en articles faciles à consulter.

## Pourquoi ce blog ?
- Garder une trace écrite de nos publications sociales qui disparaissent vite du fil.
- Ajouter des explications et des exemples chiffrés complémentaires.
- Vous offrir un point d’entrée unique pour partager les ressources avec vos clients ou partenaires.

## Derniers formats issus de Facebook
{% assign facebook_posts = site.posts | where_exp: "post", "post.tags contains 'Facebook'" | slice: 4 %}
<ul class="archive-list">
  {% for post in facebook_posts %}
  <li>
    <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a><br>
    <small>{{ post.date | date: "%d %B %Y" }}</small><br>
    {{ post.excerpt | strip_html }}
  </li>
  {% endfor %}
</ul>

## Rejoindre la communauté
- 👍 Suivez-nous sur Facebook : [Fiscalité Immo Facile](https://www.facebook.com/FiscaliteImmoFacile).
- 🗓️ Participez aux lives hebdomadaires : chaque jeudi à 12h30.
- 📨 Abonnez-vous à la newsletter pour recevoir le résumé du dimanche soir.

> 💡 *Astuce : enregistrez cette page dans vos favoris. Chaque nouvelle publication Facebook est transformée ici en article détaillé pour que vous ne manquiez aucune information.*
