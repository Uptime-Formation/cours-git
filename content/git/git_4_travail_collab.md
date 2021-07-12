---
title: Git 4 - Forges Git
weight: 400
---

# Git - quatrième partie

<!-- FIXME: Parler de merge --continue -->

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
- **_`git push`_** : envoyer la dernière version locale de la branche actuelle jusqu'au dépôt distant (bouge le `HEAD` distant, en d'autres termes modifie `origin/HEAD`)

 <!-- FIXME: leanringgit :  "Remote" Push & Pull -- dépôts gits distants ! (ou `remote1`) -->
 <!-- FIXME: ajouts commande git remote add / set + speech sur le rôle de origin ou any other one -->
