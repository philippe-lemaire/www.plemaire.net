---
title: "Comment désactiver les actions sur les coins du pavé tactile sous Linux"
Date: 2019-04-12T10:00:00Z
categories: 
- "Logiciels libres"
Tags: 
- "Linux"
- "Debian"
- "Xfce"
Slug: comment-desactiver-les-actions-sur-les-coins-du-pave-tactile-sous-linux
Summary: Les affres de la vie sans environnement de bureau.

resources:
- name: "featured-image"
  src: "featured-image.jpg"

featuredImage: "/img/pave-tactile.jpg"
toc:
  enable: false
math:
  enable: false

---

J’ai récemment adopté la ditribution [MX Linux](https://www.mxlinux.org).

C'est une sympathique petite distribution à base de Debian et Xfce, avec une esthétique très discutable (mais modifiable) et des petits outils spécifiques for utiles notamment un gestionnaire de paquets qui inclut des sources externes à debian comme les [flatpacks](https://flatpak.org/).

Mais depuis mon passage dessus sur mon ordinateur portable dell du boulot, je subissais un comportement très bizarre du pavé tactile.
Sans que je comprenne pourquoi, mon navigateur semblait faire des bonds en avant ou en arrière pendant que je rédigeais des emails, paramétrais doctolib pour un client, ou bien pendant que je mettais à jour mes opportunités dans SalesForce.

J'ai fini par réaliser que bien que le clic en tapottant le pavé soit désactivé, bien que le pavé soit désactivé pendant la frappe, une fonctionnalité que j'ignorais envoyait le signal "Reculer d'une page" et "Avancer d'une page" si je touchais les coins inférieurs gauche et droit du pavé tactile, respectivement.

Pour désactiver cette folie :
Dans un terminal :

```
xinput
⎡ Virtual core pointer                    	id=2	[master pointer  (3)]
⎜   ↳ Virtual core XTEST pointer              	id=4	[slave  pointer  (2)]
⎜   ↳ AlpsPS/2 ALPS GlidePoint                	id=13	[slave  pointer  (2)]
⎣ Virtual core keyboard                   	id=3	[master keyboard (2)]
    ↳ Virtual core XTEST keyboard             	id=5	[slave  keyboard (3)]
    ↳ Power Button                            	id=6	[slave  keyboard (3)]
    ↳ Video Bus                               	id=7	[slave  keyboard (3)]
    ↳ Power Button                            	id=8	[slave  keyboard (3)]
    ↳ Sleep Button                            	id=9	[slave  keyboard (3)]
    ↳ Integrated_Webcam_HD: Integrate         	id=10	[slave  keyboard (3)]
    ↳ Dell WMI hotkeys                        	id=11	[slave  keyboard (3)]
    ↳ AT Translated Set 2 keyboard            	id=12	[slave  keyboard (3)]
    ↳ ACPI Virtual Keyboard Device            	id=14	[slave  keyboard (3)]
    ↳ DELL Wireless hotkeys                   	id=15	[slave  keyboard (3)]

```

Ici on voit que mon pavé a l'ID 13.

```
xinput list-props 13


Device 'AlpsPS/2 ALPS GlidePoint':
	Device Enabled (153):	1
	Coordinate Transformation Matrix (155):	1.000000, 0.000000, 0.000000, 0.000000, 1.000000, 0.000000, 0.000000, 0.000000, 1.000000
	Device Accel Profile (282):	1
	Device Accel Constant Deceleration (283):	2.000000
	Device Accel Adaptive Deceleration (284):	1.000000
	Device Accel Velocity Scaling (285):	12.500000
	Synaptics Edges (286):	614, 3481, 307, 1740
	Synaptics Finger (287):	25, 30, 0
	Synaptics Tap Time (288):	180
	Synaptics Tap Move (289):	201
	Synaptics Tap Durations (290):	180, 180, 100
	Synaptics ClickPad (291):	0
	Synaptics Middle Button Timeout (292):	75
	Synaptics Two-Finger Pressure (293):	282
	Synaptics Two-Finger Width (294):	7
	Synaptics Scrolling Distance (295):	-80, -80
	Synaptics Edge Scrolling (296):	0, 0, 0
	Synaptics Two-Finger Scrolling (297):	1, 0
	Synaptics Move Speed (298):	1.000000, 2.000000, 0.075000, 0.000000
	Synaptics Off (299):	1
	Synaptics Locked Drags (300):	0
	Synaptics Locked Drags Timeout (301):	5000
	Synaptics Tap Action (302):	0,0,1,0,1,0,0
	Synaptics Click Action (303):	1, 1, 1
	Synaptics Circular Scrolling (304):	0
	Synaptics Circular Scrolling Distance (305):	0.100000
	Synaptics Circular Scrolling Trigger (306):	0
	Synaptics Circular Pad (307):	0
	Synaptics Palm Detection (308):	1
	Synaptics Palm Dimensions (309):	10, 200
	Synaptics Coasting Speed (310):	8.000000, 50.000000
	Synaptics Pressure Motion (311):	30, 160
	Synaptics Pressure Motion Factor (312):	1.000000, 1.000000
	Synaptics Grab Event Device (313):	0
	Synaptics Gestures (314):	0
	Synaptics Capabilities (315):	1, 1, 1, 1, 1, 0, 0
	Synaptics Pad Resolution (316):	38, 40
	Synaptics Area (317):	0, 0, 0, 0
	Synaptics Noise Cancellation (318):	22, 22
	Device Product ID (277):	2, 8
	Device Node (278):	"/dev/input/event6"

```

Ici le réglage coupable était :

>	Synaptics Tap Action (302):	0,0,1,0,1,0,0

J'ai donc ajouté dans "Session et démarrage" de Xfce une petite commande exécutée à chaque lancement de session :

    xinput set-prop 13 302 0,0,0,0,0,0,0

Et le problème était réglé.

