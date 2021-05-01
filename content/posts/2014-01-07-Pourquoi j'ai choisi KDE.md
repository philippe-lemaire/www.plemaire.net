---
title: "Pourquoi j’ai choisi KDE"
Date: 2014-01-07T10:30:00Z
categories: 
- "Logiciels libres"
Tags: 
- "KDE"
- "Linux"
- "Logiciel libre"
Slug: pourquoi-j-ai-choisi-kde
Summary: Ou comment j’ai cheminé du fanboy GNOME à KDE en passant par les gestionnaires de fenêtres en mosaïque.
---


#### Pourquoi j’ai initialement choisi GNOME 2

[Ubuntu](http://www.ubuntu.com) entre 2004 et 2010 utilisait GNOME 2. J’ai découvert Linux avec Ubuntu 5.04, et j’ai utilisé GNOME 2 jusqu’en 2011.

Ça ressemblait à ça :  
![Ubuntu 5.04](/img/ubuntu-5.04.jpg)

GNOME 2 était simple, et relativement peu gourmand en ressources.
Il avait un look rondouillard et sympathique.
Il était personnalisable avec masse de thèmes et de petits applets dans les panneaux, mais la gestion du positionnement des applets était lourdingue.

GNOME 2 manquait des fonctionnalités modernes 3D comme l’exposition des fenêtres ouvertes, certaines animations de transition entre bureau…

La réponse de GNOME fut de repenser radicalement son expérience utilisateur et de faire un grand bond en avant avec GNOME 3.

#### Pourquoi je n’utilise pas GNOME 3

GNOME 3 offre un workflow radicalement différent.
L’objectif affiché est de vous laisser vous concentrer sur une tâche en cours, et de minimiser la pollution visuelle des éventuelles autres fenêtres ouvertes.

Pour passer d’une fenêtre à une autre, vous avez 2 options :

1. Utiliser le raccourci clavier Alt-Tab
2. Basculer sur la vue de sélection de fenêtre, en poussant votre souris vers le coin supérieur gauche ou d’une pression de la touche "Windows" de votre clavier.
Vous avez droit à une présentation des fenêtres ouvertes sur l’espace de travail en cours, et sur la droite vous pouvez voir les autres espaces de travail, et y déposer des fenêtres.

![Vue de sélection de fenêtre dans GNOME 3.10](/img/gnome-window-selection-3.10.png)


On peut dire ce qu’on veut sur ce workflow, mais on ne peut pas enlever à GNOME la qualité de sa présentation.
C’est aéré, bien aligné, et minimaliste.
Mais ce n’est pas pour moi.

C’est lorsque je me suis mis à travailler véritablement sur mon ordinateur personnel que j’ai compris à quel point le workflow pensé pour GNOME 3 ne me convenait pas.
Mon problème est que lorsque je travaille, j’ai besoin de nombreux outils ouverts : 

* un [éditeur de texte](http://www.vim.org) 
* un navigateur 
* un [outil de manipulation d’image](http://www.gimp.org)
* un gestionnaires de fichiers
* un visionneur d’image, et [libreoffice](http://www.libreoffice.org) ou un visionneur de document PDF pour afficher les contenus textes rédigés par mes clients.

Avec de nombreuses fenêtres ouvertes, GNOME 3 devient fastidieux à utiliser.
Le mode Alt-Tab présente de grosses icônes d’application et de minuscules fenêtres, et a un comportement pénible si vous avez plusieurs instances du même programme qui tournent.
Le mode présentation des fenêtres est joli mais ne présente pas d’icône d’application.
Si vous avez beaucoup de fenêtres présentées, vous pouvez perdre du temps à hésiter pour savoir quelle fenêtre vous voulez sélectionner.

#### La grande errance
Ce fut pour moi une période de grande instabilité, j’ai essayé un grand nombre d’alternatives.

##### MATE
[MATE](http://mate-desktop.org) est un fork de GNOME 2, dont l’objectif est de maintenir le look and feel de GNOME 2. Il m’a été bien utile pour les membres de ma famille que j’avais convertis à Linux avec [Ubuntu](http://www.ubuntu.com) + Gnome 2.  
Il souffre des mêmes limitations que GNOME 2, et dans les premières versions que j’ai essayées, d’un manque manifeste de développeurs. 

En remplaçant massivement le terme "gnome" par "mate" dans leur code, ils avaient ainsi cassé certaines fonctionnalités comme la gestion des touches multimédia du clavier pour mettre en pause sa musique. 
Mauvais signe.

##### Xfce 
[Xfce](http://www.xfce.org) est intéressant pour une machine un peu ancienne. 
Il ressemble beaucoup à GNOME 2, en légèrement plus léger.
Mais il souffre des mêmes problèmes, il lui manque certaines fonctionnalités modernes comme un mode exposé pour présenter les fenêtres ouvertes.
##### Xmonad
[Xmonad](http://xmonad.org) est un gestionnaire de fenêtres en mosaïques (tiling window manager dans la langue de Shakespeare).

![Xmonad avec plusieurs écrans](/img/xmonad.jpg)

On change carrément de monde avec ce genre de workflow : vos fenêtres se disposent de manière à occuper tout l’écran, sans se superposer.
Vous ne pouvez pas les réduire, il faut jouer avec ses espaces de travail pour organiser tout ça.

Ça encourage à utiliser des applications à l’interface gérable au clavier, voire des applications qui vivent entièrement dans un terminal.
Et il y en a, pour tout : [email](http://www.mutt.org/), [multimedia](http://www.musicpd.org/clients/ncmpc/), [lecture de flux RSS](http://www.newsbeuter.org/)

##### i3
[i3](http://i3wm.org) est similaire à Xmonad. C’est aussi un gestionnaire en mosaïque.

![i3 avec vim, mplayer et git](/img/i3.png)

Il diffère de Xmonad dans sa gestion fine des conteneurs : dans une disposition de base, vous pouvez créer des subdivisions qui utilisent un modèle différent. Dans le screenshot ci-dessus, vous avez par exemple une division horizontale avec la fenêtre tout à gauche et le reste à droite. Dans la partie de droite, vous avez une subdivision verticale, avec Mplayer en haut et un autre terminal en bas. Enfin, dans le bloc du haut, vous avez une subdivision en onglets, avec 2 fenêtres, dont une masquée.

Vous pouvez faire ça à mesure que vous lancez vos applications. Ou après coup, mais avec plus de manipulations.

Ce modèle permet de créer sur chaque espace de travail une disposition taillée sur mesure.
C’est un modèle intéressant, mais qui pour mon usage a plusieurs limitations :

* C’est au final beaucoup de travail, il faut se concentrer sur ce qu’on fait avec ses fenêtres, et ça peut nuire au travail.
* Il faut dans une certaine mesure se rappeler où on a mis ses fenêtres. Catégoriser ses espaces de travail (web, terminal, graphisme) peut aider.
* C’est très difficile à utiliser dès que vous avez une main prise (téléphone, tasse de café). Ça a l’air bête mais dès qu’on a pas les deux mains sur le clavier on ne peut pratiquement plus rien faire.

#### La révélation : KDE
J’ai longtemps essayé [KDE](http://fr.kde.org), sans l’adopter.
Les dernières versions ont fait d’énormes progrès en terme de performance, ce qui m’a permis de passer à KDE comme environnement de bureau.

##### Idées reçues sur KDE
KDE souffre souvent d’idées reçues. Certaines de ces idées ont une base réelle, mais obsolète.

> C’est lent, c’est moche, c’est copié sur windows 95, les applications ont des noms débiles qui commencent par K.

Dans mon expérience, KDE offre des performances très satisfaisantes, meilleures que [GNOME 3](http://www.gnome.org) et [Elementary OS](http://elementaryos.org) par exemple.
Mais c’est sans doute une chose relativement récente, je ne parierai pas sur les performances d’une version antérieure à KDE 4.8.

Le look and feel du thème par défaut peut être un peu étrange quand on est habitué aux thèmes plus minimalistes côté GTK.
J’ai fini par l’adopter et même l’adorer, je ne supporte aucune alternative plus de 10 minutes.

Par défaut KDE a une barre des tâches effectivement proche de celle de Windows 95.
Mais on peut la remplacer par une barre des tâches à icônes, comme celle de Windows 7.  
On peut aussi s’en passer, à la GNOME 3, ou bien reproduire la disposition Unity d’[Ubuntu](http://www.ubuntu.com). 

Le nom des applications est parfois riche de K en effet, mais la tendance actuelle est de s’en éloigner, ou du moins de ne plus commencer systématiquement par un K.  
Exemples :

* [Dolphin](http://dolphin.kde.org/)
* [Choqok](http://choqok.gnufolks.org/)
* [Gwenview](http://www.kde.org/applications/graphics/gwenview/)
* [Okular](http://www.kde.org/applications/graphics/okular)

##### Mon expérience avec KDE
KDE est extrèmement personnalisable.
Peut-être trop, ça donne à son interface de réglages du système un nombre astronomique d’entrées.
Mais je préfère ça à l’excès inverse de GNOME 3.

Je façonne le workflow et l’interface que je veux :

* Disposition et contenu du ou des paneaux.
* Comportement et affichage du cyclage entre les fenêtres (Alt-Tab).
* Hot corners : la fonctionnalité exposé de GNOME 3 en déplaçant la souris dans un coin est utile à ses heures, et reproductible dans KDE.  
![L’exposition des fenêtres dans KDE](/img/kde-expose.png)
* Mise en mosaïque au clavier (présent dans Gnome 3.x et Xfce 4.10) : disposer deux fenêtres sur chacune sa moitié d’écran est un must. Pour moi c’est l’avantage clé des gestionnaires en mosaïque, sans les inconvénients.  
![KDE avec 2 fenêtres en mosaïque](/img/kde-tiling.png)
* Bureau en mode "Rechercher et lancer" : j’ai pour habitude depuis des années d’avoir un bureau sans dossiers ou raccourcis d’application. Un bureau sans fonctionnalité. Le mode "Rechercher et lancer" fait du bureau une espèce de menu le lancement des applications géant. Pratique pour lancer une application à la souris.  
![Bureau en mode "Rechercher et lancer"](/img/kde-rechercher-et-lancer.png) 
* Les dialogues de fichier. Un détail qui paraît bête, mais qui change la vie. Les dialogues de fichier de GTK sont atroces. Quand vous voulez y choisir un fichier image, sa vignette est minuscule. Quand vous voulez enregistrer un fichier sur votre disque, l’interface pour créer un nouveau dossier est incompréhensible. Les dialogues de fichier de KDE règlent tous ces problèmes.  
![dialogue de fichier KDE](/img/kde-file-dialog.png)

##### Distributions recommandées
Attention, ici je ne vais parler que des distributions que j’ai essayées plus d’une semaine.  
Je ne prétends pas faire un benchmark complet des distributions qui ont une version KDE.
Je ne mentionne pas [Fedora](http://www.fedora-fr.org) par exemple non pas parce que je ne l’apprécie pas, mais simplement parce que je ne l’ai pas essayée.


1. [Arch Linux](https://www.archlinux.org/) : ma distribution de choix. Les versions les plus récentes de tous vos logiciels à disposition, très peu de temps après leur sortie grâce à son modèle de rolling release.
2. [Kubuntu](http://www.kubuntu.org/) : ubuntu sous le capot, et un KDE "vanilla" par dessus. Une release tous les 6 mois, avec la dernière KDE dispo à chaque fois. Un dépôt ppa avec la toute dernière mouture de KDE est aussi disponible quand il y a un décalage entre les releases, ou si vous voulez rester sur une base "Long Term Support" de Kubuntu.
3. [Netrunner](http://www.netrunner-os.com/) est basée sur Kubuntu, avec une sélection de logiciels légèrement différente, et un look and feel propre. Si vous préférez son thème par défaut. Sinon pas de différence majeure avec Kubuntu.
4. [OpenSuse](http://fr.opensuse.org/Bienvenue_sur_openSUSE.org) a la réputation d’être la meilleure implémentation de KDE. Je ne reste jamais longtemps dessus, non par manque de qualité, mais parce que j’avoue avoir du mal à comprendre les bonnes pratiques avec leurs différents dépôts de logiciels. Je me sens plus à l’aise sous un système Debian ou Arch.
4. [Debian](http://www.debian.org/CD/) est un excellent choix si vous voulez installer un système et ne pas vous en inquiéter pendant plus de deux ans. La version actuelle de KDE dans Debian Stable est la 4.8.4. Bien, mais un peu frustrant pour qui suit les annonces de nouvelles fonctionnalités dans KDE.

##### Conclusion

Le bureau Linux est une affaire de choix, et de cas d’usage.  
Je n’ai rien contre GNOME ou Xfce, ce sont des environnements fantastiques s’ils correspondent à votre utilisation.

KDE vous offre la possibilité de le plier à votre workflow, et avec un peu de temps consacré à le configurer, vous en ferez ce que vous voulez. Il peut manquer de polish ici ou là, mais il offre par ailleurs la meilleure synthèse entre les workflows classiques (barre des tâches, minimisation) et modernes (tâches comme icônes, menus globlaux, exposé).
