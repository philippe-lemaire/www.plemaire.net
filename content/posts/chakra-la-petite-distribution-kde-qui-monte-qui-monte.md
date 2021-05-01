---
title: "Chakra la petite distribution KDE qui monte qui monte"
Date: 2013-06-29T00:20:00Z
categories: 
- "Logiciels libres"
Tags: 
- "Linux"
- "KDE"
Slug: chakra-la-petite-distribution-kde-qui-monte-qui-monte
Summary: Premières impressions sur Chakra, une distribution basée sur Arch Linux et le bureau KDE
---


#### Qu’est-ce que Chakra ?
<a href="http://chakra-project.org" target="_blank">Chakra</a> est une distribution linux qui était à l’origine un installeur simplifié de Arch Linux avec l’environnement de bureau <a href="http://www.kde.org" target="_blank">KDE</a>, qui est devenu une distribution indépendante, même si elle garde par certains aspects technique une filiation avec <a href="http://www.archlinux.org" target="_blank">Arch Linux</a>.

Là où Arch Linux utilise un modèle de rolling release (les paquets sont mis à jour en continu avec de nouvelles versions dès que celles-ci sont disponibles), Chakra utilise un modèle semi-rolling, où le cœur du système n’est pas mis à jour constamment, mais les applications les plus visibles de l’utilisateur le sont.

Chakra est distribuée sous la forme d’une ISO live, pour les processeurs 64bit uniquement.
Étant donnée la taille de l’ISO, il vous faudra une clé USB ou un DVD vierge pour procéder à l’installation.
Le choix de ne pas fournir de version 32bit peut surprendre, mais à moins d’avoir une machine vraiment ancienne, auquel cas utiliser KDE n’est pas une riche idée, ce n’est pas un problème majeur.

Même si vous ne comptez pas forcément l’installer, vous pouvez vous faire une idée de Chakra en démarrant l’ISO live sur votre machine. C’est l’occasion de tester la dernière release de KDE qui apporte pas mal de corrections de bogues depuis mon dernier billet à son sujet.
#### Pourquoi utiliser Chakra ?
Chakra est destinée aux utilisateurs qui veulent utiliser un système purement KDE, et veulent une installation simple et rapide. Les applications avec des dépendances GTK sont dans un dépôt "extra", désactivé par défaut. Personnellement j’ai fini par craquer au bout de quelques jours car malgré ses qualités, rekonq n’est pas au niveau de chromium ou firefox.

Dans son état actuel je ne la recommanderais qu’à des utilisateurs de linux expérimentés, mais si vous savez utiliser le wiki de Arch Linux, vous ne devriez rencontrer aucune difficulté insurmontable.
#### Points forts

* Des packages récents, avec le dernier KDE, systemd
* Une installation simple et rapide
* Un installeur qui vous laisser utiliser n’importe quelle disposition de clavier, même le bépo (contairement à Debian et Arch Linux)
* Un habillage de KDE élégant (thème caledonia)
* Un petit utilitaire qui apparait à la première connexion et qui permet de faire en quelques clics un premier paramétrage
* Les applications KDE, avec des fonctionnalités jusqu’au dents
* La puissance et la rapidité de pacman, sans les difficultés liées à l’installation et la maintenance d’une Arch Linux
* Firefox est fourni avec les patches de OpenSUSE qui le font mieux s’intégrer dans KDE : il utilise les dialogues de fichiers de KDE au lieu des horribles dialogues GTK par exemple

#### Points faibles

* Un installeur aux possibilités limitées en terme de gestion du disque dur, encryption…
* Un bug avec les locales mal paramétrées suite à l’installation, ce qui posait problème avec les fichiers et dossiers contenant des caractères accentués comme "~/vidéos". Facilement résolu en ajoutant "fr_FR.UTF-8 UTF-8" dans le fichier "/etc/locale-gen" et en regénérant les locales
* Besoin de se déconnecter puis reconnecter pour certaines choses, comme le thème oxygen-gtk, ou que le plugin flash fonctionne dans firefox, là où il suffit de quitter et relancer firefox dans d’autres distributions.
* Le manque de polish de KDE, sur certains détails comme le dimensionnement et la position des menus, pop-ups
* Le wiki et le site web sont loin d’être à jour. Par exemple le fait que chakra ait abandonné son système de bundle (qui permettait d’isoler complètement les applications GTK) remplacé par un dépôt extra à décommenter dans le fichier de conf de pacman n’est pas indiqué sur un grand nombre de pages du site, notamment leur page "about".
* attention, certains fichiers de votre partition /home seront écrasés sans sommation, par exemple mon ~/.bashrc a été remplacé par celui fourni par Chakra. Faites un backup de vos fichiers de config sensibles

#### Conclusion
Chakra est une réussite. C’est une distribution très soignée qui donne une très agréable expérience de KDE. Certains petits désagréments peuvent arriver, mais ils sont principalements dûs à KDE.

J’en viens à souhaiter que les développeurs de KDE fassent une pause dans le développement de nouvelles fonctionnalités et se consacrent pendant une version ou deux à corriger tous les petits soucis d’ergonomie, d’affichage et de cohérence graphique dans KDE.

Allez une petite série de screenshots, pour le plaisir des yeux.

![Akregator](/img/akregator-624x390.png)

![Dolphin](/img/dolphin-624x390.png)

![Firefox avec intégration KDE](/img/firefox-kde-624x390.png)

![Le widget menu QML](/img/menu-qml-624x390.png)

![L’interface graphique de pacman développée pour Chakra](/img/oktopi-624x390.png)


PS : après quelques jours d’utilisation, quelques soucis m’ont fait quitter chakra : une horloge qui se détraque, le serveur akonadi qui ne fonctionne plus après une mise en veille, mais surtout un wiki complètement à la ramasse et un avenir quelque peu incertain…

Du coup j’ai réinstallé KDE sur un arch toute propre, et tout roule !

Chakra reste une distribution intéressante pour quelqu’un qui souhaite tester une distribution KDE sans se frotter à l’installation d’une Arch. Ceci dit, sa réputation de difficulté est exagérée. En suivant le guide pour débutant sur une autre machine connectée à internet, c’est même très facile.
