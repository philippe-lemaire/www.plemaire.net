---
title: "10 trucs à savoir après une migration vers Linux"
Date: 2014-12-07T09:00:00Z
Category: Logiciels libres
Tags: 
- "Linux"
Slug: 10-trucs-a-savoir-apres-une-migration-vers-linux
Summary: Guide pour s’y retrouver dans ce monde de barbus quand on vient de Windows
---

Ça y est, vous avez fait le grand pas, et vous avez installé une distribution GNU/Linux sur votre PC pour la première fois. Ça fonctionne, vous avez un menu, des applications installées par défaut, tout baigne.

Pourtant, vous êtes sans doute un peu perdus, hors de votre zone de confort. Comment gérer tel ou tel problème futur, quels sont les réflexes que vous avez acquis en utilisant Windows qui ne s’appliquent pas ici, où trouver de l’information ?

J’ai compilé une liste de 10 choses que j’ai apprises avec le temps en utilisant Linux comme système d’exploitation principal voire unique depuis bientôt 10 ans.

#### 1 - Les paquets et leur gestion

En venant du monde Windows, vous êtes habitués au mode de fonctionnement suivant pour ajouter un programme sur votre ordinateur :

1. Aller sur le web et chercher le programme, sur un site annuaire de logiciels ou sur le site officiel du logiciel
2. Chercher un lien pour le télécharger
3. Exécuter le fichier d’installation téléchargé
4. Cliquer sur suivant jusqu’à ce que le logiciel soit installé

Pour retirer un programme, vous alliez dans "ajouter / supprimer un programme", vous laissiez Windows faire péniblement la liste des choses installées, et vous trouviez votre programme à désinstaller dans cette liste.

Les mises à jour des logiciels utilisaient des méthodes variables, plus ou moins pénibles.

Oubliez tout ça, et vous ne le regretterez pas.

Les distributions Linux utilisent généralement un système centralisé de gestion de paquets qui permet d’installer et de désinstaller tout logiciel depuis une interface centrale.

Un paquet est un ensemble de fichiers constituant un programme, plus des métadonnées (nom du programme, numéro de version, paquets dont il dépend), et éventuellement une série de commandes à exécuter après l’installation ou la désinstallation du paquet.
L’ensemble des logiciels de votre installation est décomposées en paquets, du noyau Linux à votre navigateur internet.

Vous disposez d’au moins un logiciel permettant de réaliser les opérations suivantes :

1. Mettre à jour l’ensemble des paquets ayant une version plus récente disponible
2. Chercher un paquet par son nom, sa description
2. Installer un ou plusieurs paquets d’un coup, avec les paquets supplémentaires dont ils ont besoin pour fonctionner, leur dépendances
2. Désinstaller un ou plusieurs paquets, et leurs dépendances non utilisées par d’autres paquets

Les logiciels pour gérer ces opérations varient d’une distribution à l’autre. Sur Ubuntu et Xubuntu, c’est le rôle de la "Logithèque Ubuntu", sur Debian, vous pouvez utiliser Synaptic.

Ces interfaces graphiques sont en réalité des surcouches par dessus des commandes que vous pouvez directement passer dans un terminal. Voir [apt-get](http://doc.ubuntu-fr.org/apt-get) pour les distributions Debian et ses dérivées comme Ubuntu.

#### 2 - Les drivers

Un driver est un bout de logiciel qui fait fonctionner un périphérique de votre ordinateur comme la carte graphique, la carte son, le clavier, la souris, votre clé USB, etc.

Sous Windows, un driver est installé à chaque fois que vous branchez un périphérique USB classique. Bizarrement, si vous branchez le même périphérique dans une autre prise USB, Windows devra recommencer l’opération. Pour la carte graphique, vous devez généralement aller sur le site de son constructeur et chercher votre driver, puis le mettre à jour régulièrement pour bénéficier de bonnes performances 3D.

Sous Linux, la chose est un peu différente. Le noyau Linux lui-même se charge dans la plupart des cas de piloter les périphériques. Vous branchez un disque, un clavier, une souris, une caméra USB, et ces périphériques vont fonctionner immédiatement, sans installer de driver. Vous pouvez jeter le CD-ROM qui venait avec votre caméra ou votre graveur de DVD.

Il y a 2 types de périphériques cependant où vous aurez peut-être besoin de faire quelques efforts supplémentaires pour installer les paquets de pilotes propriétaires, qui ne sont pas installés par défaut.
Votre carte réseau Wi-Fi peut exiger un pilote propriétaire pour fonctionner. Si vous avez une carte graphique AMD ou Nvidia, elle fonctionnera peut-être mieux avec le driver propriétaire.

Ubuntu dispose d’un module de recherche de drivers propriétaires qui s’occupera de ces cas pour vous.

Sur Debian, installer le paquet "firmware-linux-nonfree" devrait gérer le cas des pilotes de carte réseau propriétaires. Vous devrez peut-être vous brancher à votre box internet par cable ethernet le temps d’installer ce paquet avant de pouvoir utiliser le Wi-Fi.  
Pour votre carte graphique, regardez par ici [pour les cartes Nvidia](https://wiki.debian.org/fr/NvidiaGraphicsDrivers) et [pour les cartes AMD ou ATI](https://wiki.debian.org/fr/ATIProprietary)

#### 3 - Trouver un logiciel équivalent à logiciel propriétaire

C’est une des principales barrières quand on débarque du monde Windows. Quel logiciel va remplacer ce logiciel que vous utilisez sous Windows ?

Dans la plupart des cas, un équivalent existe, mais encore faut-il connaître son nom.

Voici une petite liste, ainsi qu’un site qui répertorie les logiciels libres par catégories.

##### Navigateurs
Internet Explorer > Mozilla Firefox ou Chromium

##### Suite bureautique
Pack Office (Word, Excel, PowerPoint) > LibreOffice (Writer, Calc, Impress)

Adobe PDF viewer > Evince ou Okular

##### Multimedia
iTunes > Rhythmbox, Clementine

Lecteur vidéo > Totem, VLC, mplayer

##### Communication
Skype est disponible sous Linux.  
Le plugin Google Hangout également (chez moi fonctionne beaucoup mieux que Skype).

Les récentes versions de Firefox intègrent un système de chat vidéo qui pourra remplacer ces deux services.  
Pour le chat texte, empathy est compatible avec les protocoles de google talk, MSN messenger, Yahoo, etc…

Pour une liste beaucoup plus complète, consultez [l’annuaire Framasoft des logiciels libres](http://www.framasoft.net/rubrique2.html)

#### 4 - Logiciels propriétaires disponibles
Si les équivalents libres ne vous satisfont pas, il existe quelques logiciels propriétaires créés pour tourner sous Linux. En règle générale, ils sont distribués sous la forme de paquets Debian ou Ubuntu (fichiers .deb) qui une fois installés peuvent être mis à jour par le système de paquets.

Voici une petite liste, à vous de les trouver :

* Google Chrome
* Skype
* Adobe PDF Reader
* Spotify
* Adobe Flash

#### 5 - Le système de fichiers et les disques externes

Sous Windows, les différents disques de votre système sont représentés par des lettres.

C:\ est la racine de votre premier disque dur. A:\ et B:\ représentaient votre disquette et disque souple historiquement, mais je doute que vous ayez ces disques actuellement.

Lorsque vous branchez d’autres disques, leur racine est représentée par une autre lettre, et chaque disque est séparé ainsi des autres.

Le système de fichier utilisé par Linux est différent.

Vous avez une racine unique, /

Chaque disque va prendre sa place dans un certain dossier dans le système de fichier. On dit qu’il est monté dans un dossier.

Par exemple, mes documents personnels sont dans un disque séparé des logiciels et du système.
Pourtant, mes documents sont rangés dans "/home/phil/" comme ils le seraient si je n’avais qu’un disque.
Il s’avère que mon second disque est "monté" dans /home, alors que mon premier disque est monté dans /

Si vous branchez un disque dur, il va se monter dans un dossier du genre /media/user/usb1 par exemple.

#### 6 - Où et comment trouver de l’aide

Si vous coincez, le plus simple est de rechercher votre problème via Google. Ajoutez simplement "debian" ou "ubuntu" dans les mots-clés de votre recherche.

Vous trouverez la plupart du temps la réponse à vos problèmes sur des forums d’utilisateurs de votre distribution. Faites toutefois attention à la date des conversations sur les forums, ce qui était une solution en 2007 ne l’est sans doute plus.

Une bonne source d’information fraîche et bien rangée : le wiki de votre distribution.
Voici le [wiki ubuntu francophone](http://doc.ubuntu-fr.org/wiki) et le [wiki debian francophone](https://wiki.debian.org/fr/FrontPage).

#### 7 - Outils de maintenance habituels (Défragmentation, anti-virus, anti-malware)
Oubliez ça, inutile :)

#### 8 - Les différents environnements de bureau
Windows utilise une seule interface par version majeure, avec généralement un bureau sur lequel on pose son bazar, et une barre dans laquelle on trouve le bouton Démarrer, les logiciels qui tournent, un "systray" qui se remplit d’icônes sans qu’on ait rien demandé, et la date.

Dans le monde Linux, il existe différents environnements de bureau, qui s’écartent plus ou moins du fonctionnement auquel vous êtes habitués sous Windows.

Vous avez ainsi le choix entre :

* Unity qui est l’interface par défaut d’[Ubuntu](http://www.ubuntu.com), et exclusive à cette distribution
* [GNOME](http://www.gnome.org) : design sobre et moderne, interface très pilotable au clavier, applications cherchant à avoir le minimum de boutons et entrées menu. Utilisée par défaut dans [Debian](http://www.debian.org), [Fedora](http://fedoraproject.org/fr/) et [Ubuntu Gnome](http://ubuntugnome.org/)
* [Xfce](http://www.xfce.org) : fonctionnement plus proche de Windows, simple et très léger. Recommandé pour ceux qui ont une machine un peu ancienne, ou ne veulent pas bousculer leurs habitudes. Utilisé par défaut dans [Xubuntu](http://www.xubuntu.org).
* [KDE Plasma Desktop](https://www.kde.org/workspaces/plasmadesktop/), souvent appelée "KDE" pour des raisons historiques. Extrèmement malléable, cette interface peut resembler à Windows 7 par défaut, mais peut être configurée pour se comporter comme MacOS, GNOME, ou Windows 98…
* Pantheon qui est l’interface de la distribution [ElementaryOS](http://elementaryos.org/), qui ressemble à MacOS X en très simplifié.

#### 9 - Jeux vidéos

Pour les joueurs, la plateforme de référence reste et restera sans doute longtemps Windows.  
Cependant, de plus en plus de jeux, surtout indépendants, ont des versions Linux.

2 bonnes sources pour les trouver :

* [Steam](http://store.steampowered.com/search/?term=&sort_by=_ASC&os=linux&page=1)
* [Humble Bundle](https://www.humblebundle.com)

#### 10 - Pour aller plus loin

Si vous êtes super à l’aise avec tout ça, alors à vous de contribuer ! 

Après tout, le logiciel libre est un effort collectif, et pour dans la majorité des cas bénévole.

Même sans être développeur, vous pouvez contribuer en : 

* traduisant des logiciels ou des pages de wiki
* aidant les utilisateurs débutant sur les forums
* rédigeant des billets et tutoriels sur votre site
* faisant une donation à vos projets préférés
