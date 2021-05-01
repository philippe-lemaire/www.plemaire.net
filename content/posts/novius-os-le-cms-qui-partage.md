---
title: "Novius OS, le CMS qui partage"
Date: 2013-12-17T00:20:00Z
categories: 
- "Internet"
Tags: 
- "CMS"
- "Logiciel libre"
Slug: novius-os-le-cms-qui-partage
Summary: Premières impressions sur Novius OS, un CMS PHP développé par une équipe française.
---


Hello, Internet,

Aujourd’hui, pas de billet sur debian ou les théories du complot, mais un petit tour d’horizon d’un CMS développé par une agence web lyonnaise appelée Novius.

#### Présentations
Le CMS en question s’appelle Novius OS, et vous trouverez son site officiel ici : <a href="http://www.novius-os.org/" target="_blank">http://www.novius-os.org/</a>

Novius n’est pas un système d’exploitation à proprement parler, mais bien un outil de gestion de contenu pour construire un site web. Cependant, il emprunte certains paradigmes au monde des systèmes d’exploitation d’où son nom. Certains pans du logiciel, qui seraient appelés modules ou extensions dans d’autres CMS, sont appelés des Applications dans Novius OS, par exemple.

Novius OS est un logiciel libre, son code est hébergé sur [github](https://github.com).

Pour essayer Novius OS, vous pouvez soit aller cloner son [dépôt github](https://github.com/novius-os/novius-os), soit utiliser l’[instance de démo mise à disposition](http://demo.novius-os.org/admin).

Ce qui suit est une série de captures d’écrans et ma réaction après avoir essayé cette démo. Je vais principalement le comparer à WordPress car c’est la plateforme que je connais le mieux.

#### Interface d’administration
L’interface d’administration est colorée et agréable, elle tranche par rapport à la sobriété de l’interface d’autres CMS comme WordPress ou Drupal.

![Interface admin](/img/novius/capture-décran1.png)

Un aspect original et agréable est que à chaque fois que vous entrez dans une section, un article ou un billet, ceci se fait dans un onglet de cette interface (et non un onglet de votre navigateur), ce qui permet d’aller rapidement entre une page en cours de rédaction et la liste des pages, par exemple, ou tout autre partie de l’administration. C’est le genre de chose que les utilisateurs avancés font avec les onglets de leur navigateur quand ils utilisent un autre CMS, mais c’est assez pratique et beaucoup mois envahissant ici.

![Onglets](/img/novius/onglets.png)

#### Gestion des pages, billets
Pour l’édition des contenus textes (pages, billets), Novius OS semble utiliser un éditeur WYSIWYG inspiré de tinyMCE. Vous pouvez utiliser une vue html sur simple pression d’un bouton.

![Éditeur WYSIWYG](/img/novius/capture-décran10.png)

![Éditeur HTML](/img/novius/capture-décran9.png)

#### Multi-site, multilangue
Novius OS permet de créer un site multilangue par défaut. Un bon point par rapport à WordPress, où les plugins pour faire ça sont soit un peu "clunky" (qtranslate) soit payant (WPML).

Une même installation de Novius OS peut faire tourner plusieurs sites. Encore une fois c’est possible avec WordPress, mais compliqué.

#### Images
Insérer une image dans sa bibliothèque est très facile.

![Bibliothèque](/img/novius/capture-décran6.png)
Cependant, contrairement à WordPress, Novius OS ne créé pas de vignettes redimensionnées de votre image. Vous devez l’utiliser telle que vous l’avez uploadé, ou jouer sur les paramètres width et height quand vous l’insérez dans votre contenu.

![Détails image](/img/novius/capture-décran7.png)

Avec les images de votre bibliothèque, vous pouvez également créer facilement des sliders animés, et les insérer ensuite dans vos billets ou vos pages. C’est simple et efficace, beaucoup plus que dans WordPress où il faut partir à la chasse au plugin pour faire ça, et trouver un bon plugin parmi la masse de ceux proposés peut être très pénible.

![Gestion sliders](/img/novius/capture-décran27.png)

#### Partage des contenus
La fonctionnalité mise en avant par les créateurs de Novius OS est le partage des contenus sur les plateformes sociales.
Quand votre contenu est prêt, il suffit de cliquer sur le bouton partager pour partager ce contenu sur Facebook ou Twitter. C’est évidemment quelque chose que l’on peut aussi faire avec WordPress, mais pas sans avoir passé du temps à la chasse au plugins.

![Partage de contenu](/img/novius/capture-décran15.png)

L’idée est de faire gagner du temps aux web-marketeurs, et pour le coup ça simplifie énormément le canal du contenu aux plateformes de partage.
J’aimerais bien voir d’autres réseaux sociaux proposés, comme Google + et Reddit par exemple, mais les deux plus importants sont là.

#### Création de formulaires
Une autre fonctionnalité sympathique par défaut est le créateur de formulaires. La démo contient un formulaire de contact créé avec, mais on peut le modifier ou en créer d’autres. Un plugin de moins à chercher.

![Créateur de formulaire](/img/novius/capture-décran24.png)

#### Front Office
Le look and feel du site créé avec la démo est très nu. Je n’imagine pas l’utiliser tel quel, mais comme une base pour créer un template personnalisé.
Il n’y a pas de thèmes prêts à l’emploi à ma connaissance. À vous de créer le votre. Du fait, Novius OS s’adresse plus au développeur ayant l’expérience de développer un front office, plutôt qu’au grand public.

#### Sites utilisant Novius OS
Voici quelques sites "pros" qui tournent sous Novius OS

* [http://www.oivmsc.org/en/](http://www.oivmsc.org/en/)
* [http://biomol.pl/biomol/en_GB/](http://biomol.pl/biomol/en_GB/)
* [http://www.bioaster.org/home.html](http://www.bioaster.org/home.html)

#### Conclusion

Novius OS semble très agréable à utiliser au quotidien pour la ou les personnes en charge d’animer et promouvoir leur contenu.
Obtenir un site avec un look fini demandera cependant plus de travail qu’une simple installation de WordPress accompagné un thème.
Un projet à suivre de près.
