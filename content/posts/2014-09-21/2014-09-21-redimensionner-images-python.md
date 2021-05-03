---
title: "Redimensionner des images en masse avec Python"
Date: 2014-09-21T08:00:00Z
categories: 
- "Python"
Tags: 
- "Python"
Slug: redimensionner-des-images-en-masse-avec-python
Summary: Longtemps j'ai installé Shotwell juste pour faire ça…
toc: false
---

#### Contexte
Si vous avez un appareil photo numérique et une famille ou un blog, vous êtes rapidement confrontés à un léger problème technique. Votre appareil vous fait de très belles images de 4272 par 2848 pixels, et qui pèsent entre 5 et 7 Mo chacune. Si vous voulez les envoyer par email, vous allez coincer au niveau volume des pièces jointes au bout de 2 ou 3 photos. Si vous voulez les envoyer sur un site web, votre blog par exemple, vous allez devoir attendre un long moment pour chaque image, si vous n'êtes pas bloqués par la taille limite autorisée pour chaque fichier envoyé.

La solution évidente, c'est de réduire la taille en pixels de l’image, ce qui mécaniquement réduit son poids en Mo. Vous pouvez faire ça très facilement avec [Gimp](http://www.gimp.org/). On ouvre l’image, on va dans "Image", "Échelle et taile de l’image", on réduit la largeur de 4872 à 1000 ou 1200, on laisse la hauteur suivre proportionnellement, et miracle, après sauvegarde, l’image ainsi réduite a vu sa taille divisée par 10.

Mais c’est plutôt fastidieux à faire sur une série de photos.

Jusqu’à ce que je me penche un peu sur le langage [Python](http://www.python.org), je faisais ça en installant [Shotwell](http://yorba.org/shotwell/help/), un gestionnaire de photos qui a une fonction d’export de photos avec redimensionnement.
Mais aujourd’hui, j’utilise un petit script que j’ai écrit en Python et qui fait le même job, sans essayer de scanner l’ensemble de mon dossier image, comme ce gros lourdeau de Shotwell.

#### Le script

Pour que le script fonctionne, vous avez besoin d’installer la bibliothèque Python de manipulation d’images appelée PIL (Python Image Library). Le paquet s’appelle **python3-pil** dans debian, ubuntu et linux mint.

    sudo apt-get install python3-pil

Créez vous un fichier appelé *imgresize.py* où vous voulez.
Son contenu :

    # Objectif : redimensionner en masse des images dans un dossier, avant utilisation pour blog ou partage par email par exemple
    # TODO : fix si fichier non image présent dans le dossier (genre .directory), fait mais hard codé sur terminaison fichier image en "G" ou "g"

    from PIL import Image
    from os import listdir
    from os.path import isfile, join

    mypath = input("Dans quel dossier sont les images ? ")
    imageFiles = [ f for f in listdir(mypath) if isfile(join(mypath,f)) and (f.endswith("G") or f.endswith("g")) ]
    target = int(input("Dimension maximum voulue (ex 1000) : "))

    for im in imageFiles :
        im1 = Image.open(join(mypath,im))
        originalWidth, originalHeight = im1.size
        ratio = originalWidth / originalHeight
        if ratio > 1 :
            width = target
            height = int(width / ratio)
        else :
            height = target
            width = int(height * ratio)

        im2 = im1.resize((width, height), Image.ANTIALIAS) # linear interpolation in a 2x2 environment
        im2.save(join(mypath, "".join([str(width),"x",str(height),"_",im])))
        print (im, "redimensionnée…")
    print ("Travail terminé !", len(imageFiles), "images redimensionnées.")

Pour exécuter le script, 

1. vous ouvrez un terminal, 
2. vous l’amenez dans le dossier où est le script à coup de :

    cd chemin/jusqu'au dossier/où est le script/

3. Vous copiez le chemin du dossier où sont vos images à redimensionner dans le presse papier.
4. Vous lancez le script dans le terminal

    python3 imgresize.py

5. Le script vous demande le chemin du dossier où sont les images (collez en cliquant avec la molette)
6. Le script vous demande quelle dimension max vous voulez, par exemple 1000. Si l’image est en paysage, sa largeur sera de 1000, si elle est en portrait, sa hauteur sera de 1000.
7. Le script crée des copies redimensionnées dans le même dossier que les images sources, et préfixe leur nom avec "largeur"x"hauteur", pour les distinguer plus facilement des images source.

![script en image](/img/imgresize-py.png)

Le script sur [mon dépôt Github](https://github.com/mekkagodzilla/python/blob/master/tools/imgresize.py).

#### Conclusion

Sachez que je ne suis en aucun cas un expert de la programmation. Si vous avez une suggestion d’amélioration du script, n’hésitez pas à m’en faire part via les commentaires. Je suis preneur.

Si le script s’avère utile pour vous, n’hésitez pas non plus à me le faire savoir.


