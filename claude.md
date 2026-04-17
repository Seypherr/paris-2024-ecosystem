# Paris 2024 Olympic Ecosystem

## Présentation

Ce projet est une webapp académique réalisée dans le cadre d'un exercice de Vibe Coding autour des Jeux Olympiques de Paris 2024.  
L'objectif était de transformer quatre livrables de Session 1 en une expérience web cohérente, interactive, responsive et publiable en ligne.

## Correspondance entre le brief et la solution

| Exercice Session 1 | Transposition web |
|---|---|
| Infographie de l'écosystème JO | [pages/ecosysteme.html](C:/Users/eporc/Desktop/ia/paris-2024-ecosystem/pages/ecosysteme.html) avec réseau SVG, filtres et panneau de détail |
| Analyse des performances d'un athlète | [pages/dashboard.html](C:/Users/eporc/Desktop/ia/paris-2024-ecosystem/pages/dashboard.html) avec filtres, graphiques et focus interactif |
| Héritage olympique vu par un habitant | [pages/heritage.html](C:/Users/eporc/Desktop/ia/paris-2024-ecosystem/pages/heritage.html) avec scroll storytelling, citation, avant/après et carte |
| Innovations technologiques des JO Paris 2024 | [pages/innovations.html](C:/Users/eporc/Desktop/ia/paris-2024-ecosystem/pages/innovations.html) avec catégories filtrables, modals, jauges et radar |

## Méthodologie Vibe Coding

Le projet a été mené selon une logique itérative:

1. architecture et direction artistique,
2. génération d'une page par exercice,
3. correction des interactions et du responsive,
4. audit qualité,
5. documentation des prompts,
6. préparation du déploiement et du dossier Moodle.

Phrase de positionnement à reprendre dans le rendu final:

> Nous avons utilisé l'IA pour générer, itérer, corriger, tester et documenter la webapp.

## Stack technique

| Élément | Choix |
|---|---|
| Front-end | HTML5, CSS3, JavaScript vanilla |
| Graphiques | SVG inline |
| Interactions | `onclick`, filtres dynamiques, `IntersectionObserver`, modals |
| Typographies | Google Fonts — Barlow Condensed, Inter |
| Hébergement ciblé | Vercel |

## Structure du dépôt

```text
index.html
404.html
css/style.css
img/Anne_Hidalgo.jpg
img/Leon_Marchand.jpg
pages/ecosysteme.html
pages/dashboard.html
pages/heritage.html
pages/innovations.html
pages/mentions-legales.html
pages/politique-confidentialite.html
PROMPTS.md
DOSSIER_MOODLE.md
CHECKLIST_RENDU.md
```

## Points forts du rendu

- identité visuelle homogène sur l'ensemble des pages,
- navigation commune et mobile,
- 4 sections clairement alignées avec le brief,
- plusieurs niveaux d'interactivité visibles sans explication orale,
- documentation méthodologique prête pour Moodle.

## Déploiement

- URL publique: `https://paris-2024-ecosystem.vercel.app`
- Dépôt: `https://github.com/Seypherr/paris-2024-ecosystem`
- Type de déploiement: site statique sur Vercel

## Membres du groupe

- Matias Bouchenoire
- Ethan Porcaro
- Geoffrey Deverchere
- Louis Delarue

## Personnalisation avant remise

- Vérifier que l'URL publique finale est bien active
- Ajouter si possible des captures d'écran des prompts dans le document Moodle
