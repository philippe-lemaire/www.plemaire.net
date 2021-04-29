---
title: "Le scroll naturel à la Mac OS sous Linux"
Date: 2013-11-09T00:20:00Z
categories: 
- "Logiciels libres"
Tags: 
- "Linux"
Slug: le-scroll-naturel-la-mac-os-sous-linux
Summary: Comment utiliser le scroll naturel sous Linux
---


Début 2012, Mac OS X "Mountain Lion" innovait sur le plan de l’utilisation de la molette de la souris pour défiler verticalement les fenêtres.
Baptisé "natural scrolling", cette innovation était tout simplement l’inversion du défilement vertical auquel nous étions habitués depuis des lustres, pour se rapprocher du mouvement de défilement utilisé sur les smartphones. Pour descendre dans une page web, on pousse ainsi la molette vers devant soi, comme si le bas de la molette était le bas de la page que l’on pousserait du doigt.

Quand je suis tombé sur cette idée, en empruntant quelques secondes un mac, j’ai évidemment eu du mal à rompre avec mes habitudes. Mais à la longue, je dois avouer que j’aime beaucoup.

Pour reproduire l’effet sous n’importe quel bureau linux, c’est très simple, grâce à `xmodmap`, qui devrait être déjà installé sur votre machine.

Il suffit d’ouvrir ou de créer le fichier `.Xmodmap` à la racine de votre dossier personnel :

    vim ~/.Xmodmap

Et d’y insérer la ligne suivante :

    pointer = 1 2 3 5 4 7 6 8 9 10 11 12
    
L’effet est d’inverser les boutons 5 et 4 de la souris qui correspondent au défilement haut et bas de la souris.

Pour charger le changement, faites un petit :

    xmodmap ~/.Xmodmap

Assurez-vous que cette dernière instruction soit exécutée au chargement de votre session pour un effet permanent. Certains Display Managers chargent automatiquement le fichier ~/.Xmodmap s’il existe au démarrage de la session.

Pour retirer la modification, supprimez cette ligne de votre fichier `~/.Xmodmap`.

