---
title: "Comment avoir un menu global dans KDE"
Date: 2014-01-09T10:30:00Z
categories: 
- "Logiciels libres"
Tags: 
- "KDE"
- "Linux"
- "Logiciel libre"
- "Arch Linux"
Slug: comment-avoir-un-menu-global-dans-kde
Summary: Une menu global à la Mac OSX ou Unity avec KDE, c’est possible !
---


## C’est quoi un menu global ?
L’idée d’un menu global est d’afficher le menu de la fenêtre active dans le tableau de bord au lieu de la fenêtre active elle même.

Plusieurs avantages :

* vous gagnez de la place dans vos fenêtres
* le menu est toujours au même endroit
* les fenêtres peuvent être étroites tout en ayant leur menu entièrement affiché : application de chat, client twitter par exemple

Inconvénients :

* aller dans le menu d’une fenêtre non active prend un clic de plus
* potentiellement une grande distance à parcourir à la souris

## Quels sont les paquets à installer ?
Dans KDE, il y a un widget plasma pour afficher le menu.
Il vous faut donc l’installer ainsi que quelques paquets supplémentaires pour les applications Qt et éventuellement GTK2 / GTK3.

### Pour Arch Linux :
Depuis le [AUR](https://aur.archlinux.org) : (j’utilise packer comme gestionnaire pour les paquets du AUR.)

    sudo packer -S kdeplasma-applets-menubar

Dans les dépôts principaux :

    sudo pacman -S appmenu-qt

### Pour Ubuntu ou Linux Mint :

    sudo apt-get install appmenu plasma-widget-menubar

## Comment configurer ses widgets et son thème ? 
Vous avez deux choses à faire :

1. Insérer le widget appmenu dans votre tableau de bord
2. Régler Oxygen pour que le menu soit exporté dans le widget
![Réglage dans la configuration d’Oxygen](/img/kde-appmenu-oxygen.png)

## Et mes applications GTK ?
Pour que tout ça fonctionne aussi avec les applications GTK 2 et GTK 3, vous avez un peu plus de travail à faire.

### Pour Archlinux

Installer depuis le AUR :

    packer -s gtk2-appmenu gtk3-appmenu appmenu-gtk2

### Pour Ubuntu ou Linux Mint

    sudo apt-get install appmenu-gtk3 appmenu-gtk

### Modification du fichier settings de gtk3
Quelque soit votre distribution, vous allez devoir insérer cette ligne à la fin du fichier  `~/.config/gtk-3.0/settings.ini`

    gtk-shell-shows-menubar = 1

Déconnectez-vous de votre session et reconnectez vous.

## Et voilà le travail :
Une application gtk2 : Chromium.  
![Chromium avec menu global sous KDE](/img/kde-appmenu-gtk2.png)

Une application gtk3 : GIMP.  
![GIMP avec menu global sous KDE](/img/kde-appmenu-gtk3.png)

