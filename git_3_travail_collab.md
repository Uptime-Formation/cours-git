---
title: Introduction Git
class: animation-fade
layout: true
---

<!-- class: impact -->

# Git - troisième partie

## Collaborer à l'aide de gitlab

---

# Git pour collaborer...

Git devient indispensable lorsque :

- L'équipe avec laquelle vous collaborez est grande...
- Changeante...
- Le logiciel évolue dans le temps et en taille.

---

# La merge request / pull request

---

- Github.com
  - ... est une forge logicielle en forme de réseau social.
- Gitlab
  - ... est une forge logicielle concurrente, et qui est open source : on peut en installer sa propre instance (ex: framagit.org). La plus grosse instance Gitlab est gitlab.com.

---

# CI/CD (0/1)

L'intégration continue.

S'assurer automatiquement de la qualité du code

La forge est la source et autour viennent se greffer :

- _forge logicielle_

  - Github
  - Gitlab/Framagit

- _merge requests_ : valider du code à plusieurs

- **_`git fetch`_** : récupérer la dernière version du dépôt distant (sans rien changer à son dépôt local)
- **_`git pull`_** : récupérer la dernière version de la branche actuelle depuis le dépôt distant (bouge le `HEAD`)

<!-- FIXME: illustrations d'un flow et mention de différents flows -->

- Cycles de développement : l'exemple de Gitlab flow
  - notre version simplifiée master + feature branch
