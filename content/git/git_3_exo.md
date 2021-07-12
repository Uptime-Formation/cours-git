---
title: Git 3 - Les branches - Exercices
weight: 320
---

<!-- Le faire sur Github ET gitlab ? -->

# Partie 3 : Les branches

<!-- Explore branches in: -->
<!-- https://github.com/spring-projects/spring-petclinic.git -->
<!-- https://github.com/miguelgrinberg/microblog -->

<!-- Git cherrypick du commit d'ajout de about dans TP2 -->

## Maîtriser les commandes Git

[Learn Git branching](https://learngitbranching.js.org/?locale=fr_FR)

## Merge

Les fusions de branche peuvent s'effectuer en local sur la machine ou sur la forge logicielle.

Prendre le TP microblog et localiser la branche qui ajoute une page "A propos". Faire un `merge` de cette branche avec `master`...

<!-- FIXME: conflit avec TP4 qui fait créer un compte Framagit -->

- ... en local
- ... via Gitlab avec une Merge Request
- ... via Github avec une Pull Request

## Rebase

<!-- FIXME: précisions + tester -->

Prendre le TP microblog et localiser la branche qui ajoute une page "A propos".

- Faire un `rebase` de cette branche sur `master`.
- Faire un `rebase` de cette branche (ou d'une autre) sur `master` en mode interactif.
