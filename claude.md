# Paris 2024 — Écosystème Olympique

## Présentation du projet

Ce site web est une vitrine interactive dédiée à l'écosystème des Jeux Olympiques de Paris 2024. Il présente les parties prenantes, les résultats sportifs, l'héritage urbain et les innovations technologiques liées à cet événement mondial.

Le projet est réalisé dans le cadre d'un exercice académique (Ynov 2025-2026) et déployé sur GitHub Pages.

---

## Architecture du site

```
├── index.html                  # Page d'accueil (hero + présentation)
├── ecosysteme.html             # Cartographie des parties prenantes
├── dashboard.html              # Tableau de bord des résultats sportifs
├── heritage.html               # Héritage socio-économique et urbain
├── innovations.html            # Innovations technologiques et durables
├── css/
│   └── style.css               # Feuille de style partagée (~1 500 lignes)
├── img/
│   └── Anne_Hidalgo.jpg        # Photo portrait d'Anne Hidalgo (section héritage)
├── pages/
│   ├── mentions-legales.html   # Mentions légales
│   └── politique-confidentialite.html  # Politique de confidentialité
├── claude.md                   # Documentation du projet (ce fichier)
├── PROMPTS.md                  # Journal des prompts utilisés
└── design-*.html               # Maquette HTML originale (fichier source)
```

---

## Stack technique

| Élément          | Technologie                                     |
|------------------|--------------------------------------------------|
| Langages         | HTML5, CSS3, JavaScript (vanilla)                |
| Polices          | Google Fonts — Barlow Condensed, Inter           |
| Graphiques       | SVG inline avec `<animate>` (courbes, barres, radar, jauges) |
| Icônes           | SVG inline (aucune librairie externe)            |
| Animations       | CSS @keyframes + IntersectionObserver            |
| Hébergement      | GitHub Pages (branche `main`)                    |
| Versioning       | Git + GitHub CLI                                 |

---

## Palette de couleurs

| Couleur   | Code hex  | Utilisation                  |
|-----------|-----------|-------------------------------|
| Teal      | `#00c4a0` | Accent principal, liens, CTA  |
| Magenta   | `#e91e8c` | Accent secondaire, highlights |
| Or        | `#ffd60a` | Médailles d'or, alertes       |
| Noir      | `#0e0e0e` | Fond global                   |
| Surface   | `#1a1a1a` | Cartes et conteneurs          |
| Gris      | `#6b7280` | Texte secondaire, bordures    |
| Blanc     | `#e5e7eb` | Texte principal               |

---

## Pages détaillées

### 1. Accueil (`index.html`)
- Hero plein écran avec titre animé et bouton CTA
- Présentation rapide du projet

### 2. Écosystème (`ecosysteme.html`)
- Diagramme réseau SVG interactif (8 nœuds)
- Liste cliquable des parties prenantes (athlètes, CIO, COJO, sponsors, médias, ville, spectateurs, sécurité)
- Panneau latéral de détails avec description et statistiques
- Icônes SVG inline pour chaque catégorie

### 3. Dashboard (`dashboard.html`)
- Tableau des médailles françaises (source : données officielles Paris 2024)
- Graphiques SVG : courbe de progression, barres par discipline, radar par catégorie
- Filtres par discipline (Judo, Natation, Escrime, Cyclisme, Athlétisme)
- Résultats détaillés avec indicateurs visuels (pastilles or/argent)

### 4. Héritage (`heritage.html`)
- Compteurs animés : emplois créés, touristes, investissements
- Slider avant/après pour la transformation du Village des Athlètes
- Timeline des projets d'héritage (2021-2030)
- Citation d'Anne Hidalgo avec photo portrait
- Jauges d'impact sur la satisfaction citoyenne, le transport et les espaces verts

### 5. Innovations (`innovations.html`)
- Grille de 12 innovations réparties en 4 catégories (durabilité, tech sportive, diffusion média, expérience spectateur)
- Filtres par catégorie
- Scores d'impact visuels
- Modal de détails au clic
- Icônes SVG thématiques (feuille, soleil, recyclage, capteur, cerveau, etc.)

---

## Fonctionnalités transversales

- **Navigation responsive** : barre de navigation fixe avec menu hamburger sur mobile
- **Animations au scroll** : les éléments `.fade-in-up` apparaissent progressivement via IntersectionObserver
- **Footer** : liens de navigation, mentions légales, politique de confidentialité
- **Mode sombre** : design entièrement dark par défaut, optimisé pour le contraste WCAG

---

## Données utilisées

Les données présentées dans le site sont issues de sources officielles :
- Comité d'Organisation des Jeux Olympiques (COJO Paris 2024)
- Comité International Olympique (CIO)
- Rapports d'impact économique de la Ville de Paris
- Données de performance sportive issues des résultats officiels

---

## Déploiement

- **URL** : https://seypherr.github.io/paris-2024-ecosystem/
- **Dépôt** : https://github.com/Seypherr/paris-2024-ecosystem
- **Branche** : `main` (GitHub Pages legacy build)

---

## Outils IA utilisés

- **Claude (Anthropic)** — Génération de code HTML/CSS/JS, refactoring, documentation
- **GitHub Copilot** — Assistance à l'édition dans VS Code
