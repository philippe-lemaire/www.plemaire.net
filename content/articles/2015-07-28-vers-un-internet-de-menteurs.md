---
title: "Les DNS menteurs"
Date: 2015-07-28T17:00:00Z
Category: Internet
Tags: 
- "Censure"
- "DNS"
Slug: les-dns-menteurs
Summary: Ou comment un opérateur peut faire disparaître un site de la toile pour ses abonnés
---

Aujourd’hui l’opérateur historique Orange a unilatéralement fait disparaître du web pour ses abonnés le site [www.t411.io](http://www.t411.io).

Alors certes, ce site est un repère de pirates utilisant le protocole BitTorrent pour s’échanger films, séries TV, jeux piratés, musique en mp3, et il est évident que son utilisation est à des fins pas tout à fait réglo.

De plus, Orange semble agir ici à la demande du tribunal de Grande Instance de Paris, qui a ordonné en avril 2015 aux opérateurs d’empêcher l’accès à ce site, la principale source de torrents en français ou sous-titrés français.

Ce qui pose question, c’est la manière dont la chose a été faite, qui est risible pour les gens techniquement initiés.

La méthode utilisée par Orange est celle du DNS menteur.
Un Serveur DNS est une machine qui oriente votre activité sur internet vers le serveur hébergeant le site ou le service que vous recherchez.
Quand vous tapotez [www.t411.io](http://www.t411.io) dans votre navigateur, votre ordinateur demande à un serveur DNS quelle est l’adresse IP qui correspond à ce nom de domaine.
Normalement, le serveur DNS doit répondre : 

    108.162.204.254

mais celui qu’utilisent les clients d’Orange va désormais répondre :

    127.0.0.1

Ce qui correspond à l’adresse locale de votre propre ordinateur, et ne peut aboutir, exactement comme vous pouvez [forcer les domaines pénibles à ne pas aboutir grâce à votre fichier hosts](http://www.plemaire.net/un-fichier-hosts-pour-un-internet-moins-sale).

Du coup, pour contourner la manœuvre d’Orange, il suffit de paramétrer sa connexion pour [utiliser un autre serveur DNS](http://assiste.com/Comment_Changer_de_DNS_pour_utiliser_ceux_de_Google.html) qui ne ment pas, comme celui de Google par exemple, ou bien d’indiquer dans son fichier hosts que t411.io est à l’IP 

    108.162.204.254

Quitte à changer de temps en temps ce réglage manuel si d’aventure t411 change d’IP. Un jeu d’enfant pour l’utilisateur averti.

Moralité, on a là un opérateur qui s’exécute parce que la justice l’a ordonnée, mais il l’a fait d’une manière qui ne bloquera probablement pas grand monde.

Si c’est avec ce genre de technique qu’on compte également bloquer l’accès aux sites faisant l’apologie du terrorisme, c’est pas gagné…

Sinon, pour une vue plus technique du sujet et une solution pour avoir son propre résolveur DNS sur sa machine, je vous invite à lire l’[excellent article de Stéphane Bortzmeyer](http://www.bortzmeyer.org/son-propre-resolveur-dns.html).
