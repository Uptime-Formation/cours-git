---
title: "Git - Partie1"
visible: true
---

# Créer un projet git

Durant ces exercices utilisez git en ligne de commande (sans interface graphique) l'objectif est de pratiquer les différentes commandes de base git

### Initialiser le dépôt

<!-- FIXME: URL microblog ou prendre un dossier qu'ils ont déjà -->

- Reprenez la solution finale de l'app microblog.
<!-- - Reprenez le corrigé de l'[exercice de programmation orienté objet (9.2) ](https://eliegavoty.fr/devops/python-poe/exercices-corriges-partie-3) -->

<!-- - En ligne de commande créez le dossier de code de votre `exercice_poo`. -->

- Chargez ce dossier avec VSCode.
  <!-- - FIXME: -->
  <!-- - Créez un nouveau fichier `about.py` -->
- Copier à l'intérieur le code nécessaire.
- Lancez `git status`. Quel est le problème ?
- Initialisez le dépot de code avec la commande `git init`.
- Utilisez ensuite `git status` pour voir l'état de votre dépôt.

### Dire à git de suivre un fichier

Pour le moment git ne versionne aucun fichier du dépôt comme le confirme la commande `git status`.

- Utilisez `git add <nom_fichier>` sur le fichier. Puis faites à nouveau `git status`. Le fichier est passé à l'état suivi (_tracked_).
<!-- FIXME: autre fichier -->
- Créez un nouveau fichier python `afficher_tables.py` dans lequel vous importez votre classe et l'utilisez pour afficher les tables de 1 à 10.
<!-- - Lancez votre script `afficher_tables.py` pour vérifier -->
- Faites `git status` à nouveau. Que s'est-il passé ?

### Faire votre premier commit

- Faites `git status` pour constater que tous les fichiers sont **non suivis** sauf un.
- Un commit est une version du code validée par un·e développeur/développeuse. Il faut donc que git sache qui vous êtes avant de faire un commit. Pour ce faire, utilisez :

```bash
git config --global user.name "<votre nom>"
git config --global user.email "<votre email>"
```

- Pour créer un commit on utilise la commande `git commit -m "<message_de_commit>"` (_commit_ signifie s'engager alors réfléchissez avant de lancer cette commande !). Généralement on utilise le message `initial commit` pour le premier commit d'un dépôt. Valider la version courante.
- Lancez un status pour voir l'état du dépôt. Que constate-t-on ?

### Commit de tous les fichiers

- Utiliser `git add` avec l'option `-A` pour ajouter tous les fichiers actuels de votre projet.
- Qu'affiche `git status` ?
- Lancez à nouveau `git commit` avec un message adéquat.
<!-- FIXME: ah y a pycache parce qu'on a lancé le code ? -->
- A quoi sert le dossier `__pycache__` ? Que faire avec ce dossier ?

### Supprimer un fichier

Oh non ! Vous avez ajouté le dossier `__pycache__` dans votre commit précédent 🙃
Ce ne serait pas correct de pousser sur Internet votre code en l'état !

- Supprimez le suivi du dossier `__pycache__` avec la commande `git rm`:
  - Quelles options sont nécessaires ? utilisez `git rm --help` pour les trouver.

### Ignorer un fichier

Maintenant que nous avons supprimé ce dossier nous voulons éviter de l'ajouter accidentellement à un commit à l'avenir. Nous allons ignorer ce dossier.

- Ajoutez un fichier `.gitignore` et à la première ligne ajoutez `__pycache__`
- Ajoutez ce fichier au suivi.
- Ajoutez un commit avec le message "`ignore __pycache__`"
<!-- - FIXME: il faut donc un programme à lancer -->
- Lancez le programme `afficher_tables` à nouveau.
- Lancez `status`. Que constate-t-on ?

### Annuler un ou plusieurs commit

Le problème avec la suppression de `__pycache__` de la partie précédente est qu'elle n'affecte que le dernier commit. Le dossier inutile `__pycache__` encombre encore l'historique de notre dépôt.

- Pour le constater, installez l'extension [`Git Graph` de VSCode](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph).
- Explorer la fenêtre git graph en cliquant sur `Git Graph` en bas à gauche de la fenêtre.
- Regardez successivement le contenu des deux commits.

<!-- FIXME: Wallah compliqué là tout de suite ! -->

Pour corriger l'historique du dépôt nous aimerions revenir en arrière.

- Utilisez `git reset` avec `HEAD~2` pour revenir deux commits en arrière (nous parlerons de `HEAD` plus tard).
- Faites `git status`. normalement vous devrier avoir deux fichiers non suivis `.gitignore` et `afficher_tables.py`. Git vient de réinitialiser les ajouts des deux commits précédents.
- Constatez dans Git Graph que seul reste le premier commit qui est toujours là.
- Ajouter et _committez_ tous les fichiers non suivis du dépôt.
- Vérifier que **`__pycache__`** n'apparaît pas dans l'historique.

 <!-- https://learngitbranching.js.org/?locale=fr_FR 1:  Séquence d'introduction et  Montée en puissance   -->
