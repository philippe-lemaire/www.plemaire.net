---
title: "KDE SC 4.10 est sortie !"
Date: 2013-02-09T00:20:00Z
categories: 
- "Logiciels libres"
Tags: 
- "KDE"
- "Linux"
Slug: kde-sc-4-10-est-sortie
Summary: Impressions et screenshots de la version 4.10 de KDE SC
---


## Quoi de neuf dans KDE 4.10 ?
À intervalles réguliers, les joyeux drilles derrière <a title="KDE SC" href="http://www.kde.org">KDE SC</a> sortent une <a title="L’annonce sur dot.kde.org" href="http://dot.kde.org/2013/02/06/410-release-plasma-workspaces-applications-and-development-platform">nouvelle version</a> de leur environnement de bureau libre, et comme à chaque fois, je suis pris d’une envie irrépressible de faire du <a title="Relevant xkcd" href="http://xkcd.com/456/">distro-hopping</a>.

Hier soir, j’ai remplacé ma brave <a title="CrunchBang" href="http://crunchbang.org/about">CrunchBang Waldorf</a>, excellente distribution par ailleurs, par <a title="Le site de Kubuntu" href="http://www.kubuntu.org">Kubuntu</a> 12.10. Au premier reboot, j’ai ajouté le ppa kubuntu backports qui apporte les derniers paquets KDE. Un **sudo apt-get update &amp;&amp; sudo apt-get dist-upgrade** plus tard, KDE 4.10 était installé et fonctionnel.

De prime abord, l’aspect graphique était complètement corrompu. J’ai essayé de rétablir les réglages par défaut des thèmes Plasma et Qt, mais rien à faire. Il s’avère que KDE stocke du cache, un peu comme un navigateur, et mon dossier ~/.kde qui contenait tous mes réglages KDE, contenait du cache de la version 4.9 qui créait ces désagréments. Un petit **rm -r ~/.kde**, déconnexion / reconnexion, et KDE 4.10 était en place et c’est une petite merveille.

Quoi de neuf dans cette nouvelle version ? En surface, pas énormément de changements par rapport à la version 4.9 :

* un nouveau [fond d’écran par défaut](/img/plasma-empty.jpg) (qui n’est vraiment pas à mon goût)
* de nouvelles animations lorsqu’une fenêtre est maximisée / réduite
* Une option un poil masquée pour mettre le [menu d’une application dans un bouton de la barre de fenêtre](/img/kwin-appmenu.gif)

Mais sous le capot, les améliorations de la structure qui fait tourner toutes ces applications ont l’air importantes. Je verrai dans la durée si le système est plus stable et plus agréable à utiliser qu’il y a un an.

Allez un petit screenshot de ma config :
![Screenshot](/img/capture.png)

## Non mais qu’est-ce que c’est que ce binz ?!
Ces derniers mois, le bureau linux a connu énorméments de changements :

* GNOME a jeté à la poubelle le modèle traditionnel de bureau qu’utilisait GNOME 2, pour partir dans une direction très différente avec <a title="GNOME 3" href="http://www.gnome.org/gnome-3/">GNOME 3</a>
* des développeurs qui devaient vraiment aimer GNOME 2 l’ont forké, donnant naissance à <a title="MATE Desktop" href="http://mate-desktop.org/">MATE</a>
* <a href="http://www.ubuntu.com">Ubuntu</a>, qui utilisait GNOME 2 jusque là,  a créé sa propre interface <a href="http://unity.ubuntu.com/">Unity</a>, proche techniquement de GNOME 3, mais fonctionnellement tendant vers OS X d’Apple (menu global, dock, boutons des fenêtres à gauche)
* <a title="Xfce" href="http://www.xfce.org">Xfce</a> restait toujours le même, léger et traditionnel, s’améliorant lentement mais sûrement.
* Linux Mint, ne voulant utiliser ni Unity ni GNOME 3, lançait son environnement <a title="Cinnamon" href="http://cinnamon.linuxmint.com/">Cinnamon</a>, basé sur les mêmes technos que GNOME 3, mais avec une approche plus traditionnelle de l’interface.
* Les personnes hyper trendy derrière le <a title="Elementary sur Deviant Art" href="http://danrabbit.deviantart.com/art/elementary-gtk-theme-83104033">thème elementary</a> se sont lancées dans leur propre distribution dérivée d’Ubuntu : <a title="Plus Mac OSX, tu meurs" href="http://elementaryos.org/">elementary OS</a>.
* Les über-geeks restèrent sur leurs Window Managers customisés : <a title="Xmonad, un WM en mosaïque" href="http://xmonad.org/">Xmonad</a>, <a title="Openbox, un WM flotant" href="http://openbox.org/">Openbox</a>

Ce fut une période de grands mouvements de population, les utilisateurs d’Ubuntu, Linux Mint, Fedora, Debian, et tant d’autres, qui utilisaient toutes par défaut GNOME 2, se sont retrouvés avec toutes ces options plus ou moins abouties, et les distro-hoppers comme moi ont passé des heures à faire tour de toutes ces solutions.

Tout le monde y est allé de son <a title="Linus himself bashes GNOME 3" href="https://plus.google.com/102150693225130002912/posts/UkoAaLDpF4i">coup de gueule contre GNOME 3</a>, contre Unity, contre les conservatismes qui poussent des gens à forker des technos vieillissantes…

Pendant ce temps là, KDE poursuivait son petit bonhomme de chemin. KDE avait fait sa révolution plus tôt, en 2008, avec la version 4.0, et après avoir testé les 2 premières itérations de la série 4.x, j’avais laissé tombé KDE comme option viable.

Un peu plus de 4 ans plus tard, KDE a poursuivi sa voie, offrir un environnement de bureau au premier abord traditionnel, mais extrèmement personnalisable. À tel point qu’il est possible, sans ajout d’extension, de le faire se comporter presque tout comme :

* Windows XP
* Windows 7
* GNOME 3
* Unity
* OSX

Le revers de la médaille, c’est le nombre vertigineux d’options dans l’application de réglage du système. De quoi chopper la migraine quand on la découvre.

Au delà de l’environnement de bureau en lui-même, KDE est avant tout une collection d’applications libres, et à ce niveau, la qualité et le nombre de fonctionnalités (croissant, pas comme chez certains) des applications le place largement au dessus de la concurrence. Encore une fois, on perd la simplicité des applis GNOME ou Xfce, mais le gain en choix, souplesse, personnalisation, et fonctionnalités compense largement. Mon seul grief est le manque de cohérence de l’ensemble en terme de design des applications. C’est là que KDE a encore le plus de marge de progression à mon humble avis.

En résumé, le libre c’est un peu le bazar parce que chacun est libre de donner vie à sa vision, mais au bout du compte l’utilisateur a l’embarras du choix, et on a connu pire comme problème.
