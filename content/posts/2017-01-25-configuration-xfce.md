---
title: "Comment faire de Xfce un environnement personnel et productif"
Date: 2017-01-25T12:00:00Z
categories: 
- "Logiciels libres"
Tags: 
- "Linux"
- "fedora"
- "Xfce"
Slug: comment-faire-de-xfce-un-environnement-personnel-et-productif
Summary: Xfce est un environnement de bureau qui peut sembler être un peu austère à première vue. Certains comme Cyrille Borne l’ont qualifié de « Gnome 2 du pauvre ».
---
Pourtant il offre une beaucoup plus grande flexibilité sans sacrifier aucune performance par rapport à GNOME 2 et son incarnation actuelle, MATE.

## Introduction

Je dois avouer une chose en préambule. Je suis un incorrigible distro-hopper. Je change souvent de distribution et d’environnement de bureau.
Mais j’ai tendance, après avoir expérimenté un environnement de bureau « moderne » et plein de fonctionnalités,
à retourner au confort et au calme qu’offrent les expériences plus minimalistes.

J’ai déjà parlé de Xfce sur ce blog. C'est un environnement de bureau qui offre une excellente stabilité (au sens où les choses changent peu d’une version à la suivante).
Je l’ai parfois utilisé pour les ordinateurs de tiers comme celui de ma femme, au moment de la transition de Gnome 2 à Gnome 3, comme une valeur refuge.

Mais c'est un environnement qui derrière sont apparente simplicité cache beaucoup de flexibilité, et peut devenir très confortable pour 
un utilisateur plus chevronné, à condition de passer un peu de temps à farfouiller dans les options.

Voici un petit guide des options que je considère les plus intéressantes.


## Gestion au clavier

Si vous êtes un utilisateur avancé, vous savez probablement vous servir de votre clavier, et aller chercher votre souris pour réaliser
des opérations courantes est une perte de temps.
Par défaut, assez peu de raccourcis clavier sont paramétrés, mais les options sont là, prêtes à être réglées à votre guise.

Ces réglages se trouvent dans les paramètres dans la section **Gestionnaire de fenêtres**, à l’onglet **Clavier**.

![gestionnaire fenêtres](/img/xfce412/xfce4-gestionnaire-fenetres.png)

### Manipuler les fenêtres

Si comme moi vous disposez d’un écran large, les 3 opérations les plus courantes pour manipuler vos fenêtres sont :

- Maximiser, 
- mettre en mosaïque à gauche ou droite
- déplacer une fenêtre sur les bureaux virtuels

Je vous recommande les réglages suivants :

- Maximiser une fenêtre : touche Super (celle avec le logo Windows sur la plupart des claviers) + Flèche Haut
- Mettre en mosaïque à gauche / droite : Super + Flèche Gauche / Droite
- déplacer la fenêtre vers l’espace de travail 1/2/3/4 : Super + Shift + 1/2/3/4
- Aller vers l’espace de travail 1/2/3/4 : Super + 1/2/3/4

Si vous disposez vos espaces de travail sur plusieurs lignes, vous pouvez également ajouter des raccourcis pour :

- Vous déplacer vers l'espace de travail à gauche / droite, au dessus, en dessous
- Envoyer la fenêtre active vers l'espace de travail à gauche / droite, au dessus, en dessous

J'utilise les touches JKHL de vim pour ça, avec Shift pour l'action consistant à déplacer la fenêtre.

### Lancer les applications

Lancer une application via le clavier est devenu très mainstream, même sur Windows.

Pour régler tout ça, il faut aller dans la partie **Clavier** des paramètres, puis dans l’onglet **Raccourcis d’applications**.

![clavier](/img/xfce412/xfce4-clavier.png)

Par défaut, le lanceur d’Xfce est appelé par le très clasisque et ancien raccourci alt + f2.
Mais celui-ci est plutôt inconfortable.
Mieux vaux le remplacer par une combinaison plus facile depuis la position par défaut des doigts sur le clavier, comme Super+Espace.

Lancer un terminal ou le gestionnaire de fichiers fait également partie des opérations très fréquentes.

Vous pouvez par exemple utiliser comme moi :

- Super + F pour lancer `Thunar`
- Super + Entrée pour lancer `xfce4-terminal`

## Tableaux de bord et widgets 
Les tableaux de bord sont assez flexibles, et permettent de présenter différentes informations comme les fenêtres ouvertes, l’heure et la date, les bureaux virtuels.
La configuration par défaut est intéressante, mais j’y apporte généralement 3 changements :

### le menu Whisker
![whisker-menu](/img/xfce412/xfce4-whisker-menu.png)

C'est un menu plus flexible et riche que le menu des applications par défaut, avec une recherche et une gestion des applications favorites.

### Le widget de date et heure Orage

![orage](/img/xfce412/xfce4-orage.png)

Il permet d'avoir un petit calendrier qui apparaît et disparait quand on clique sur la date et l'heure. Vous pouvez dans ses préférences faire en sorte
qu'il n’ait pas de barre de fenêtre, et qu'il n’apparaisse pas dans la liste des fenêtres actives, ce qui rend son comportement plus proche des autres environnements de bureau.

### Suppression du tableau de bord avec lanceurs en bas d’écran

Ce tableau de bord fait partie de la configuration par défaut d’Xfce mais est redondant avec les raccourcis clavier pour lancer ses applications.

## Bureau

Le bureau par défaut se comporte comme celui de Windows, à savoir comme un espace pour poser des fichiers, dossiers, et raccourcis vers des applications.
Je préfère un bureau vide, sans icône aucune. 

![bureau](/img/xfce412/xfce4-bureau.png)

Avantage supplémentaire : un clic droit sur le bureau donne accès à un menu pour lancer une application.


## Choix des applications

Xfce contient un certain nombre d’applications de base, comme son gestionnaire de fichiers `Thunar` et un éditeur de texte appelé `Mousepad`.

Vous êtes toutefois libre de remplacer ces applications par vos favorites.

Voici la liste de celles que j’utilise, qui restent dans l’esprit de Xfce : gtk, simples et légères

### Multimédia

- `Parole` (lecteur vidéo, projet Xfce)
- `Viewnior` (visionneur d’images)
- `Pragha` (musique)

### Éditeur de texte

- `Geany`
- `Gvim`

## Présentation et thème

Cette partie est sans doute la plus subjective.
Xfce utilisant GTK, un très grand nombre de thèmes peut être utilisés.

Le thème par défaut de la dernière version d’Xfce est malheureusement assez moche, avec de gros boutons pour réduire / maximiser / fermer les fenêtres.
Pour une utilisation prolongée de l’ordinateur, je préconise `Greybird`, avec les icônes `Elemantary-xfce-darkest`.

Exemple avec `Thunar` :
![paramètres](/img/xfce412/xfce4-thunar.png)

### Conclusion

Et vous, comment utilisez-vous Xfce ?
Si vous avez trouvé une astuce de configuration dont vous ne pourriez plus vous passer, n’hésitez pas à la partager dans les commentaires.
