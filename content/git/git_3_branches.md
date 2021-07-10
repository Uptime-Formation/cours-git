---
title: Git - Troisième partie - Les branches
weight: 310
---

## Collaborer à l'aide des branches

Nous avons pour l'instant utilisé Git de manière linéaire : nos commits représentent une ligne qui va du commit le plus ancien au commit le plus récent.

Mais la force de Git est le concept d'arborescence (d'arbre) constituée de branches.

Théoriquement, une branche n'est qu'un pointeur, une sorte d'étiquette vers un commit particulier, qui est mise à jour à chaque fois que l'on crée un commit en ayant _activé_ telle branche.

### Créer une branche et basculer sur une branche

Créer une branche se fait avec la sous-commande `checkout` et l'option `-b` :
`git checkout -b <nom_de_branche>`
Si la branche existe déjà, il suffit d'utiliser `git checkout` suivi du nom de branche :
`git checkout <nom_de_branche>`

<!-- ### Supprimer une branche distante

**Attention ! C'est dangereux !** -->

### Les tags

Les tags sont supposés immutables. Ils servent souvent pour garder la trace du commit qui définit une version précise d'un logiciel.

<!-- FIXME: illustrations d'un flow et mention de différents flows -->

<!-- ## Cycles de développement -->
 <!-- FIXME: soit là soit dans partie 4 travail collab  -->

<!-- ### l'exemple de Gitlab flow

- notre version simplifiée master + feature branch -->
