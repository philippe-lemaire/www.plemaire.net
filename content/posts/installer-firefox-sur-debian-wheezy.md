---
title: "Installer Firefox sur Debian Wheezy"
Date: 2013-09-09T09:20:00Z
categories: 
- "Logiciels libres"
Tags: 
- "Firefox"
- "Debian"
Slug: installer-firefox-sur-debian-wheezy
Summary: Comment installer le vrai Firefox sur Debian Wheezy
---


Debian est une distribution GNU/Linux qui offre de nombreux avantages sur nombre de ses concurrentes : stabilité, immense dépôt d’applications pré-empaquetées, philosophie libre. Elle a de ce fait "engendré" un très grand nombre de distribution dérivées, comme ubuntu, linux mint, et crunchbang.

Debian ne fournit malheureusement pas Firefox. Pour des raisons légales, Debian choisit de fournir à la place iceweasel, qui est Firefox avec un nom et un logo différent. Je n’ai pas de problème avec ça, sauf que certaines extensions de Firefox ne fonctionnement pas avec iceweasel.

Heureusement, le projet ubuntuzilla permet d’installer les dernières versions de Firefox, Seamonkey et Thunderbird sur toute distribution dérivée de Debian, au moyen d’un dépôt Debian.

Voici la marche à suivre.

On désinstalle Iceweasel, et/ou Icedove :

    sudo apt-get purge iceweasel

    sudo apt-get purge icedove

On ajoute le dépôt ubuntuzilla, en insérant la ligne suivante :

    deb http://downloads.sourceforge.net/project/ubuntuzilla/mozilla/apt all main

soit dans /etc/apt/sources.list
soit dans un fichier finissant en .list dans le dossier /etc/apt/sources.list.d/

Il faut ensuite ajouter la clé du dépôt à votre keyring:

    sudo apt-key adv --recv-keys --keyserver keyserver.ubuntu.com C1289A29

Vous n’avez plus qu’à mettre à jour votre base de données de paquets :

    sudo apt-get update

Puis vous pouvez installer le programme voulu

    sudo apt-get install firefox-mozilla-build
    sudo apt-get install thunderbird-mozilla-build
    sudo apt-get install seamonkey-mozilla-build

Ces versions sont en anglais, mais vous pouvez installer la traduction en français via la gestion des addons.
