# Rendu : Nicolas Bestauros Alvarez

- Dépôt : tp-git-qqch
- Site GitHub Pages : https://nicolasb659.github.io/tp-git-qqch/

## Ex2
git log --oneline :
367f03b (HEAD -> main, origin/main) ex2: corrige une faute
cb081ac ex2: ajoute trois lignes
9665edb ex2: crée les notes
41c1da8 ex1: initialise le dépôt

## Ex3
- config.local est-il encore dans l'historique ? Pourquoi ?

config.local est toujours présent dans l'historique puisque si on tape git log --oneline --all -- config.local, on obtient :
5c8aa11 (HEAD -> main, origin/main) ex3: arrête de suivre config.local
414f603 ex3: ajoute config.local (erreur)

Cela est normal car on a fait que arrêter de le suivre et donc les étapes antérieurs sont toujours persistantes dans la mémoire de git car il était toujours suivis. Ainsi, le dernier commit enregistre son retrait de la version actuelle du dépôt, sans effacer les commits antérieurs.

## Ex4
- git status après avoir retiré brouillon.txt du staging :

Quand on fait git status on obtient :

On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   RENDU.md
        modified:   brouillon.txt

no changes added to commit (use "git add" and/or "git commit -a")


- Différence entre annuler une modification et retirer du staging ?

La différence consiste en que retirer du staging conserve les modifications, tandis qu’annuler une modification les efface. 

## Ex6
- À quoi servent <<<<<<<, ======= et >>>>>>> ?

Les marqueurs permettent de mieux identifier les conflits entre les différentes versions d'un fichier. 
<<<<<<< HEAD => après est affiché la version actuellement présente sur main.
======== => sépare les différentes versions 
et >>>>>>> => version provenant de l'autre branche.

## Ex7
- git stash list (avant récupération) : stash@{0}: On main: ex7: travail en cours
- Pourquoi annuler un commit plutôt que l'effacer de l'historique ?

Il vaut mieux annuler un commit plutôt que de l'effacer de l'historique car cela permets de conserver une trace des modifications effectuées et de leur annulation. Donc, on peut mieux comprendre les erreurs passées et éviter de reproduire la même erreur surtout quand plusieurs personnes travaillent sur le dépôt. 

## Ex8
- git pull = git fetch + quoi ?

git pull = git fetch + git merge

## Ex10
git log --oneline --graph --all :

git config (--global) alias.lg "log --oneline --graph --all" => mettre --global permet de créer l'alias dans les dépôts git sur mon mac. 