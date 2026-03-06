# 📝 Documentation des Prompts — Paris 2024 Olympic Ecosystem

## 🎯 Objectif du Projet

Créer un site web interactif multi-pages présentant l'écosystème des Jeux Olympiques de Paris 2024, englobant les acteurs, les performances athlétiques, l'héritage olympique et les innovations technologiques.

---

## 📋 Prompt Principal

> **Prompt utilisé :**
>
> « À partir de ce design et de la première page, je veux que tu crées un site entier utilisant uniquement le même style de CSS que dans le script. Sépare le code avec HTML et CSS de chaque côté avec aussi les différentes pages présentes dans la nav bar. »

### Contraintes spécifiées :
- Séparation stricte HTML / CSS (fichier `style.css` partagé)
- Conserver l'identité visuelle du design original (couleurs, typographies, animations)
- Site multi-pages avec navigation cohérente

---

## 📄 Spécifications par Page

### Page 1 — Écosystème des JO (`ecosysteme.html`)
> « La page Écosystème des JO devra présenter l'ensemble des acteurs et parties prenantes (athlètes, fédérations, comité d'organisation, sponsors, médias, gouvernance, villes hôtes, spectateurs...) via une visualisation interactive en réseau (graphiques et schéma de relations en SVG), permettant de filtrer par catégorie et de cliquer pour afficher le détail de chaque acteur. »

**Éléments attendus :**
- Schéma réseau SVG interactif avec des nœuds cliquables
- Panneau de détail glissant
- Filtres par catégorie (Organisation, Commercial, Public)
- Liste des acteurs avec icônes et descriptions

### Page 2 — Dashboard Performance Athlète (`dashboard.html`)
> « La page Dashboard Performance Athlète présentera une analyse détaillée d'un athlète réel (Léon Marchand) avec un minimum de 3 graphiques interactifs en SVG : un graphique linéaire montrant l'évolution des performances dans le temps, un graphique en barres comparant les résultats par compétition, et un radar chart des dimensions de performance. La page inclura aussi un profil complet de l'athlète, un tableau de résultats détaillé avec filtres (année, compétition, épreuve), et des cartes de statistiques clés. »

**Éléments attendus :**
- Fiche athlète complète (Léon Marchand)
- 4 cartes de statistiques animées
- Graphique linéaire SVG (évolution 400m 4 nages)
- Graphique en barres SVG (médailles par compétition)
- Radar chart SVG (profil athlétique)
- Tableau de résultats filtrable
- 3 filtres dynamiques (année, compétition, épreuve)

### Page 3 — Héritage Olympique (`heritage.html`)
> « La page Héritage Olympique utilisera un format de scroll storytelling (défilement narratif chapitre par chapitre) pour montrer l'impact des Jeux sur la ville de Paris : impact urbain avec des compteurs animés, impact économique avec des barres de données, un témoignage d'habitant, une section avant/après interactive avec un slider glissable, et une carte interactive des infrastructures olympiques cliquable. »

**Éléments attendus :**
- 5 chapitres avec timeline verticale
- Compteurs animés au scroll (via IntersectionObserver)
- Citations stylisées
- Barres de données d'investissement
- Slider avant/après draggable
- Carte SVG interactive avec points cliquables

### Page 4 — Innovations Technologiques (`innovations.html`)
> « La page Innovations Technologiques présentera un rapport interactif sur les technologies déployées à Paris 2024. Elle inclura un radar chart à 8 axes, des jauges circulaires SVG animées par catégorie, une grille de 12 cartes d'innovations filtrables par catégorie (Durabilité, Tech Sportive, Diffusion Média, Exp. Spectateur), chaque carte affichant une barre d'impact et ouvrant un modal de détail au clic. »

**Éléments attendus :**
- Radar chart SVG 8 axes
- 4 jauges circulaires animées
- 12 cartes d'innovations filtrables
- Barres d'impact avec gradient
- Modal de détail au clic
- Score d'impact global

---

## 🎨 Directives de Design

| Aspect | Valeur |
|---|---|
| **Palette principale** | Teal `#00c4a0`, Magenta `#e91e8c`, Or `#ffd60a` |
| **Fond** | Dark `#0e0e0e`, Surface `#1a1a1a` |
| **Police titres** | Barlow Condensed (700, uppercase) |
| **Police corps** | Inter (300–600) |
| **Bordures** | `rgba(255,255,255,0.08)` |
| **Animations** | fadeInUp, float, pulse, apparition au scroll |
| **Graphiques** | SVG natifs avec `<animate>` |
| **Responsivité** | Mobile-first, breakpoints 768px / 1024px |

---

## 🔧 Choix Techniques

- **Aucun framework CSS** : CSS pur dans `style.css` partagé
- **Aucun framework JS** : Vanilla JavaScript dans chaque page
- **SVG dynamique** : Tous les graphiques générés en JavaScript
- **IntersectionObserver** : Animations au scroll (heritage)
- **Pas de dépendance externe** : Seulement Google Fonts en CDN

---

## 🔄 Itérations et Améliorations

### Itération 1 — Création initiale
Génération des 6 fichiers (style.css + 5 pages HTML) à partir du design monolithique.

### Itération 2 — Audit & Corrections
- Ajout du menu hamburger responsive pour mobile
- Migration des styles inline vers `style.css`
- Correction des filtres du dashboard (mise à jour de tous les graphiques)
- Correction du double attribut `style` sur dashboard.html
- Initialisation visible du panneau détail écosystème
- Déploiement sur GitHub Pages

---

## 📊 Résultat Attendu

Un site web de 5 pages entièrement fonctionnel, interactif, responsive, avec :
- **15+ graphiques/visualisations SVG**
- **5 types d'interactivité** (filtres, clics, drag, scroll, modals)
- **Navigation cohérente** entre toutes les pages
- **Design uniforme** respectant la charte graphique
- **Déploiement en ligne** accessible publiquement
