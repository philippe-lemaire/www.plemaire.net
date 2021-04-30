---
title: "Migration Du Blog Sous Hugo"
subtitle: ""
date: 2021-04-30T08:31:25+02:00
lastmod: 2021-04-30T08:31:25+02:00
draft: false
author: "Philippe Lemaire"
summary: "Où comment se relancer dans le blogging grâce au plaisir de jouer avec un nouvel outil… "

page:
    theme: "wide"

upd: ""
authorComment: ""

tags: [Hugo, Python]
categories: [Internet]

rssFullText: true

hiddenFromHomePage: false
hiddenFromSearch: false

featuredImage: "/img/hugo-featured.png"

---

## Introduction

La plupart des outils de gestion de contenus en ligne (CMS) utilisent un language de scripting comme Php et une base de données pour permettre la création et l’édition de contenus par l’utilisateur directement dans son navigateur. J’ai longtemps utilisé WordPress pour ça, et les premiers articles de ce blog ont été rédigés dans ce système, avant une première migration vers un outil de blog statique appelé [Pelican](https://blog.getpelican.com/) 

Le côté pratique des CMS est évident, mais il vient avec un prix : l’utilisation d’une base de données pour accéder au contenu et reconstruire les pages demandées par les visiteurs à la volée, ça prend du temps au serveur, et sur la plupart des sites, même des publications professionnelles, ça prend une petite seconde ou deux d’afficher une page, et parfois bien plus. 

Les outils de blog statiques permettent de créer des sites contenant toutes les pages nécessaires d’un blog (index, articles, listes par catégories, par étiquettes, par date) en quelques millisecondes, et le bénéfice est un travail beaucoup plus simple côté serveur puisqu’il n’y a pas de base de données à consulter ni de pages à générer à la volée, juste des fichiers html, css et images à servir.

Initialement, j’avais utilisé Pelican donc pour faire une première migration depuis WordPress. 
Aujourd’hui, il est assez apparent que Pelican, s’il est plus simple, offre beaucoup moins de fonctionnalités et a une communauté de développeurs beaucoup moins active, aussi j’ai décidé d’utiliser le framework de site statique qui me semble le plus actif et le plus populaire, [Hugo](https://gohugo.io/).

## Comment utiliser Hugo pour créer un site

La [documentation d’Hugo](https://gohugo.io/getting-started/quick-start/) est plutôt bien faite.
Il suffit d’installer la dernière version d’Hugo, et de suivre les commandes pour créer l’ossature de base du site, puis d’aller dans le fichier de config pour régler différents aspects comme l’url de base, le nom, l’auteur, etc…

Ensuite on installe un thème, on rédige son contenu dans des fichiers textes en Markdown, et on passe une commande à Hugo pour qu’il mouline le tout et nous crée toutes les pages du site dans un dossier `public`, qui devra être servi par le serveur.

On peut faire ça sur sa machine puis envoyer le contenu du dossier public sur le serveur, mais il y a un moyen un peu plus propre et moderne en passant par un dépôt git et en générant le site final directement depuis le serveur, je vais détailler tout ça dans la dernière partie.

## Comment s'est faite la migration ?

Dans mon cas, ce fut un peu plus compliqué car j’avais déjà un blog statique et donc des fichiers de contenus faits pour Pelican, et la syntaxe de l’entête de chaque fichier pour indiquer son titre, url, résumé, date de création et autres avait besoin d’être légèrement modifiée.

Heureusement, je n’étais pas le premier à faire cette migration et j’ai trouvé un [script python](https://github.com/anthonynelzin/PelicanToHugo) écrit par [Anthony Nelzin](https://anthony.nelzin.fr/) que je remercie au passage, et qui après quelques modifications pour l’adapter à ma situation m’a permi de récupérer tous mes anciens contenus et les rendre "hugo compatibles".

Une fois que tout fonctionnait correctement en local, sur mon serveur j’ai renommé le dossier de mon ancien site pour faire une copie de secours, j’ai tiré de mon dépôt git le nouveau site, et ajusté les fichiers de configuration d’Apache2 pour adapter à la nouvelle structure des répertoires.

Un petit coup de `certbot` plus tard pour rafraîchir le certificat SSL et le nouveau site était fonctionnel.

J’ai pris le parti de ne pas remettre d’outil de commentaire comme disqus, qui n’apporte pas grand chose, et ajoute une couche de complexité et de cookies.

Je n’ai pas non plus installé d’outil de tracking des visites comme Google Analytics, sans intérêt pour un site perso à mon humble avis. Souriez, vous n’êtes pas pistés, et vous n’avez pas besoin d’accepter l’utilisation des cookies, il n’y en a pas !

## Le mode de publication plus en détail 

### Première étape : créer le fichier d’un nouvel article 

En local, dans le répertoire principal du site :

`hugo new articles/mon-nouvel-article.md`

Le fichier est créé automatiquement dans le répertoire `content/articles/`.

On le crée ainsi plutôt que directement à la main parce que hugo va se baser sur le fichier `archetypes/default.md` pour créer le fichier avec le bon contenu d’entête avec le titre, la date, l’auteur. Certains champs sont automatiquement remplis selon la date, l’heure, le nom du fichier, d’autres sont à compléter.

### Deuxième étape : rédiger son contenu

Vous pouvez utiliser votre éditeur de texte préféré pour rédiger votre contenu. La syntaxe pour la mise en forme (listes, entêtes, images, gras…) est [markdown](https://daringfireball.net/projects/markdown/) que j’utilise tous les jours dans mes emails ou Jupyter Notebooks. C’est très simple et ça permet d’écrire en pseudo html beaucoup moins envahissant que le vrai. Hugo se chargera ensuite de transformer ce marquage en véritable html lors de la création des pages du site.

### Étape optionnelle : vérifier le rendu en local

Un petit `hugo serve` dans le dossier principal du site en local crée une version temporaire consultable en local du site, ce qui permet de vérifier que tout s’affiche correctement avant de pousser le nouveau contenu vers le serveur. 

### Troisième étape

Ce qui est génial avec un outil de blog statique, c’est que vous pouvez tout gérer avec du contrôle de version, comme votre code.
Un fois mon article prêt, je fais un `git add` suivi d’un `git commit` avec et je le pousse sur mon dépôt externe.
Ensuite, je n'ai plus qu’à me connecter à mon serveur en ssh, aller dans le répertoire du site, et faire un `git pull && hugo` pour récupérer les contenus nouveaux et reconstruire le site depuis le serveur.

## Conclusion

Voilà après quelques années d’inactivités en raison d’un manque criant de temps libre, cet exercice de migration m’a redonné envie de rédiger des billets pour le simple plaisir de structurer ma pensée et de me relire plus tard.
