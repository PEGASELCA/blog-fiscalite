# Structure du blog Jekyll - Fiscalité Immobilière

## 📁 Structure des dossiers

```
blog-fiscalite/
├── _config.yml
├── index.md
├── _data/
│   └── navigation.yml
├── _posts/
│   └── 2025-06-12-sci-revenus-locatifs.md
├── a-propos.md
├── contact.md
├── fiscalite-sci.md
└── Gemfile
```

## 📄 Fichiers à créer

### 1. `_config.yml`

```yaml
# Configuration du site
title: Fiscalité Immobilière
email: contact@fiscalite.mca13.fr
description: >-
  Blog spécialisé dans la fiscalité immobilière : SCI, revenus fonciers,
  optimisation fiscale, défiscalisation et conseils patrimoniaux.
baseurl: ""
url: "https://fiscalite.mca13.fr"
twitter_username: fiscalite_immo
github_username: votre-username

# Construction
markdown: kramdown
remote_theme: "mmistakes/minimal-mistakes@4.26.2"
minimal_mistakes_skin: "default" # "air", "aqua", "contrast", "dark", "dirt", "neon", "mint", "plum", "sunrise"

# Plugins
plugins:
  - jekyll-paginate
  - jekyll-sitemap
  - jekyll-gist
  - jekyll-feed
  - jekyll-include-cache
  - jekyll-seo-tag

# Configuration de l'auteur
author:
  name: "Expert Fiscalité"
  avatar: "/assets/images/avatar.jpg"
  bio: "Spécialiste en fiscalité immobilière et optimisation patrimoniale"
  location: "France"
  email: "contact@fiscalite.mca13.fr"
  links:
    - label: "Email"
      icon: "fas fa-fw fa-envelope-square"
      url: "mailto:contact@fiscalite.mca13.fr"
    - label: "LinkedIn"
      icon: "fab fa-fw fa-linkedin"
      url: "https://linkedin.com/in/votre-profil"

# Configuration des défauts
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: true
      share: true
      related: true

# Pagination
paginate: 5
paginate_path: /page:num/

# Archives
category_archive:
  type: liquid
  path: /categories/
tag_archive:
  type: liquid
  path: /tags/
```

### 2. `Gemfile`

```ruby
source "https://rubygems.org"

gem "github-pages", group: :jekyll_plugins
gem "jekyll-include-cache", group: :jekyll_plugins

# Windows et JRuby
gem "tzinfo", ">= 1", "< 3"
gem "tzinfo-data"
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
```

### 3. `index.md`

```yaml
---
layout: home
title: Bienvenue sur le blog fiscalité
author_profile: true
classes: wide
---

# Expert en Fiscalité Immobilière

Bienvenue sur votre ressource complète pour tout comprendre de la fiscalité immobilière en France. 

## 🏠 Nos derniers articles

Découvrez nos analyses détaillées sur :
- La fiscalité des SCI (IR vs IS)
- L'optimisation des revenus fonciers
- Les dispositifs de défiscalisation
- La transmission de patrimoine immobilier

## 💡 Pourquoi ce blog ?

La fiscalité immobilière est complexe et évolue constamment. Notre mission est de vous apporter des informations claires, actualisées et pratiques pour optimiser votre patrimoine immobilier.

---

*Abonnez-vous à notre newsletter pour ne manquer aucune actualité fiscale !*
```

### 4. `_data/navigation.yml`

```yaml
# Navigation principale
main:
  - title: "Accueil"
    url: /
  - title: "À propos"
    url: /a-propos/
  - title: "Contact"
    url: /contact/
  - title: "Fiscalité SCI"
    url: /fiscalite-sci/
  - title: "Articles"
    url: /posts/
  - title: "Catégories"
    url: /categories/
```

### 5. `a-propos.md`

```yaml
---
layout: single
title: À propos
permalink: /a-propos/
author_profile: true
---

# À propos de Fiscalité Immobilière

## Notre mission

Démocratiser l'accès à l'information fiscale immobilière et vous accompagner dans l'optimisation de votre patrimoine.

## Qui sommes-nous ?

Fort de plus de 10 ans d'expérience dans le conseil patrimonial et la fiscalité immobilière, notre équipe met à votre disposition son expertise pour vous aider à :

- ✅ Comprendre les mécanismes fiscaux
- ✅ Optimiser vos revenus fonciers
- ✅ Choisir les bons montages juridiques
- ✅ Anticiper les évolutions réglementaires

## Nos domaines d'expertise

- **SCI** : IR vs IS, optimisation, transmission
- **Revenus fonciers** : déclaration, charges déductibles
- **Défiscalisation** : Pinel, Denormandie, Malraux
- **Plus-values immobilières** : calcul et exonérations
- **IFI** : stratégies d'optimisation

## Contact

N'hésitez pas à nous contacter pour toute question ou suggestion d'article !

📧 [contact@fiscalite.mca13.fr](mailto:contact@fiscalite.mca13.fr)
```

### 6. `contact.md`

```yaml
---
layout: single
title: Contact
permalink: /contact/
---

# Contactez-nous

## 📧 Par email

Pour toute question fiscale ou suggestion d'article :
**contact@fiscalite.mca13.fr**

## 📝 Formulaire de contact

<form action="https://formspree.io/f/VOTRE-ID" method="POST">
  <div style="margin-bottom: 1em;">
    <label for="name">Nom :</label>
    <input type="text" id="name" name="name" required style="width: 100%; padding: 0.5em;">
  </div>
  
  <div style="margin-bottom: 1em;">
    <label for="email">Email :</label>
    <input type="email" id="email" name="_replyto" required style="width: 100%; padding: 0.5em;">
  </div>
  
  <div style="margin-bottom: 1em;">
    <label for="subject">Sujet :</label>
    <select id="subject" name="subject" style="width: 100%; padding: 0.5em;">
      <option>Question fiscale</option>
      <option>Demande de conseil</option>
      <option>Suggestion d'article</option>
      <option>Autre</option>
    </select>
  </div>
  
  <div style="margin-bottom: 1em;">
    <label for="message">Message :</label>
    <textarea id="message" name="message" rows="5" required style="width: 100%; padding: 0.5em;"></textarea>
  </div>
  
  <button type="submit" style="background: #0066cc; color: white; padding: 0.5em 2em; border: none; cursor: pointer;">Envoyer</button>
</form>

## 💬 Réseaux sociaux

- LinkedIn : [Fiscalité Immobilière](https://linkedin.com)
- Twitter : [@fiscalite_immo](https://twitter.com)

## ⏰ Délai de réponse

Nous nous efforçons de répondre sous 48h ouvrées.
```

### 7. `fiscalite-sci.md`

```yaml
---
layout: single
title: Fiscalité SCI
permalink: /fiscalite-sci/
toc: true
toc_label: "Sommaire"
toc_icon: "cog"
---

# La fiscalité des SCI : Guide complet

## Qu'est-ce qu'une SCI ?

La Société Civile Immobilière (SCI) est une forme juridique permettant de détenir et gérer un patrimoine immobilier à plusieurs.

## IR ou IS : Quel régime choisir ?

### SCI à l'IR (Impôt sur le Revenu)

**Avantages :**
- Transparence fiscale
- Déduction des intérêts d'emprunt
- Imputation des déficits fonciers

**Inconvénients :**
- Imposition au TMI (jusqu'à 45%)
- Prélèvements sociaux (17,2%)

### SCI à l'IS (Impôt sur les Sociétés)

**Avantages :**
- Taux d'imposition réduit (15% jusqu'à 42 500€)
- Amortissement du bien
- Charges déductibles étendues

**Inconvénients :**
- Option irrévocable
- Double imposition en cas de distribution

## Articles récents sur la SCI

{% for post in site.categories.SCI limit:5 %}
  - [{{ post.title }}]({{ post.url }})
{% endfor %}

[Voir tous les articles SCI →](/categories/#sci)
```

### 8. `_posts/2025-06-12-sci-revenus-locatifs.md`

```yaml
---
title: "Comment déclarer les revenus locatifs en SCI ?"
date: 2025-06-12
categories: [Fiscalité, SCI]
tags: [SCI, Revenus fonciers, Déclaration, IR, IS]
excerpt: "Guide complet pour déclarer correctement vos revenus locatifs en SCI selon le régime fiscal choisi (IR ou IS)."
header:
  teaser: /assets/images/sci-declaration.jpg
---

# Déclarer les revenus locatifs en SCI : Le guide complet

La déclaration des revenus locatifs en SCI dépend essentiellement du régime fiscal choisi. Voici tout ce qu'il faut savoir pour éviter les erreurs.

## 📊 SCI à l'IR : La transparence fiscale

### Principe de base

En SCI à l'IR, les revenus sont imposés directement entre les mains des associés, proportionnellement à leurs parts.

### Étapes de déclaration

1. **La SCI établit le résultat**
   - Loyers perçus
   - Moins : charges déductibles
   - = Résultat à répartir

2. **Chaque associé déclare sa quote-part**
   - Formulaire 2044 (régime réel)
   - Case 4BA à 4BE selon la situation

### Charges déductibles en SCI IR

✅ **Déductibles :**
- Intérêts d'emprunt
- Taxe foncière
- Charges de copropriété
- Travaux d'entretien et réparation
- Frais de gestion
- Assurances

❌ **Non déductibles :**
- Travaux d'amélioration
- Amortissement du bien

## 💼 SCI à l'IS : L'imposition des sociétés

### Calcul du résultat fiscal

```
Loyers encaissés
- Charges déductibles
- Amortissements
= Résultat imposable
```

### Taux d'imposition 2025

- **15%** sur les 42 500 premiers euros
- **25%** au-delà

### Avantages spécifiques

1. **Amortissement du bien**
   - Sur 25 à 40 ans selon la nature
   - Réduit considérablement l'impôt

2. **Report des déficits**
   - Sans limitation de montant
   - Report indéfini

## 📝 Exemple concret

**Situation :** SCI avec 2 associés à 50/50
- Loyers annuels : 24 000€
- Charges : 8 000€
- Intérêts d'emprunt : 6 000€

### En SCI IR
- Résultat : 24 000 - 8 000 - 6 000 = 10 000€
- Chaque associé déclare : 5 000€
- Impôt (TMI 30%) : 1 500€ par associé

### En SCI IS
- Avec amortissement (4 000€/an)
- Résultat : 10 000 - 4 000 = 6 000€
- IS à payer : 6 000 × 15% = 900€

## ⚠️ Points de vigilance

1. **Conservation des justificatifs**
   - Minimum 6 ans
   - Tous les justificatifs de charges

2. **Déclaration dans les délais**
   - SCI IS : 3 mois après clôture
   - SCI IR : avec la déclaration personnelle

3. **Cohérence des déclarations**
   - Entre la SCI et les associés
   - D'une année sur l'autre

## 🎯 Conclusion

Le choix du régime fiscal impacte directement la méthode de déclaration. L'IS peut être avantageux pour les gros patrimoines, tandis que l'IR reste plus simple pour les petites SCI familiales.

---

*Besoin d'aide pour optimiser votre SCI ? [Contactez-nous](/contact/) pour un accompagnement personnalisé.*
```

### 9. `.gitignore`

```
_site
.sass-cache
.jekyll-cache
.jekyll-metadata
vendor
.bundle
Gemfile.lock
```

### 10. `README.md`

```markdown
# Blog Fiscalité Immobilière

Blog Jekyll utilisant le thème Minimal Mistakes, spécialisé dans la fiscalité immobilière.

## 🚀 Installation locale

1. Cloner le repository
```bash
git clone https://github.com/VOTRE-USERNAME/blog-fiscalite.git
cd blog-fiscalite
```

2. Installer les dépendances
```bash
bundle install
```

3. Lancer le serveur local
```bash
bundle exec jekyll serve
```

4. Ouvrir http://localhost:4000

## 📝 Ajouter un article

Créer un fichier dans `_posts/` avec le format :
`YYYY-MM-DD-titre-article.md`

## 🎨 Personnalisation

- Modifier `_config.yml` pour les paramètres globaux
- Éditer `_data/navigation.yml` pour le menu
- Changer le thème dans `minimal_mistakes_skin`

## 📦 Déploiement GitHub Pages

1. Pusher sur la branche `main`
2. Aller dans Settings > Pages
3. Sélectionner Source : Deploy from a branch
4. Choisir `main` et `/root`
```

## 🎯 Prochaines étapes

1. **Créer le repository GitHub** : `blog-fiscalite`
2. **Copier tous ces fichiers** dans le repo
3. **Activer GitHub Pages** dans les settings
4. **Configurer le domaine custom** : fiscalite.mca13.fr

Tu veux que j'ajoute d'autres fonctionnalités comme :
- 📊 Google Analytics
- 💬 Système de commentaires
- 📧 Newsletter
- 🔍 Recherche interne ?