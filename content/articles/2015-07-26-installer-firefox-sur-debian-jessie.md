---
title: "Installer Firefox sur Debian Jessie"
Date: 2015-07-26T16:20:00Z
Category: Logiciels libres
Tags: 
- "Firefox"
- "Debian"
Slug: installer-firefox-sur-debian-jessie
Summary: Comment installer le vrai Firefox sur Debian Jessie
---


*Ceci est un recyclage de mon article de 2013 sur comment installer Firefox dans la version précédente de Debian. Je viens de tester sur une Debian Jessie toute fraîche et les instructions sont toujours valables.*

![Firefox sous Debian Jessie](/img/firefox-debian-jessie.png)

Debian ne fournit pas Firefox directement. Pour des raisons légales, Debian choisit de fournir à la place Iceweasel, qui est Firefox avec un nom et un logo différent. Je n’ai pas de problème avec ça, sauf que certaines extensions de Firefox ne fonctionnement pas avec Iceweasel.

Heureusement, le projet Ubuntuzilla permet d’installer les dernières versions de Firefox, Seamonkey et Thunderbird sur toute distribution dérivée de Debian, au moyen d’un dépôt Debian.

Voici la marche à suivre.

On désinstalle Iceweasel, et/ou Icedove :

    sudo apt-get purge iceweasel

    sudo apt-get purge icedove

On ajoute le dépôt ubuntuzilla, dans ses sources.
On modifie la liste de sources ou en crée une exprès pour ça. Par exemple

    sudo nano /etc/apt/sources.list.d/mozilla.list

On y insére la ligne suivante :

    deb http://downloads.sourceforge.net/project/ubuntuzilla/mozilla/apt all main

Il faut ensuite ajouter la clé du dépôt à votre keyring:

    sudo apt-key adv --recv-keys --keyserver keyserver.ubuntu.com C1289A29

Vous n’avez plus qu’à mettre à jour votre base de données de paquets :

    sudo apt-get update

Puis vous pouvez installer le programme voulu

    sudo apt-get install firefox-mozilla-build
    sudo apt-get install thunderbird-mozilla-build
    sudo apt-get install seamonkey-mozilla-build

Ces versions sont en anglais, mais vous pouvez installer la traduction en français via la gestion des addons.
