---
title: "Le guide du débutant sous Linux : choisir sa distribution et son environnement de bureau"
Date: 2015-07-15T18:00:00Z
categories: 
- "Logiciels libres"
Tags: 
- "Linux"
Slug: le-guide-du-debutant-sous-linux-choisir-sa-distribution-et-son-environnement-de-bureau
Summary: Un des premiers casse-tête qui attend toute personne qui découvre l’éco-système GNU/Linux pour la première fois est le vaste choix de distributions et d’environnements de bureau. Choisir une distribution qui vous conviendra dépend de multiples critères, dont l’environnement de bureau proposé, aussi les deux sujets sont liés.
---

## Introduction

Dans mon précédent [guide sur la migration de Windows XP à Linux](http://www.plemaire.net/posts/le-guide-de-migration-de-windows-xp-vers-Linux), j’ai pris le parti de recommander Debian avec Xfce aux débutants. 
Même s’il est contraire à la sagesse populaire qui veut qu’Ubuntu soit la distribution de référence pour les débutants, ce choix de Debian peut se justifier, mais ce n’était pas l’objet du guide.

Étudions plus en détail quelques distributions adaptées aux débutants sous Linux, leurs forces, et leurs faiblesses.

## Ubuntu et son environnement Unity
![Ubuntu et son environnement Unity](/img/ubuntu-unity.png)
**Ubuntu et son environnement Unity**

[Ubuntu](http://www.ubuntu.com) est la distribution Linux la plus célèbre, et généralement c’est elle qui est recommandée aux débutants. C’est la première distribution que j’ai personnellement installée il y a maintenant 10 ans, et qui m’a bien servi pendant 5 ans. 

Ses grandes forces pour les débutants :

- Une procédure d’installation très simple. On vous demandera simplement votre langue, disposition de clavier préférée, fuseau horaire, quel disque dur utiliser, un nom et un mot de passe, et tout le reste va se dérouler automatiquement. L’installation prend environ 20 minutes sur un disque dur à l’ancienne, et sans doute beaucoup moins sur un disque SSD.
- Un module de recherche des pilotes propriétaires de votre matériel. Il y a généralement 2 périphériques de votre ordinateur qui ne fonctionneront pleinement qu’après installation d’un pilote propriétaire : votre carte graphique et votre carte réseau Wi-Fi. Un utilisateur chevronné de distributions moins orientées grand public saura très bien quoi chercher et installer ça sur sa machine, mais pour les débutants, Ubuntu a créé une petite application qui scanne votre matériel, et vous propose d’installer ces pilotes en quelques clics.
- La force du nombre : Ubuntu étant la distribution la plus populaire, en l’utilisant vous bénéficiez du fait que la plupart des ressources en ligne sont ciblées pour les utilisateurs d’Ubuntu.

Ses faiblesses :

- Son environnement Unity peut être gourmand en ressources, pas idéal sur une machine un peu ancienne.
- Son cycle de développement rapide, une version tous les 6 mois, peut être pénible à suivre, car trop fréquent et donnant lieu à des machines instables dans les premières semaines d’une nouvelle version. Préférez les versions dites LTS (Long Term Support) qui bénéficient d’un suivi (màj de sécurité) pendant 5 ans.

## Xubuntu
![Xubuntu et son bureau Xfce](/img/xubuntu-xfce.png)
**Xubuntu et son bureau Xfce**

[Xubuntu](http://xubuntu.org) est une variante d’Ubuntu avec un environnement de bureau différent, le très simple et léger Xfce.
Xubuntu a le même rythme de sortie qu’Ubuntu, mais comme Xfce lui-même évolue beaucoup moins fréquemment, les différences d’une version à l’autre de Xubuntu sont souvent mineures.

Ses forces pour les débutants :

- Les trois points évoqués plus haut pour Ubuntu s’appliquent à Xubuntu.
- De plus le bureau Xfce est simple et léger, et donnera une seconde jeunesse à un PC vieillissant.
- Une esthétique par défaut plutôt propre. Facile à reproduire sur d’autre distributions cependant (thème Greybird et icônes elementary-xfce)

Ses faiblesses :

- Le cycle de vie rapide, comme pour Ubuntu.
- D’autres distributions embarquant Xfce semblent avoir de meilleures performance sur des machines anciennes.

## Linux Mint et ses environnements Cinnamon et MATE
![Linux Mint avec MATE Desktop](/img/mint-mate.png)
**Linux Mint avec MATE Desktop**

[Linux Mint](http://www.linuxmint.com/) est une distribution basée sur Ubuntu (une vaste partie des logiciels proposés viennent directement des serveurs d’Ubuntu et sont donc identiques). Les différences vont essentiellement porter sur les environnement de bureau proposés et certains choix techniques / légaux.

Les deux environnements proposés sont Cinnamon et MATE.
Les deux sont assez traditionnels : un menu, une barre des tâches montrant les fenêtres ouvertes, la date et l’heure, etc.
Cinnamon utilise des effets de bureau de manière plus intensive, et a donc un look plus moderne au niveau des animations de fenêtres, des transitions d’un bureau virtuel à l’autre, mais est plus exigeant sur la configuration de votre machine.   
MATE est beaucoup plus simple techniquement, et propose un environnement sans fioritures modernes.

Notez que contrairement à Unity pour Ubuntu, ces deux environnements ne sont pas exclusifs à Linux Mint, même si Cinnamon a été créé par l’équipe de Mint. On peut très bien installer ces environnements sur d’autres distributions comme Ubuntu ou Debian.

Ses forces pour les débutants :

- Procédure d’installation identique à Ubuntu.
- Module de recherche des pilotes identique à Ubuntu.
- Les paquets nécessaires à la lecture de fichier mp3 ou vidéos sont pré-installés, contrairement à Ubuntu
- Force du nombre, les infos et paquets concernant Ubuntu s’appliquent la plupart du temps à Linux Mint. Attention cependant à bien réaliser à quelle version d’Ubuntu correspond la version de Mint qu’on utilise.
- Les environnemnts graphiques proposés (Cinnamon et MATE) sont relativement traditionnels dans leur fonctionnement (proche de Windows XP dans l’esprit), et donc facile à adopter pour les débutants ayant l’expérience de Windows 95 à Vista).

Faiblesses :

- Performances de Cinnamon sur machines anciennes
- Esthétique douteuse, mais bon les goûts et les couleurs. Et puis ça se change.
- Dérivée d’Ubuntu, elle-même dérivée de Debian. Les deux couches en plus peuvent être source de problèmes.

## Debian, le système d’exploitation universel
![Debian et le bureau Cinnamon](/img/debian-cinnamon.png)
**Debian et le bureau Cinnamon**

[Debian](http://www.debian.org) est un des projets les plus anciens, il remonte au début des années 90. C’est une distribution très complète, au sens où la quasi totalité des logiciels libres et des environnements de bureau y sont empaquetés et prêts à être installés. Dans sa nouvelle version stable, nom de code "Jessie", debian propose les environnements de bureau suivants :

- GNOME
- Xfce
- KDE
- Cinnamon
- MATE 
- LXDE

Debian est un projet communautaire, contrairement à Ubuntu, aucune société commerciale ne se trouve derrière. C’est un avantage au sens où Debian ne tente jamais de monétiser ses utilisateurs comme Ubuntu a pu le faire avec la recherche Amazon intégrée au bureau, ou ses services de téléchargement de musique. Mais ça signifie aussi que Debian dispose de peu de moyens financiers, en restant tributaire de dons et du bénévolat de ses développeurs.

Parmi l’ensemble des environnements de bureau proposés, ceux qui conviennent le plus aux débutants à mon sens sont Xfce, Cinnamon, et MATE, déjà évoqués plus haut. En terme de performance, debian est généralement plus légère qu’Ubuntu ou Mint avec le même environnement de bureau, mais de peu. En revanche, du fait du cycle de développement beaucoup plus lent (une nouvelle version tous les 2 ou 3 ans), les versions de logiciels empaquetés pour Debian ont tendance à avoir entre 1 et 3 ans de retard par rapport à celles qu’on trouve dans la Ubuntu la plus récente.

Ses forces pour les débutants :

- De meilleures performances toutes choses égales par ailleurs. Important pour de vieilles machines.
- Un installeur plus simple techniquement, qui peut tourner sur n’importe quel ordinosaure, contrairement à celui d’Ubuntu et ses dérivées.
- Une distribution non commerciale.
- Un excellent processus qualité, qui fait que les logiciels empaquetés sont sans mauvaise surprise.
- Un cycle de développement long. Vous être tranquille pour au moins 3 ans, et la migration sans réinstallation d’une version à la suivante est testée et éprouvée, contrairement à Ubuntu / Mint. Important si vous installez une distribution pour un tiers.

Ses faiblesses : 

- La documentation est moins simple d’accès. La plupart des infos qu’on trouve sur le web sont pour Ubuntu, et peuvent s’appliquer ou non à Debian. Le wiki debian est souvent source de confusion, avec des instructions différentes pour différentes versions de Debian, et parfois sans instructions pour la version stable actuelle. Le site web de debian est difficile à naviguer.
- Le processus d’installation reste simple, mais il offre plus de choix que celui d’Ubuntu et autre, et peut rebuter le grand débutant.
- Pas d’installation automatisée des pilotes propriétaires. Il faut savoir qu’ils existent, et installer le paquet qu’il faut soi-même. 

## HandyLinux
[HandyLinux](http://handylinux.org/) est une distribution française basée sur Debian, et qui cible spécifiquement les débutants.
Ici le choix de l’environnement de bureau est volontairement limité à Xfce, configuré avec un choix de logiciles pré-installé couvrant les besoins des utilisateurs classiques : VLC pour la vidéo, OpenOffice pour le traitement de texte et les tableaux.
Le truc en plus de HandyLinux, c’est son menu spécifique, qui permet de lancer facilement les applications et certaines pages web considérées comme utiles par les développeurs de cette distribution.

![le menu HandyLinux](http://handylinux.org/img/screenshot/handymenu.png)
**le menu HandyLinux**

Ses forces pour les débutants :

- Pensée pour les débutants, avec son choix d’applis par défaut et son menu spécial
- Excellentes performances
- [Excellente documentation](http://wiki.handylinux.org/doku.php/fr/start) en français sur le site web (accessible du menu). Esprit d’entraide sur les forums dédiés.
- Debian sous le capot, excellente stabilité : peu de bugs, peu de changements dans le temps.

Ses faiblesses :

- Debian sous le capot, des versions de logiciels du coup parfois anciennes.

## Conclusion

Entre ces 5, je dirais que HandyLinux se démarque. Les performances et la simplicité d’Xfce, l’orientation utilisateur débutant, la stabilité de Debian, la documentation de qualité et la communauté frenchie et sympa en font un excellent choix.  
Si vous souhaitez avoir une base logicielle plus récente, Xubuntu est un très bon choix, et bénéficie du fait qu’Ubuntu est très largement distribuée, ce qui rend l’installation de logiciels propriétaires ciblant Ubuntu plus simple (jeux vidéos, Skype, Google Hangout, par exemple).  
Debian n’est pas un choix complètement délirant, mais restera réservée aux utilisateurs qui ont le goût de personnaliser eux-même leur ordinateur, l’esthétique par défaut étant assez douteuse.
