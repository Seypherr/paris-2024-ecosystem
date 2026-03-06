# Documentation des Prompts — Paris 2024 Olympic Ecosystem

## Objectif du projet

Créer un site web interactif multi-pages présentant l'écosystème des Jeux Olympiques de Paris 2024 : acteurs, performances, héritage et innovations.

---

## Outils IA utilisés

| Outil | Utilisation |
|---|---|
| **Claude (Anthropic)** | Génération de code, refactoring, documentation, débogage |
| **GitHub Copilot** | Autocomplétion et suggestions dans VS Code |
| **ChatGPT (OpenAI)** | Recherche de données, rédaction de contenus textuels |

---

## Prompts utilisés

### Prompt 1 — Découpage initial

> « À partir de ce design et de la première page, je veux que tu crées un site entier utilisant uniquement le même style de CSS que dans le script. Sépare le code avec HTML et CSS de chaque côté avec aussi les différentes pages présentes dans la nav bar. »

**Résultat** : séparation du design monolithique en 6 fichiers (style.css + 5 HTML).

---

### Prompt 2 — Page Écosystème

> « Crée la page écosystème avec un diagramme réseau SVG interactif qui montre les relations entre les parties prenantes des JO. Je veux pouvoir cliquer sur chaque nœud pour voir les détails dans un panneau latéral. Ajoute des filtres par catégorie. »

**Résultat** : schéma réseau 8 nœuds, panneau de détails, liste cliquable.

---

### Prompt 3 — Dashboard athlète

> « Fais un dashboard performance pour Léon Marchand avec au moins 3 graphiques SVG : une courbe de progression, un graphique en barres et un radar chart. Ajoute un tableau de résultats avec des filtres par année et discipline. Utilise des données réelles de ses compétitions. »

**Résultat** : dashboard avec 4 indicateurs, courbe SVG, barres par discipline, radar, tableau filtrable.

---

### Prompt 4 — Page Héritage

> « Conçois une page héritage avec du scroll storytelling montrant l'impact des JO sur Paris. Intègre des compteurs animés, un slider avant/après pour le Village des Athlètes, une timeline des projets et des jauges de satisfaction. »

**Résultat** : 5 chapitres, compteurs IntersectionObserver, slider draggable, timeline, jauges SVG.

---

### Prompt 5 — Innovations

> « Crée une page innovations avec 12 fiches d'innovations technologiques dans 4 catégories. Chaque fiche doit avoir un score d'impact et ouvrir un modal au clic. Ajoute un radar chart global et des jauges par catégorie. »

**Résultat** : grille filtrable de 12 innovations, modal, jauges circulaires, radar 8 axes.

---

### Prompt 6 — Audit qualité et corrections

> « Évalue le site sur 20 en vérifiant les critères suivants : responsivité, accessibilité, cohérence du design, qualité du code, fonctionnalité des interactions. Propose les corrections nécessaires et applique-les. »

**Résultat** : note initiale 14.5/20, corrections appliquées (hamburger menu, migration CSS, filtres dashboard, visibilité panneau écosystème).

---

### Prompt 7 — Refonte architecture et emojis

> « Réorganise le projet avec des dossiers css/, img/ et pages/. Remplace tous les emojis par des icônes SVG inline pour que le site ait un rendu plus professionnel. Crée un footer fonctionnel avec mentions légales et politique de confidentialité. »

**Résultat** : nouvelle arborescence, 30+ emojis remplacés par des SVG, footer avec liens de navigation et pages légales.

---

### Prompt 8 — Intégration image Hidalgo

> « Integre la photo Anne_Hidalgo.jpg dans la section citation de la page héritage. Mets-la dans un conteneur rond avec une bordure teal. »

**Résultat** : avatar rond avec bordure `#00c4a0` dans le chapitre 1 heritage.

---

### Prompt 9 — Déploiement

> « Déploie le site sur GitHub Pages en utilisant le repository paris-2024-ecosystem. »

**Résultat** : déploiement GitHub Pages, URL publique fonctionnelle.

---

### Prompt 10 — Documentation

> « Crée un fichier claude.md avec toute la documentation du site : architecture, stack technique, palette, description des pages, données utilisées et liens de déploiement. »

**Résultat** : fichier de documentation complet.

---

### Prompt 11 — Migration des pages et lazy loading

> « Il faut passer toutes les pages dans pages/. Mettre du lazy loading afin de ne pas faire de bug. Créer une page 404 avec les redirections dessus en cas de chemin non existant. Mettre l'image de Leon_Marchand dans sa rubrique. »

**Résultat** :
- Les 4 pages de contenu (écosystème, dashboard, héritage, innovations) déplacées dans `pages/`
- Tous les liens internes (nav, footer, CSS, images) mis à jour dans les 7 fichiers HTML
- Lazy loading via `IntersectionObserver` ajouté sur écosystème (réseau SVG), dashboard (graphiques + table) et innovations (jauges, radar, grille)
- Page `404.html` créée avec navbar, liens de redirection et countdown automatique de 10s
- Photo `Leon_Marchand.jpg` intégrée dans le profil athlète du dashboard

---

### Prompt 12 — Correction graphiques héritage

> « Le graphique de répartitions des investissements ne marche pas, est-ce que tu peux le corriger. Le graphique Carte des Infrastructures manque de clarté sur quelle axe est quoi. »

**Résultat** :
- Bug des barres d'investissement corrigé : les éléments dynamiques étaient créés avec la classe `appear` (opacity: 0) après que l'observer ait scanné le DOM — remplacé par des transitions inline déclenchées par un observer dédié
- Carte des infrastructures améliorée : ajout d'un titre, d'indications d'orientation (Nord/Sud/Est/Ouest avec zones géographiques), du tracé du Périphérique, du label « La Seine » et d'une légende couleur

---

## Résultat final

Un site de 5 pages + page 404 fonctionnel, responsive et interactif avec :
- 15+ visualisations SVG (courbes, barres, radar, jauges, réseau, carte)
- 5 formes d'interactivité (filtres, clics, drag, scroll, modals)
- Navigation cohérente et footer complet avec pages légales
- Lazy loading sur tous les contenus lourds
- Page 404 avec redirection automatique
- Design dark mode uniforme
- Photos réelles intégrées (Anne Hidalgo, Léon Marchand)
- Déploiement sur GitHub Pages
