---
title: "Écrire un article WordPress en Markdown"
Date: 2013-12-26T01:38:00Z
categories: 
- "Internet"
Tags: 
- "Markdown"
Slug: ecrire-un-article-wordpress-en-markdown
Summary: Comment utiliser Markdown pour la rédaction d’articles sous WordPress
---


Si vous êtes comme moi, vous préférez utiliser les outils auxquels vous êtes habitué et avec lesquels vous vous sentez performants plutôt que ceux qu’on vous impose au nom de la simplicité.

Depuis que j’ai appris à utiliser [vim](http://www.vim.org), je préfère formater mes contenus avec, en HTML, puis copier le résultat obtenu dans l’éditeur de contenu de mon CMS, plutôt que d’utiliser l’éditeur WYSIWYG fourni avec WordPress, Magento, PrestaShop, ou autre.

Ça permet aussi de garder des copies locales des contenus, et de bénéficier de la coloration syntaxique et de toutes les fonctionnalités de vim.

Le seul problème de cette approche, c’est que c’est fastidieux d’écrire en HTML, surtout pour faire des liens tout simples où le texte à faire apparaître est l’url du lien.
C’est aussi difficile à lire et relire, et une erreur de frappe (un / ou > manquant par exemple) est difficile à percevoir.

Mais comme toute pour tâche bête et méchante en informatique, il y a au moins un geek que ça a énervé et qui s’y est collé pour trouver une solution.

Et une des solutions à ce problème est Markdown, une façon simple et légère de baliser votre contenu.

Pour tout savoir sur Markdown, vous pouvez commencer par [la page Wikipedia sur Markdown](http://fr.wikipedia.org/wiki/Markdown).

Pour utiliser Markdown dans la rédaction de vos articles et pages WordPress, vous avez un [plugin fort sympathique](http://wordpress.org/plugins/markdown-on-save-improved).

Résultat :

* les titres se font avec de simples # en début de ligne (#### pour h2, ##### pour h3, etc)
* les items d’une liste se font avec de simples * en début de ligne
* il suffit d’indenter des lignes avec 4 espaces pour faire un bloc de code
* il suffit de démarrer une ligne par > pour en faire une citation
* les liens sont super faciles à faire et relire avec le texte entre crochets suivis de l’url entre parenthèses.

