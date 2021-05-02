---
title: "Comment installer Xfce 4.10 dans Debian Wheezy"
Date: 2013-06-12T00:20:00Z
categories: 
- "Logiciels libres"
Tags: 
- "Debian"
- "Xfce"
- "Linux"
Slug: comment-installer-xfce-4-10-dans-debian-wheezy
Summary: Tutoriel pour installer Xfce 4.10 dans Debian Wheezy
---


Salut à tous,
Petit tutoriel pour installer la nouvelle version de [Xfce](http://www.xfce.org/) dans [Debian](http://www.debian.org/) Wheezy, la version stable à l’heure où je vous écris.

Premièrement, si ce n’est déjà fait, vous pouvez installer Debian Wheezy en vous procurant une [image CD](http://www.debian.org/CD/).

Choisissez l’architecture qui correspond à votre PC, et le type de CD : Xfce ou netinstall.

Wheezy a la version 4.8 de Xfce, mais la version 4.10, qui apporte des [améliorations sympathiques](http://www.xfce.org/download/changelogs/4.10), est disponible dans la version testing.

On va donc déclarer que la version stable est notre version de prédilection :

(en tant que root) : 

    nano /etc/apt/apt.conf.d/local

Dans ce fichier, que l’on crée s’il n’existait pas, on ajoute :

    APT::Default-Release "stable";

Dans le fichier de sources de apt, on va ajouter un ligne pour testing :

(en tant que root) : 

    nano /etc/apt/sources.list

On ajoute la ligne :

    deb http://ftp.fr.debian.org/debian/ testing main

On met à jour la base de données de paquets avec :

(en tant que root): 

    apt-get update

Et il n’y a plus qu’à installer le paquet xfce4 en précisant qu’exceptionnellement on veut le prendre dans testing :

(en tant que root) : 

    apt-get -t testing install xfce4

La fonctionnalité que je préfère dans Xfce 4.10 : la possibilité de mettre en mosaïque une fenêtre sur la moitié de l’écran, à la souris en la glissant vers le bord, ou au clavier (à vous de régler les raccourcis clavier voulus dans "paramètres, gestionnaire de fenêtres, clavier".

Et voilà le travail :

![Capture d’écran](/img/Capture-décran-11062013-074244.png)

