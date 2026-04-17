# Journal des Prompts — Paris 2024 Olympic Ecosystem

## Note de méthode

Ce document constitue une **reconstitution méthodologique fidèle** des prompts utilisés, ou très proches de ceux qui ont permis d'obtenir le résultat final visible dans ce dépôt.  
L'objectif est de montrer une logique réaliste de Vibe Coding: architecture d'abord, production section par section, corrections, puis passe de qualité finale.

## Outils IA mobilisés

| Outil | Usage principal |
|---|---|
| Claude | génération HTML/CSS/JS, itérations, refactoring, documentation |
| ChatGPT | reformulation de prompts, aide à la structuration, synthèse |
| GitHub Copilot | autocomplétion et micro-corrections dans l'éditeur |

---

## 01. Architecture globale

**Contexte**  
Nous devions transformer 4 rendus de Session 1 en une webapp cohérente.

**Prompt**  
> Crée une architecture de site web multi-pages sur le thème des JO Paris 2024 avec une page d'accueil, 4 pages métiers, une navigation commune et un style visuel sombre premium avec accents teal et magenta.

**Intention**  
Poser un squelette clair avant de détailler les contenus.

**Résultat obtenu**  
Une base avec home, pages internes et direction visuelle.

**Limite rencontrée**  
La première version manquait de hiérarchie de navigation.

**Itération suivante**  
Ajouter explicitement le menu, le footer et les pages secondaires.

---

## 02. Arborescence et séparation des fichiers

**Contexte**  
Le premier prototype était trop monolithique.

**Prompt**  
> Sépare le projet en plusieurs fichiers: une feuille de style centrale, une page d'accueil, une page par exercice, un dossier images et une structure simple à déployer sur GitHub Pages.

**Intention**  
Rendre le projet maintenable et lisible.

**Résultat obtenu**  
Découpage en HTML/CSS avec dossier `pages/` et `img/`.

**Limite rencontrée**  
Les chemins relatifs sont vite devenus fragiles.

**Itération suivante**  
Faire une passe de correction des liens internes.

---

## 03. Prompt d'identité visuelle

**Contexte**  
Nous voulions un rendu cohérent sur toutes les pages.

**Prompt**  
> Propose une direction artistique dark UI inspirée des JO Paris 2024, avec une typographie forte, des accents lumineux et des cartes élégantes, sans dépendance à une librairie externe.

**Intention**  
Créer une signature visuelle mémorable.

**Résultat obtenu**  
Palette sombre + teal/magenta + Barlow Condensed + Inter.

**Limite rencontrée**  
Le design était joli mais encore trop générique.

**Itération suivante**  
Ajouter des blobs, des rings, des gradients et des cartes plus premium.

---

## 04. Navbar et footer communs

**Contexte**  
Le jury devait pouvoir naviguer très vite dans les 4 parties.

**Prompt**  
> Ajoute une navbar fixe commune à toutes les pages avec état actif, version mobile hamburger et footer global avec liens de navigation et pages légales.

**Intention**  
Sécuriser l'UX transversale.

**Résultat obtenu**  
Navigation cohérente et footer homogène.

**Limite rencontrée**  
Le comportement mobile devait être davantage testé.

**Itération suivante**  
Faire une passe responsive dédiée.

---

## 05. Hero d'accueil

**Contexte**  
La home devait présenter le projet en moins de 10 secondes.

**Prompt**  
> Crée une page d'accueil héro avec un titre fort, un sous-texte clair, deux CTA et des éléments graphiques décoratifs évoquant un univers data + événement mondial.

**Intention**  
Rendre la page d'accueil immédiatement lisible.

**Résultat obtenu**  
Hero immersif avec CTA vers les sections clés.

**Limite rencontrée**  
La home ne justifiait pas encore assez la démarche pédagogique.

**Itération suivante**  
Ajouter une section sur les 4 transpositions et la méthode Vibe Coding.

---

## 06. Section “4 transpositions”

**Contexte**  
Le brief insiste sur la transformation des rendus de Session 1.

**Prompt**  
> Ajoute sur la home une section qui résume comment chacun des 4 exercices a été transposé dans la webapp, avec une phrase métier et un lien direct vers la page concernée.

**Intention**  
Rendre le mapping “brief → solution” évident.

**Résultat obtenu**  
Une lecture plus académique et plus claire pour le jury.

**Limite rencontrée**  
Il fallait aussi expliciter la méthode de travail.

**Itération suivante**  
Créer une section “Méthode Vibe Coding”.

---

## 07. Section “Méthode Vibe Coding”

**Contexte**  
La qualité des prompts compte autant que le résultat final.

**Prompt**  
> Ajoute une section éditoriale sur la home qui explique la méthode: architecture d'abord, génération par section, corrections, audit final et documentation.

**Intention**  
Montrer que le projet n'est pas qu'un rendu visuel.

**Résultat obtenu**  
Une mise en contexte utile pour la soutenance et le dépôt.

**Limite rencontrée**  
Les noms du groupe restaient inconnus au moment de l'édition.

**Itération suivante**  
Prévoir des placeholders à remplacer avant dépôt.

---

## 08. Écosystème — premier prompt fonctionnel

**Contexte**  
L'infographie de Session 1 devait devenir une page interactive.

**Prompt**  
> Crée une page écosystème avec un diagramme réseau SVG représentant les parties prenantes des JO Paris 2024, une liste cliquable à gauche et un panneau de détail à droite.

**Intention**  
Transformer une infographie statique en interface vivante.

**Résultat obtenu**  
Un schéma central avec nœuds et panneau de lecture.

**Limite rencontrée**  
La lecture des catégories n'était pas assez rapide.

**Itération suivante**  
Ajouter des filtres par famille d'acteurs.

---

## 09. Écosystème — filtres par catégorie

**Contexte**  
Le schéma était riche mais dense.

**Prompt**  
> Ajoute des filtres “organisation”, “commercial”, “public” pour atténuer ou mettre en avant les nœuds concernés dans le réseau des parties prenantes.

**Intention**  
Rendre la lecture progressive.

**Résultat obtenu**  
La page est devenue plus pédagogique.

**Limite rencontrée**  
Le panneau de détail n'était pas encore assez incarné.

**Itération suivante**  
Ajouter des stats, un rôle principal et des connexions visibles.

---

## 10. Écosystème — affinage du panneau de détail

**Contexte**  
Le clic devait produire une vraie sensation d'analyse.

**Prompt**  
> Quand on clique sur un acteur, affiche dans le panneau latéral son rôle, un chiffre clé, sa catégorie et les acteurs auxquels il est connecté.

**Intention**  
Donner une valeur analytique au clic.

**Résultat obtenu**  
Le panneau détail est devenu plus “dashboard”.

**Limite rencontrée**  
Sur mobile, la lecture restait moins confortable.

**Itération suivante**  
Scroller automatiquement vers le panneau sur petit écran.

---

## 11. Dashboard — génération initiale

**Contexte**  
Le tableau analytique de Session 1 devait devenir un dashboard.

**Prompt**  
> Crée un dashboard de performance pour Léon Marchand avec filtres, cartes KPI, courbe d'évolution, graphique en barres, radar chart et tableau détaillé.

**Intention**  
Transformer la donnée en narration visuelle.

**Résultat obtenu**  
Une page riche avec plusieurs niveaux de lecture.

**Limite rencontrée**  
Le dashboard était visuel mais pas encore assez interactif au clic.

**Itération suivante**  
Ajouter un panneau de focus synchronisé.

---

## 12. Dashboard — filtres métier

**Contexte**  
Le brief demandait des filtres par période, compétition et épreuve.

**Prompt**  
> Ajoute trois filtres combinables: année, compétition et épreuve. Le tableau et le graphique des compétitions doivent se mettre à jour dynamiquement.

**Intention**  
Couvrir explicitement la consigne PDF.

**Résultat obtenu**  
Une lecture personnalisable selon le filtre actif.

**Limite rencontrée**  
Le radar restait global, ce qui était acceptable mais moins dynamique.

**Itération suivante**  
Renforcer au moins l'explication narrative autour des données filtrées.

---

## 13. Dashboard — focus interactif

**Contexte**  
Le dashboard devait mieux “parler” au jury.

**Prompt**  
> Ajoute un panneau de focus interactif qui se met à jour quand on clique sur un point de la courbe, une barre du graphique ou une ligne du tableau.

**Intention**  
Rendre la démonstration orale plus fluide.

**Résultat obtenu**  
Le dashboard est devenu plus démonstratif et plus lisible.

**Limite rencontrée**  
Il fallait synchroniser l'état sélectionné avec les filtres.

**Itération suivante**  
Ajouter une logique de reset intelligent quand le filtre invalide la sélection.

---

## 14. Dashboard — micro-copy et lisibilité

**Contexte**  
Les graphiques existaient, mais la consigne “devenir plus précis au clic” n'était pas assez visible.

**Prompt**  
> Réécris les sous-titres et la micro-copy du dashboard pour inviter explicitement à cliquer sur les éléments interactifs.

**Intention**  
Rendre les fonctionnalités évidentes sans explication orale.

**Résultat obtenu**  
Le jury comprend mieux comment lire le dashboard.

**Limite rencontrée**  
Le tableau pouvait paraître purement passif.

**Itération suivante**  
Rendre les lignes cliquables avec surbrillance.

---

## 15. Héritage — structure narrative

**Contexte**  
Le texte argumenté devait devenir une page immersive.

**Prompt**  
> Conçois une page héritage en scroll storytelling avec plusieurs chapitres, des compteurs, une citation, un avant/après et une carte de territoire.

**Intention**  
Donner du rythme à une matière plus textuelle.

**Résultat obtenu**  
Une page narrative avec 5 temps de lecture.

**Limite rencontrée**  
Certains graphiques secondaires manquaient de clarté.

**Itération suivante**  
Corriger les visualisations d'investissement et la carte.

---

## 16. Héritage — citation incarnée

**Contexte**  
Le brief demandait des citations et une approche habitant / territoire.

**Prompt**  
> Intègre une citation forte sur l'héritage urbain avec un portrait d'Anne Hidalgo et un bloc témoignage d'habitant pour ancrer la lecture dans le réel.

**Intention**  
Équilibrer data et récit humain.

**Résultat obtenu**  
La page a gagné en dimension éditoriale.

**Limite rencontrée**  
Le témoignage restait symbolique et non relié à une donnée.

**Itération suivante**  
Encadrer le récit par des compteurs et la répartition des investissements.

---

## 17. Héritage — correction de la carte

**Contexte**  
La carte d'infrastructures manquait de repères.

**Prompt**  
> Rends la carte plus lisible en ajoutant les orientations, le périphérique, le tracé de la Seine et une légende couleur compréhensible sans commentaire externe.

**Intention**  
Éviter un effet “beau mais flou”.

**Résultat obtenu**  
La carte est devenue bien plus explicite.

**Limite rencontrée**  
Sur mobile, la largeur restait une contrainte.

**Itération suivante**  
Prévoir un overflow horizontal propre sur petit écran.

---

## 18. Innovations — grille initiale

**Contexte**  
Le rapport innovations devait devenir une interface exploratoire.

**Prompt**  
> Crée une page innovations avec 12 fiches réparties en 4 catégories, un score d'impact, des filtres et un modal de détail au clic.

**Intention**  
Transformer un rapport en bibliothèque interactive.

**Résultat obtenu**  
Une grille riche, claire et démonstrative.

**Limite rencontrée**  
La page avait besoin d'une lecture globale en plus des cartes.

**Itération suivante**  
Ajouter jauges et radar.

---

## 19. Innovations — visualisations globales

**Contexte**  
Les cartes seules ne suffisaient pas à résumer l'ensemble.

**Prompt**  
> Ajoute un radar global des impacts technologiques et des jauges par catégorie pour visualiser rapidement les forces de Paris 2024.

**Intention**  
Donner une synthèse visuelle avant l'exploration détaillée.

**Résultat obtenu**  
La page s'ouvre désormais sur une lecture “macro”.

**Limite rencontrée**  
Les fiches devaient rester lisibles sur mobile.

**Itération suivante**  
Réduire la densité et ajuster les tailles aux breakpoints.

---

## 20. Innovations — modal de détail

**Contexte**  
Le clic devait approfondir, pas seulement ouvrir une fenêtre.

**Prompt**  
> Fais du modal un espace de lecture analytique avec titre, catégorie, description longue et rappel visuel du score d'impact.

**Intention**  
Éviter un modal gadget.

**Résultat obtenu**  
Le clic apporte une vraie valeur d'information.

**Limite rencontrée**  
Il fallait verrouiller le scroll du body sur ouverture mobile.

**Itération suivante**  
Ajouter un comportement de scroll lock propre.

---

## 21. Responsive — premier audit

**Contexte**  
Le brief insiste sur le test mobile.

**Prompt**  
> Audit toute la webapp sur 3 tailles d'écran: desktop, tablette, mobile étroit. Corrige la navbar, les cartes, les tableaux et les zones interactives tactiles.

**Intention**  
Sécuriser les points UX.

**Résultat obtenu**  
Le menu hamburger, les grilles et les cartes sont devenus plus robustes.

**Limite rencontrée**  
Certaines zones restaient denses sur petits écrans.

**Itération suivante**  
Ajuster padding, typographies et min-heights.

---

## 22. Responsive — ciblage mobile dashboard et héritage

**Contexte**  
Deux pages étaient plus risquées: dashboard et héritage.

**Prompt**  
> Optimise spécifiquement le dashboard et la page héritage pour mobile: cartes KPI, tableau, slider avant/après, carte SVG, textes de section et zones de clic.

**Intention**  
Fiabiliser les pages les plus complexes.

**Résultat obtenu**  
La navigation mobile est devenue bien plus crédible.

**Limite rencontrée**  
Le tableau restait forcément plus compact.

**Itération suivante**  
Accepter le scroll horizontal propre plutôt que de casser la lecture.

---

## 23. Accessibilité légère et micro-qualité

**Contexte**  
Le site devait paraître plus propre et plus pro.

**Prompt**  
> Fais une passe de micro-qualité: labels FR cohérents, accents, textes plus explicites, hover states, boutons plus lisibles et messages d'empty state clairs.

**Intention**  
Gagner des points invisibles mais décisifs.

**Résultat obtenu**  
Le rendu est plus homogène et plus “fini”.

**Limite rencontrée**  
La preuve méthodologique devait encore être renforcée.

**Itération suivante**  
Documenter mieux les prompts et la logique de travail.

---

## 24. Déploiement GitHub Pages

**Contexte**  
Le rendu final exige une URL publique.

**Prompt**  
> Prépare le projet pour GitHub Pages avec chemins relatifs propres, page 404 cohérente et structure statique simple à publier.

**Intention**  
Assurer un lien fonctionnel sans build complexe.

**Résultat obtenu**  
Le projet est compatible avec un hébergement statique simple.

**Limite rencontrée**  
Les docs n'expliquaient pas encore assez la méthode.

**Itération suivante**  
Créer une documentation projet plus orientée barème.

---

## 25. Documentation projet

**Contexte**  
Le dépôt devait aider à préparer le rendu Moodle.

**Prompt**  
> Rédige une documentation claire du projet avec architecture, stack, logique métier, mapping entre les 4 exercices et les pages web, puis prépare les éléments utiles pour le dossier final.

**Intention**  
Transformer le dépôt en support de rendu.

**Résultat obtenu**  
Documentation projet + matériaux pour Moodle.

**Limite rencontrée**  
Il manquait encore une annexe de prompts plus complète.

**Itération suivante**  
Élargir ce journal avec une chronologie plus réaliste.

---

## 26. Audit final orienté barème

**Contexte**  
La fin de session devait être optimisée pour la note.

**Prompt**  
> Évalue le projet comme un correcteur sur 20 selon: qualité des prompts, fidélité de la transposition, qualité de la webapp, interactivité et déploiement. Donne les derniers ajustements à faire pour maximiser la note.

**Intention**  
Passer d'un beau site à un rendu académique fort.

**Résultat obtenu**  
Dernière passe sur la home, le dashboard, la documentation et les livrables.

**Limite rencontrée**  
Les noms du groupe et les dernières captures restaient à personnaliser.

**Itération suivante**  
Compléter avant dépôt individuel sur Moodle.

---

## Ce que ce journal montre

- Une logique de travail par étapes et non un unique prompt magique
- Des prompts de création, mais aussi de correction, de reformulation et d'audit
- Une progression réaliste: structure, design, fonctionnalités, responsive, documentation, déploiement
- Une utilisation de l'IA comme copilote de production et non comme générateur aveugle

## Personnalisation avant rendu

- Remplacer les placeholders de noms dans les documents finaux
- Ajouter des captures d'écran des prompts si vous en avez
- Vérifier que l'URL publique finale est bien celle utilisée dans le dossier Moodle
