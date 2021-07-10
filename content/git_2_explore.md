---
title: Introduction Git
class: animation-fade
layout: true
---

<!-- FIXME: parler des branches et de ses commandes (partie 3?) mais surtout  -->
<!-- FIXME: parler de reset -->

<!-- class: impact -->

# 2. Explorer un dépôt existant

---

# 2. Explorer un dépôt existant

Il s'agit de **télécharger** le dépôt d'un **logiciel** depuis Internet en créant un dossier contenant le code ainsi que son **historique Git**:

- `git clone <url dépot>` puis `cd <dépôt>` pour aller dans le dossier du dépôt (par exemple `git clone https://github.com/YunoHost/gertrude/` et `cd gertrude`)
- `git log` pour voir la liste des commits
- `git checkout <commit num>` pour vous **déplacer** au niveau d'un commit : le code dans le dépôt **change**.
- `git diff <commit_1> <commit_2>` pour voir ce qui a changé entre deux commits.
- Plus pratique : `apt install tig` et `tig` pour explorer chaque commit ou alors utilisez **VSCode** et [**GitLens**](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

Un dépôt Git téléchargé depuis Internet peut être privé : il faut alors se connecter avant à son compte (en HTTP ou SSH) pour le télécharger. Quand on veut modifier le dépôt distant (ajouter des commits), il faut de toute façon se connecter à un compte.

---

## L'historique d'un dépôt

![](img/tig_history.png)

---

## `master` et les branches d'un dépôt

![](img/git_branches_2.png)

- Un dépôt git permet d'avoir **plusieurs historiques** en parallèle qu'on appelle des **branches**. Un dépôt git ressemble à un arbre.

- ## La **branche principale** s'appelle **`master`** dans git (par convention), parfois `main`.

- ## Ça commence à devenir compliqué ! Mais on va souvent travailler avec seulement **deux branches** 😌

- **master** + **une branche** pour votre travail en cours.

---

## Remonter le temps, déplacer HEAD

- Si git **mémorise les commits successifs** du dépôt c'est en particulier pour permettre de "_remonter le temps_", c'est-à-dire **remettre le code** du dépôt **dans un état antérieur**.
  - `git checkout <num_commit>`. L'historique se met également à jour.
  - `git diff` permet à tout moment d'afficher les différences entre deux points du dépôt.

--

- Dans git, **HEAD** désigne un curseur qui indique dans quel état est le dépôt actuellement.
  - par défaut **HEAD** pointe sur le dernier commit de la branche (`master` s'il n'y en a qu'une).
  - remonter le temps cela signifie déplacer **HEAD**.
  - `git reflog` affiche l'historique des déplacements de **HEAD**.

---

## Déplacer HEAD dans l'historique

![](img/head_point_3.jpg)

---

## Interface graphique pour explorer l'historique d'un dépôt.

Plusieurs éditeurs de code proposent des interfaces graphique pour :

- naviguer dans les modifications d'un dépôt.
- comparer plusieurs états du dépôt.

C'est le cas de VSCode, en particulier avec les extensions **Git Graph** et **GitLens**.

D'autres interfaces pratiques et indépendantes de l'éditeur : _tig_, _meld_, ...

- Installer GitLens dans VSCode si ce n'est pas déjà fait

---

<!-- class: impact -->

# Explorer un dépôt

<!-- # Démonstration -->

<!-- FIXME: Utiliser par exemple le dépôt des exercices Python. pour revenir au début sur du code que les étudiants connaissent. Ou la Flask app ?-->

---

<!-- class: impact -->

# Deuxième TP

---
