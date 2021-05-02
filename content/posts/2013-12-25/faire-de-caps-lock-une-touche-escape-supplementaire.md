---
title: "Faire de Caps Lock une touche Escape supplémentaire"
Date: 2013-12-25T15:51:00Z
categories: 
- "Logiciels libres"
Tags: 
- "Linux"
Slug: faire-de-caps-lock-une-touche-escape-supplementaire
Summary: Pour les utilisateurs de Vim, évidemment
---


Depuis que j’utilise vim comme éditeur, j’ai besoin d’avoir une touche Escape facilement accessible. Comme je n’ai pas pour habitude d’écrire tout en capitales, la touche Caps Lock est une candidate idéale du fait de son positionnement sur le clavier et de son utilité limitée de par son comportement par défaut.

Si vous utilisez un environnement de bureau comme GNOME ou KDE, il est très simple d’aller dans les options du clavier et de faire de la touche Caps Lock un Escape supplémentaire. Pour les autres, il y a `xmodmap`.

Sur le web, vous trouverez beaucoup d’instructions pour obtenir ce comportement via `xmodmap`, mais j’ai l’impression que depuis une mise à jour de `xmodmap`, les instructions qu’on trouve sur le web sont très souvent obsolètes.

Voici le fichier `~/.Xmodmap` qui fonctionne chez moi, sous Debian, Ubuntu, Linux Mint et Arch linux :

    clear lock
    keycode 66 = Escape

Si ça ne fonctionne pas pour vous, vous pouvez utiliser `xev` pour vérifier quel keycode envoie votre touche Caps Lock, et remplacer 66 par le bon keycode.

