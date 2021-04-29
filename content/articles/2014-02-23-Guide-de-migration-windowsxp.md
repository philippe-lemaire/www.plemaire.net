---
title: "Le guide de migration de Windows XP vers Linux"
Date: 2014-02-23T09:00:00Z
categories: 
- "Logiciels Libres"
Tags: 
- "Linux"
- "Debian"
- "Xfce"
Slug: le-guide-de-migration-de-windows-xp-vers-Linux
Summary: Windows XP arrive en fin de vie. Plus aucune mise à jour après juin 2014. Mais ça ne veut pas dire qu’il faut mettre son PC à la benne.
---

#### Introduction

![Windows XP en fin de vie](/img/windowsxp-rip.jpg)

Windows XP arrive bientôt en fin de vie. Ce sont des millions de PC qui ne vont plus recevoir aucune mise à jour de sécurité. Ces machines typiquement anciennes ne sont pas aptes à faire tourner Windows 7 ou 8. Trois solutions s’offrent aux utilisateurs concernés :

* Casser la tirelire pour un nouveau PC, vendu avec Windows 8,
* Casser la tirelire encore plus fort pour passer chez Apple,
* Conserver le PC et remplacer Windows XP par une distribution Linux légère.

Cette dernière option a l’avantage d’être gratuite, tout en vous donnant accès à un système à jour, immunisé contre les virus et autres malwares qui visent Windows, et l’accès aux applications importantes : Firefox, Google Chrome, Skype, LibreOffice.

Installer Linux sur un PC n’est pas aussi difficile que vous pouvez le croire. Mais avant l’installation elle-même, c’est à la migration de vos données qu’il faut penser.

#### 1. Faire un back up de vos données

Avant d’entamer votre migration, vous allez devoir faire une sauvegarde des données importantes présentes sur le disque dur de l’ordinateur vers un support externe. En effet, Linux utilise des méthodes plus avancées d’écriture des données sur le disque, mais passer à ce système de fichier va nécessiter de faire table rase sur le disque.

#### 2. Choisir une distribution

Le noyau Linux et les logiciels libres qui l’accompagnent pour former un environnement de bureau ne sont pas disponibles dans le commerce. 
Des organisations, la plupart du temps communautaires et bénévoles font le travail qui consiste à assembler toutes les pièces nécessaires et à distribuer des images disques prêtes à installer.
On appelle ça une distribution Linux.

Il existe de nombreuses distributions, car différentes personnes ont fait différents choix techniques sur les logiciels à inclure et la manière d’assembler le tout.
Certaines distributions ciblent le grand public tandis que d’autres s’adressent aux experts. 
Un autre facteur est la fraicheur des versions de logiciels proposées. Certaines distributions veulent intégrer la nouvelle version de chaque logiciel dès sa sortie, et à l’autre bout de ce spectre certaines distributions préfèrent utiliser des versions plus anciennes, mais davantage testées.

Si vous êtes débutants, et que votre matériel est un peu ancien (processeur autour de 1GHz, 2 Go de RAM par exemple), alors je préconise Debian avec le bureau Xfce.
Vous pouvez télécharger l’image disque ici : [http://cdimage.debian.org/debian-cd/current-live/i386/iso-hybrid/](http://cdimage.debian.org/debian-cd/current-live/i386/iso-hybrid/).
Choisissez le fichier Xfce dans la liste.

Notez bien que cette image contient beaucoup plus qu’un disque d’installation de Windows XP. Vous avez dans ce giga-octet le cœur du système plus un ensemble de logiciels : navigateur Firefox (renommé IceWeasel pour des raisons de droits), visionneur d’images, de PDF, suite bureautique, lecteur de musique et de vidéo. De plus, ajouter des logiciels complémentaires est rapide, sécurisé et gratuit.

#### 3. Préparer un media d’installation

Une fois l’image disque téléchargée (le fichier .iso lié ci-dessus), vous devez soit la graver sur un DVD-ROM vierge (choisissez bien dans votre logiciel de gravure de partir d’une image disque comme source), soit la transférer sur une clé USB.

Pour transférer sur une clé USB, vous devez avoir une clé de taille supérieure à 1 Go, et vous pouvez suivre les étapes suivantes :

1. Téléchargez [Win32DiskImage](http://launchpad.net/win32-image-writer/0.1/0.1/+download/win32diskimager-RELEASE-0.1-r15-win32.zip).
2. Décompressez le zip obtenu dans le dossier de votre choix, de préférence celui où vous avez mis l’image iso de la distribution Linux.
3. Lancez le programme Win32ImageWriter et cliquez sur l’icône de dossier dans la section "Image File".
4. Dans la fenêtre “Select a disk image,” allez dans le dossier où se trouve votre image disque et sélectionnez la. Cliquez sur "Save".
5. Selectionnez votre clé USB dans la liste dans la section "Device".
6. Cliquez sur le bouton “Write” pour écrire l’image disque sur la clé USB. NB : Cette opération efface le contenu de la clé avant d’écrire l’image. Vous devez donc utiliser un support différent pour votre sauvegarde de données !

Quand votre clé ou DVD-ROM sont prêts, vous êtes prêts à installer la distribution Linux.
Redémarrez l’ordinateur avec la clé branchée ou le CD-ROM dans le lecteur.

En général, les ordinateurs sont capables de démarrer à partir d’une clé USB, mais sont configurés par défaut pour prioriser le redémarrage depuis le disque dur ou le lecteur CD.
Pour remédier à ça, regardez bien le texte qui apparaît à l’écran quand vous démarrez l’ordinateur.

Ce texte doit indiquer quelle touche du clavier vous devez utiliser pour entrer dans les réglages du Bios.
Ça devrait être une phrase du genre "Press F10 to enter BIOS Setup".
La touche en question dépend des fabricants.
Si vous entrez dans ces réglages, cherchez une section "boot", et faites en sorte que la clé USB soit considérée avant le disque dur (HDD) pour le démarrage.
Sauvegardez et sortez des réglages du bios.

#### 4. Installer

Si vous avez suivi toutes les étapes précédentes, vous avez fait le plus dur.

L’installation de debian est très facile. Choisissez l’option d’installation par défaut, qui vous demandera quelques informations de base : la langue désirée, votre fuseau horaire, votre nom, le login et mot de passe de votre futur compte sur la machine.

Vous allez pouvoir partitionner vos disques. Une partition est une division de votre disque dur un plusieurs parties indépendantes. C’est une bonne idée de séparer vos données (le dossier /home) du système lui-même (le dossier racine, représenté par un /).
Ainsi, si vous souhaitez changer de distribution Linux plus tard, vous pourrez effacer et réécrire le dossier / sans toucher au disque qui contiendra vos données personnelles (le dossier /home).

Si vous décidez de suivre ces bons conseils, voici quelques indications pour choisir la taille de vos partitions :

* Créez une partition / de type Ext4. Elle devrait faire au moins 8Go. Vous pouvez monter à 15 Go si vous avez un grand disque, pour être large. Cette partition sera celle dans laquelle les logiciels que vous ajouterez à votre système vont aller.
* Créez une partition SWAP de 2 à 4 Go.
* Enfin, créez une partition /home (encore de type Ext4) avec tout l’espace qui reste. C’est dans cette partition que vous rangerez vos documents, votre musique, vos films, et que s’enregistreront vos réglages personnels de chaque application

Suite au partitionnement, l’installation à proprement parler se lance.
L’opération devrait durer environ 20 minutes.
Quand le processus sera terminé, on vous demandera de redémarrer.
Enlevez la clé USB au moment où l’ordinateur redémarre pour qu’il démarre bien sur le disque dur cette fois.

#### 5. Premier démarrage

Lorsque votre ordinateur démarre sous votre nouvelle installation de Linux, vous serez en quelques secondes sur l’écran de connexion.
Utilisez le login et mot de passe que vous avez choisi pendant l’installation.
Vous voici ensuite sur votre bureau, prêt à travailler.

![le bureau xfce sous debian](/img/debian-xfce.jpg)

C’est le moment de reprendre vos données sauvegardées avant la migration et de les transférer dans votre dossier personnel tout neuf.

#### 6. Les concepts et réflexes utiles

Un des éléments les plus importants à apprendre lorsqu’on débarque du monde windows est la gestion de l’ajout / suppression / mise à jour des logiciels.

Sous windows, vous êtiez habitués à aller chercher un logiciel sur le web, à télécharger un installeur en .exe ou .msi, et à l’exécuter, en faisant bien attention à décocher certaines options pénibles faites pour modifier votre moteur de recherche par défaut, ou ajouter une barre d’outil inutile dans votre navigateur.  
Oubliez tout ça.

Dans une distribution Linux, ajouter ou supprimer un logiciel se fait par la même interface centralisée.
Lancez le gestionnaire de paquets Synaptic depuis votre menu, donnez votre mot de passe, et vous n’avez plus qu’à chercher les logiciels que vous voulez, les sélectionner, et valider pour qu’ils soient téléchargés et installés.

![Synaptic Debian](/img/Debian-7-Synaptic-Package-Manager.png)

Cette même interface vous permet de mettre à jour l’ensemble des logiciels de votre machine.
Plus de pop-up réclamant la mise à jour de java, d’acrobat reader et autres, tout est centralisé.
Vous vous demanderez comment vous supportiez ça avant.

Un autre aspect important à comprendre est qu’un logiciel fait pour Windows ne va pas fonctionner tel quel sous Linux.
Souvent, il existe des équivalents gratuits et accessibles depuis Synaptic.
Il vous faut juste faire un peu de recherche sur Google pour trouver le nom de ces équivalents.

#### Conclusion

Migrer une vieille machine sous Linux, c’est lui donner une seconde vie.
Le système est beaucoup moins gourmand que Windows, et vous trouverez votre machine beaucoup plus rapide et agréable à utiliser.
Si jamais vous partez quand même pour un nouvel ordinateur, pensez à donner votre ancienne machine à une association comme [Emmaüs](http://www.emmaus-france.org/).

#### Post Scriptum

Si vous avez fait le grand saut, je vous invite à lire la suite de cet article : [10 trucs à savoir après une migration vers Linux](https://www.plemaire.net/10-trucs-a-savoir-apres-une-migration-vers-linux)
