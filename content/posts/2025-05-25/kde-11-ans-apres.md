---
title: "Kde 11 Ans Après"
subtitle: ""
date: 2025-05-25T16:25:36+02:00
lastmod: 2025-05-25T16:25:36+02:00
draft: false
author: "Philippe Lemaire"
summary: ""
image: "/img/kde-2025/featured-image.png"

page:
    theme: "wide"

tags: ["linux", "kde", ]
categories: ["Logiciels Libres"]

rssFullText: true

hiddenFromHomePage: false
hiddenFromSearch: false



toc:
  enable: true
math:
  enable: false
---

J’ai délaissé ce blog pendant des années. L’unique lecteur et l’auteur étant la même personne, il n’y a pas eu de victime.

Hier soir, en voulant mettre à jour un vieil article, j’ai réalisé que le thème Hugo que j’utilisais n’était plus maintenu
et plus compatible avec la version actuelle d’[Hugo](https://gohugo.io/). La tuile.

En réparant la chose, c’est à dire en testant différents thèmes, je suis tombé sur un de mes anciens articles, au titre bien présomptueux : ["Pourquoi j’ai choisi KDE"](/2014/01/pourquoi-j-ai-choisi-kde/), écrit il y a 11 ans.

Le plus drôle, c’est que pendant ces 11 années, j’ai principalement été un utilisateur de [GNOME](https://www.gnome.org/).

Pourtant, très récemment, pour changer un petit peu ma routine informatique, j’ai décidé d’installer Plasma 6.3 sur mon irréprochable Fedora 42 Workstation, juste pour voir.

## Quoi de neuf ?

J'ai fait quelques tentatives d’utiliser Plasma 5 comme bureau principal à plusieurs
reprises au cours des 11 dernières années, aussi ce nouveau Plasma 6 ne m’a pas
totalement ébourrifé par ses nouveautés.

Cependant j’ai remarqué quelques petites choses nouvelles lors de ma première
connexion.

### La barre qui flotte

Tout d’abord, la barre, en bas de l’écran par défaut, qui se détache du bord
de l’écran quand aucune fenêtre ne vient la toucher et la contraindre à descendre.

C'est tout bête, mais elle se fait remarquer aux moments où on a le plus de raison de
l’utiliser, et se fond dans le décor quand on est actif sur une tâche, et l’effet est très réussi.

![floating bar](/img/kde-2025/floating-bar.png)
*La petite barre qui flotte*

### Présentation des bureaux

Ensuite, j’ai remarqué une grande amélioration dans la vue qui présente les fenêtres ouvertes sur les
différents espace de travail ou bureaux. Avant c’était très foutraque et jamais aligné, désormais c’est beaucoup plus propre et harmonieux. Si vous avez le réflexe, dressé comme je le fus par GNOME d’envoyer le curseur de la souri dans le coin en haut à gauche pour voir vos fenêtres ouvertes et changer de tâche à la souris, c’est beaucoup plus imaginable de continuer dans Plasma 6 que ça ne l’était dans les itérations
précédentes.


![Présentation des bureaux](/img/kde-2025/presentation.png)
*Présentation des fenêtres ouvertes*


### Thème par défaut

Le theme par défaut **Breeze**, est beaucoup moins métallique et agressif que le thème **Oxygen** ne l'était dans le temps.

![Le file dialog d'il y a 11 ans](/img/kde-file-dialog.png)
*Le file picker d'il y a 11 ans, avec le thème oxygen*

![file Picker](/img/kde-2025/file-picker.png)
*Le file picker version 2025*


## Quoi de mieux ?

Quels sont les points sur lesquels [**Plasma**](https://kde.org/fr/announcements/plasma/6/6.3.0/) fait mieux que ses concurrents ?

### Dolphin

Le gestionnaire de fichier, [Dolphin](https://apps.kde.org/fr/dolphin/) est très performant et souple. Modes d'affichages (liste, arborescence, icônes), niveau de zoom, et mon truc préféré : la vue scindée qui présente le contenu de deux dossiers côte à côte, idéal pour faire du rangement. Le gestionnaire de fichiers [Nautilus](https://apps.gnome.org/fr/Nautilus/) de chez GNOME ne fait vraiment pas le poids.

![dolphin](/img/kde-2025/dolphin.png)
*Dolphin en vue scindée*

### Le File Picker

Dans un environnement GTK, une des choses les plus pénible est d’utiliser la boîte de dialogue
pour sélectionner un fichier (le file picker), particulièrement si c’est une image, car les vignettes sont
minuscules.

Le File Picker de Plasma est beaucoup plus souple, peut zoomer, et on peut même forcer Firefox et Thunderbird à l’utiliser :

![file Picker](/img/kde-2025/file-picker.png)
*le joli filepicker*

### La visionneuse de PDFs : Okular

Je suis meneur de jeux de rôles, et j’ai accumulé une belle collection de PDFs de livres
de règles et de modules.

La visionneuse de PDFs de GNOME, [Evince](https://apps.gnome.org/fr/Evince/), est beaucoup plus lente qu’[Okular](https://apps.kde.org/fr/okular/), son homologue côté KDE.
(même si je dois reconnaître qu’Evince s'est améliorée ces derniers temps là-dessus).

Comme je passe beaucoup de temps sur mes PDFs, c’est très apréciable. J’ai dû bien tailler dans les boutons affichés dans la barre d’outil, mais le résultat est probant.

![Okular](/img/kde-2025/okular.png)
*Mothership, so hot right now*


### L’outil de capture d’écran : Spectacle

C’est bête mais avoir un outil de capture d’écran souple (prendre tout l’écran, une zone rectangulaire, la fenêtre active, avec ou sans délai, sauvegarder dans un dossier donné), c’est vraiment plaisant, surtout quand on prépare un petit billet de blog tel que celui là et qu’on doit donc non seulement prendre des captures, mais également les ranger dans un dossier précis. **Spectacle** est largement plus riche en fonctionnalité que son homologue chez GNOME.

![Spectacle](/img/kde-2025/spectacle.png)

### La configuration d’une manière générale

Plasma permet de configurer énormément de chose, de manière globale (raccourcis claviers, comportement des coins du bureau, apparence) mais également application par application, vous aurez la main pour enrichir ou simplifier les barres d’outils à votre guise.

![toolbar-config](/img/kde-2025/toolbar-config.png)
*Personnalisation de la barre d'outil de l’application Dolphin*

### Clip board manager mon amour
J’ai vécu sans pendant des années, mais en rédigeant cet article j’ai évidemment bougé et rebougé des textes et des adresses de fichiers dans tous les sens, et c’est bien rageant de vouloir coller un texte qu’on avait copié auparavent, mais écrasé par un autre texte entretemps. Le Clipboard manager règle ce problème, en gardant en mémoire les 20 derniers bouts de texte que vous avez copiés.

![clipboard manager](/img/kde-2025/clipboard-manager.png)

*Mince je voudrais coller le truc que j’avais copié tout à l’heure ! Pas de problème*


## Quoi de pire ?

GNOME a une forme d’élégance minimaliste qu’il est très difficile d’égaler. Plasma et
ses applications ont une approche opposée : plein de fonctionnalités, plein de boutons, et
cela se fait souvent au détriment de l’esthétique et de la lisibilité. La configuration
proposée par défaut était bien trop chargé, notamment les barre d’outils des applications
pouvaient s’avérer vraiment immondes (Okular, je t’ai vu).

Ça peut se régler une fois qu’on a réalisé qu’on pouvait retirer les éléments superflux de l’interface,
mais ça peut être un repoussoir pour les utilisateurs habitués à avoir mois d’options présentées, ou une
meilleure hiérarchie des éléments visibles.

Malheureusement je n’ai pas trouvé d’alternatives sérieuses à Firefox ou Thunderbird (non Trojita ne compte pas, et Kmail est trop lourdingue). Donc je ne peux pas me passer totalement des bibliothèques Gtk.



## Pourquoi pas ?

Si vous passez beaucoup de temps à manipuler des fichiers, lire des PDFs ou images dans votre utilisation de votre bureau, vous devriez tester **Plasma**. Un peu d’élagage dans les barres d’outils sera peut-être nécessaire, mais vous pourrez vous forger votre interface personnelle et garder sous la main les actions qui vous sont utiles.

Si vous êtes un·e grand·e fan de l’esthétique minimaliste de **GNOME**, vous risquez d’être déçu·e, et de rebrousser chemin assez vite.
