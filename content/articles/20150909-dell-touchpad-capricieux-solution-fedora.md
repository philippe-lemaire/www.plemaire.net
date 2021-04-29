---
title: "Dell Inspiron 15 3000 faire fonctionner le touchpad sous Debian, Ubuntu et Fedora"
Date: 2015-09-09T17:30:00Z
Category: Logiciels libres
Tags: 
- "Dell"
- "Ubuntu"
- "Debian"
- "Fedora"
Slug: dell-inspiron-15-3000-faire-fonctionner-le-touchpad-sous-debian-ubuntu-et-fedora
Summary: Ou comment régler en 2 minutes ce maudit touchpad qui ne marche pas par défaut
---


Cet été, j’ai fait l’achat d’un portable dell livré sous Ubuntu a un prix défiant toute concurrence : moins de 250 €, livraison incluse.

À peine arrivé à la maison, je l’ai immédiatement formaté pour installer Debian à la place, me disant que ça allait rouler tout seul, vu qu’il marchait avec Ubuntu.

Je pars sur une netinstall avec drivers proprio inclus, au cas où pour le Wi-Fi (pas de prise ethernet en back up) et tout roule.
Jusqu’à ce que je redémarre dans mon environnement tout installé, et que je réalise que le touchpad est non fonctionnel.

Après quelques dizaines de minutes de googleries, j’ai trouvé une solution qui marche nickel sur Ubuntu et Debian : 

Il faut désactiver le module **i2c_hid** et régler les paramètres de boot de grub en **nopnp**.

Modifier en tant que root le fichier :

    /etc/default/grub

Trouver la ligne :

    GRUBCMDLINELINUX_DEFAULT="quiet splash"

et remplacez-la par :

    GRUBCMDLINELINUX_DEFAULT="quiet splash i8042.nopnp"

Sauver et lancer :

    sudo update-grub

Suivis de :

    echo "blacklist i2c_hid" | sudo tee /etc/modprobe.d/i2c-hid.conf
    sudo depmod -a
    sudo update-initramfs -u
    echo "synaptics_i2c" | sudo tee -a /etc/modules
    
Redémarrer.


Pour Fedora, ma nouvelle distribution préférée (peut-être un billet là dessus prochainement, cachez votre impatience) :


Modifier en tant que root le fichier

    /etc/default/grub

Trouver la ligne qui ressemble le plus à ça :

    GRUBCMDLINELINUX_DEFAULT="quiet splash"

et insérer **i8042.nopnp** dans les options à la fin de cette ligne.


Sauver et lancer :

    sudo grub2-mkconfig -o /boot/grub2/grub.cfg

Suivis de

    echo "blacklist i2c_hid" | sudo tee /etc/modprobe.d/i2c-hid.conf
    sudo depmod -a
    sudo dracut -v -f
    echo "synaptics_i2c" | sudo tee -a /etc/modules

Redémarrer.


