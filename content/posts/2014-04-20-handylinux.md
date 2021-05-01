---
title: "HandyLinux, Debian sans se prendre la tête"
Date: 2014-04-20T16:00:00Z
categories: 
- "Logiciels libres"
Tags: 
- "Linux"
- "Debian"
- "Xfce"
Slug: handylinux-debian-sans-se-prendre-la-tete
Summary: Aperçu d’une distribution GNU/Linux made in France, visant les débutants.
---

#### Introduction

[HandyLinux](http://handylinux.org/) est une distribution basée sur Debian et conçue pour offrir le maximum de fonctionnalités en un minimum d’efforts.
Elle cible plus particulièrement les débutants sous GNU/Linux, avec une interface très inspirée des versions récentes de Windows, son choix d’applications par défaut, et son menu de lancement original.

#### Installation

HandyLinux fournit des [images disques d’installation](http://handylinux.org/documentation/doku.php/obtenir_handylinux) sur son site officiel. Ce sont des images "live", qui permettent d’essayer la distribution sans l’installer sur le disque dur. Pour les besoins de cet article, je l’ai installée dans une machine virtuelle.

Si vous choisissez d’installer HandyLinux vous serez amenés sans grande surprise à utiliser le programme d’installation de Debian, mis aux couleurs d’HandyLinux.

![Installation HandyLinux 1](/img/handylinux/handylinux-install1.png)

![Installation HandyLinux 2](/img/handylinux/handylinux-install2.png)

Pour ne pas dérouter les débutants, le programme d’installation n’offre pas l’option d’utiliser l’installation "expert" de Debian, qui permet de réaliser l’installation étape par étape et de changer certaines options.
Toutefois, une partie assez délicate de la procédure pour les plus grands débutants est inévitable : la gestion du disque dur et des partitions.
Ici, les débutants choisiront l’option de laisser le programme d’installation gérer comme il l’entend l’espace disque, et les utilisateurs plus avancés pourront gérer leur partitions.

![Installation HandyLinux 3](/img/handylinux/handylinux-install3.png)

#### Spécificités

Une fois l’installation terminée, et connecté au compte utilisateur que vous aurez créé lors de celle-ci, vous êtes accueilli par ce sympathique écran :

![Écran accueil HandyLinux](/img/handylinux/handylinux-ecran-accueil.png)

Votre œil expert aura peut-être reconnu un bureau Xfce avec un thème inspiré de Windows 8.
Le bouton en bas de cette fenêtre d’accueil lance le navigateur par défaut (Chromium) sur un guide html installé en local.

![Le site local de documentation](/img/handylinux/handylinux-documentation.png)

Ce guide vous mènera également au [site de documentation d’HandyLinux](http://handylinux.org/wikimenu/) qui est très bien fait, entièrement en français, et habillé à l’image de la distribution.
Il y a même une [version pour utilisateurs avancés](http://handylinux.org/documentation/doku.php).

HandyLinux utilise un menu de lancement maison, qui ouvre cette fenêtre :

![HandyLinux menu internet](/img/handylinux/handylinux-menu-internet.png)

Les onglets dans cette fenêtre vous amènent sur les différentes catégories de logiciels installés.

![HandyLinux menu multimedia](/img/handylinux/handylinux-menu-multimedia.png)

Dans la partie aventuriers se trouvent en fait les outils de configuration du bureau Xfce et les utilitaires d’administration classique Debian tels que Synaptic.

![HandyLinux menu aventuriers](/img/handylinux/handylinux-menu-aventuriers.png)

La case à cocher "fermer après l’execution" (*sic*) sert à fermer ce menu après avoir lancé un de ces items. Personnellement je n’ai pas de problème avec cette formulation, mais je ne suis pas sûr que le public visé comprenne bien que ce menu est lui même une fenêtre, qui peut être fermée et relancée, ou bien laissée ouverte.

Si ce menu de lancement n’est pas à votre goût, vous pouvez le retirer du panneau et y ajouter le menu classique Xfce à la place.

![HandyLinux menu Xfce](/img/handylinux/handylinux-menu-xfce.png)

#### Logiciels installés

HandyLinux a fait le choix du pragmatisme et du confort pour les utilisateurs débutants, quitte à renoncer à ne contenir que du logiciel libre.
Par défaut, vous aurez donc :

* Le navigateur Chromium
* LibreOffice
* Le lecteur vidéo VLC
* Le lecteur audio QuodLibet
* Le gestionnaire d’images / visionneuse Shotwell
* Skype
* Icedove (Thunderbird sans le logo ni le nom, pour des raisons légales)

C’est une très bonne sélection d’applications, on reste dans le très léger avec Quodlibet pour la musique, et la suite habituelle d’applications Xfce.
La présence de Skype est discutable, mais personnellement je l’installe sur tous les postes Linux de la famille, donc l’avoir de base est bien commode.

#### Conclusion

HandyLinux vise les débutants, et leur apporte la stabilité de Debian et le confort d’avoir toutes les applications usuelles pour une utilisation standard préinstallées.

Si vous êtes un utilisateur plus avancé, elle peut être un moyen simple et rapide d’installer une debian prête à l’emploi, quitte à passer quelques secondes à changer le menu de lancement des applications.

Dans la catégorie des distributions à installer sur le PC de vos proches, machines sur lesquelles vous souhaitez avoir le minimum de maintenance à faire, elle se place aisément dans le trio de tête avec [Xubuntu](http://www.xubuntu.org) et [Linux Mint MATE](http://blog.linuxmint.com/?p=2493). Le long cycle de développement des versions de Debian est ici un avantage par rapport aux autres distributions citées, qui sortent une nouvelle version tous les 6 mois.

De plus, c’est vraiment agréable d’avoir une documentation accessible et rédigée en français. Dans la pratique, je doute fort que mes proches fassent l’effort d’aller la lire, mais pour une personne volontaire pour en apprendre un peu plus, c’est un plus indéniable.

Seul regret, pas de version 64 bits, mais c’est en projet apparemment.
