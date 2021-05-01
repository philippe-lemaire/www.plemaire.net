---
title: "Migration du site sous Pelican"
Date: 2014-01-02T10:00:00Z
categories: 
- "Internet"
Tags: 
- "Logiciel libre"
- "CMS"
Slug: migration-du-site-sous-pelican
Summary: Pourquoi je suis passé de [WordPress](http://wordpress.org) à [Pelican](http://blog.getpelican.com/) pour propulser ce blog.
---


Je suis régulièrement le [planet](https://planet.archlinux.org) de la distribution [Arch Linux](https://www.archlinux.org/). 

Une partie des articles me passe au dessus de la tête, mais je tombe souvent sur des billets très intéressants, notamment la [série "interesting links"](http://allanmcrae.com/category/links/) sur le site d’Allan McRae.

C’est via le planet que j’ai découvert [Pelican](http://blog.getpelican.com/), un outil de génération de blog en html statique.

L’idée est la suivante : plutôt que de reposer sur le duo de choc PHP et MySQL pour faire tourner un petit site ou un blog, il est beaucoup plus simple techniquement et donc intéressant en termes de ressources sur le serveur web de faire une moulinette qui prend des fichiers de contenu en entrée et sort un site statique en sortie.

Pour essayer la chose, j’ai créé un site sur le game design qui me trottait dans la tête depuis un moment : [Game Over Analyzed](http://www.game-over-analyzed.com) avec pelican.

Une fois pelican et ses dépendances installées sur mon PC, il m’a suffit de rédiger mes articles au format [Markdown](http://daringfireball.net/projects/markdown/), en ajoutant en tête des fichiers les informations suivantes pour pelican :
```
    ---
title: "Titre de notre article"
    Date: 2014-01-02T19:00:00Z
    categories: Categorie de notre article
    Tags: tags, separes, par, une, virgule
    Slug: url-de-la-page-apres-la-racine
    Summary: Resume pour la page qui liste les articles
---

    Debut du contenu.

```

La différence de performance sur un hébergement mutualisé par rapport à un WordPress est indéniable.
Du coup, j’ai eu envie de basculer ce blog en pelican aussi.

J’ai passé quelques minutes à reprendre mes articles en Markdown, je me suis assuré que les urls des articles restaient les mêmes qu’avant pour ne pas perdre l’indexation de Google sur mes pages, et j’ai regénéré mon site (ce qui prend 0.89 secondes, litérallement) avec pelican.

Et voilà le travail. Le site est visiblement plus rapide qu’avant. C’est l’avantage de faire du vieux avec du neuf.
