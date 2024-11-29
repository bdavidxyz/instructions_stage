# instructions_stage

Instructions pour stagiaires de l'ENI

# Instruction pour stage ENI

Ceci est un simple exercice pour prendre la main sur la manière de travailler avec GitHub.

Le but est de faire un site web d'une seule page (index.html), à destination de celles et ceux qui débutent dans le web 

Si vous êtes bloqué(es) et que vous ne savez pas comment faire, il faut chercher **massivement** de l'aide sur Internet : chatGPT, Google, StackOverflow, Reddit, Twitter, Discord...

Vous avez besoin de VsCode et Git

## Instructions de départ

- Créer une clé SSH pour Github : https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

- Créer un repository sur GitHub, et invitez votre collègue (ainsi que votre instructeur) à être collaborateur du repository

- La branche principale du projet doit s'appeler "main"

- Le repository doit contenir 3 fichiers : index.html, README.md et .gitignore

## Développer une feature

- Chaque feature doit faire l'objet d'une branche séparée, qui part de main
- Chaque branche doit avoir une PR (Pull Request) associée
- Chaque feature doit avoir plusieurs commits, dont au moins un commit de chaque stagiaire
- Une fois que la feature est terminée, il faire "merge pull request" pour que les modifications soient dans main.
- Une fois que la feature est terminée, il faut déployer index.html grâce aux gh-pages
- Vous pouvez travailler en pair-programming (en même temps sur  la même branche, en visio, et celui/celle qui travaille partage son écran)
- Vous pouvez travailler en parallèle sur une feature différente chacun(e).  L'arbre de commit doit rester vertical, grâce à la fonction "rebase" de git (en cas de conflit, pas de merge).


##  Liste des features demandées

- FEAT_TITL: Dans index.html, on doit trouver plusieurs niveau de titre différent, chacun ayant au moins un paragraphe rempli.
- FEAT_FORM: Dans index.html, on doit trouver un formulaire qui fait semblant d'envoyer une requete, sans JS (utiliser jsonplaceholder pour le endpoint)
- FEAT_PARA: Dans index.html, un des paragraphes doit lister l'ensemble des tags (strong, em...) liés à la typographie
- FEAT_NAV:  Dans index.html, on doit trouver une barre de menu, où chaque titre a une ancre liée (anchor link, avec un #) à un paragraphe de niveau 2 (h2)
- FEAT_ALP:  Dans index.html, on doit trouver un exemple d'utilisation d'AlpineJS pour montrer/cacher un élément
- FEAT_IMG:  Dans index.html, on doit voir au moins 2 images, en lazy-loading, format base64.

## Commandes Git utiles

(le nom "mybranch" est un example, et doit être adapté à chaque feature)

- Télécharger un repository existant sur GitHub `git clone git@github.com:nom/projet.git` (attention à bien utiliser le SSH)

- vérifier les fichiers modifiés localement `git status`

- annuler la modification d'un fichier `git checkout -- mauvaisfichier.txt`

- se positionner sur la branche principale `git checkout main`

- se positionner sur une autre branche `git checkout mybranch`

- Créer une nouvelle branche en local `git checkout -b mybranch`

- Faire une première modif du code, puis ajouter les modifs sur la branche `git add . && git commit -m 'commentaire sur les modifs'`

- Pousser la branche sur Github `git push origin mybranch`

- Créer une PR depuis mybranch : se fait depuis l'interface GitHub

- Faire le plus petit changement possible qui marche, puis `git add . && git commit -m 'mon autre modif' && git push origin mybranch`

- Encore un autre, puis `git add . && git commit -m 'presque fini' && git push origin mybranch`, etc

- Merger la Pull Request : se fait depuis l'interface Github.

- Vérifier l'arbre en local: utiliser Gitk, ou le "source control graph" de VsCode

- Récuperer en local une branche qui est sur Github : `git fetch origin $1 && git checkout $1`

Vérifier l'arbre en local

```
gitk --all &
```

Raccourcis utiles :

```
alias gs='git status'
alias gk='gitk --all &'
alias gd='git diff'
```

Fonction utile:

```
feco() {
 git fetch origin $1 && git checkout $1
}
```
