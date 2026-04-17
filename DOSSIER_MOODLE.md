# Dossier Moodle — Paris 2024 Olympic Ecosystem

## 1. Page de garde

- **Titre du projet**: Paris 2024 Olympic Ecosystem
- **Formation**: B2 — Projet supervisé Vibe Coding x JO Paris 2024
- **Membres du groupe**:
  - Matias Bouchenoire
  - Ethan Porcaro
  - Geoffrey Deverchere
  - Louis Delarue
- **URL de la webapp**: https://paris-2024-ecosystem.vercel.app

## 2. Méthodologie d'approche

Nous avons abordé le sujet comme un travail de transposition de livrables statiques vers une interface web interactive.  
Plutôt que de générer toute la webapp d'un seul bloc, nous avons procédé par étapes:

1. définir une architecture claire avec une page d'accueil et 4 sections,
2. poser une identité visuelle cohérente,
3. transformer chaque exercice de Session 1 en page web dédiée,
4. ajouter l'interactivité attendue,
5. corriger le responsive et les détails UX,
6. documenter les prompts et les itérations.

Nous avons utilisé l'IA pour générer, itérer, corriger, tester et documenter la webapp.

## 3. Outils utilisés

- Claude: génération HTML/CSS/JS, itérations, refactoring, documentation
- ChatGPT: reformulation de prompts, structuration, synthèse
- GitHub Copilot: autocomplétion et corrections locales
- Vercel: déploiement statique

## 4. Transposition des 4 exercices

### Exercice 1 — Infographie interactive de l'écosystème JO

Le rendu initial était une représentation statique de l'écosystème des JO Paris 2024.  
Nous l'avons transformé en page interactive avec:

- un réseau SVG central,
- des filtres par catégorie d'acteurs,
- une liste latérale cliquable,
- un panneau de détail mis à jour au clic.

### Exercice 2 — Dashboard performances athlète

Le rendu initial était un tableau analytique autour d'un athlète olympique.  
Nous l'avons transformé en dashboard avec:

- cartes KPI,
- filtres combinables,
- courbe d'évolution,
- graphique de podiums,
- radar chart,
- tableau détaillé,
- panneau de focus interactif au clic.

### Exercice 3 — Récit immersif sur l'héritage olympique

Le rendu initial était un texte argumenté.  
Nous l'avons transposé sous forme de page narrative avec:

- chapitres en scroll storytelling,
- citation et témoignage,
- compteurs animés,
- bloc avant/après,
- carte d'infrastructures,
- visualisation des investissements.

### Exercice 4 — Rapport innovations technologiques

Le rendu initial était un rapport structuré.  
Nous l'avons converti en page exploratoire avec:

- grille de fiches filtrables,
- catégories thématiques,
- scores d'impact,
- jauges,
- radar global,
- modal de détail pour chaque innovation.

## 5. Prompts et itérations

Le journal détaillé est disponible dans [PROMPTS.md](C:/Users/eporc/Desktop/ia/paris-2024-ecosystem/PROMPTS.md).  
Il présente une reconstitution méthodologique fidèle des étapes de travail:

- prompts d'architecture,
- prompts de design,
- prompts de production par page,
- prompts de correction,
- prompts d'audit final,
- prompts de documentation et de déploiement.

Si vous disposez de captures d'écran ou d'un historique de conversation, insérez-les ici dans la version finale du dossier.

## 6. Difficultés rencontrées

- garder une cohérence visuelle entre 4 pages très différentes,
- transformer des contenus statiques en composants interactifs sans framework,
- rendre les visualisations claires sur mobile,
- équilibrer richesse visuelle et simplicité de navigation,
- documenter correctement les itérations de prompts.

## 7. Axe critique

Si nous devions refaire le projet demain:

- nous prototyperions plus tôt les interactions les plus complexes,
- nous centraliserions encore davantage les composants communs,
- nous préparerions les captures de prompts dès le début,
- nous ferions un audit responsive intermédiaire au lieu d'un audit final plus tardif.

## 8. Conclusion

Ce projet nous a permis de comprendre que la qualité d'une production en Vibe Coding repose autant sur la formulation, l'itération et la méthode que sur le rendu final.  
La webapp obtenue montre qu'un écosystème, un tableau, un récit et un rapport peuvent être transformés en interfaces web cohérentes, interactives et démontrables rapidement.
