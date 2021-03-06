---
layout: default
title: Paramétrage du positionnement dans la base
parent: Fabriquer une base RTK
nav_order: 5
---

## Modifier la valeur de la position dans la base RTK

* Revenir dans votre interface **http://centipede.local:8000**

* Modifier **```settings.conf```** et changer la position par celle calculée précédemment **```position='46.164793681 -0.948418958 63.0686'```**

* Enregistrer **```ctrl s```** 

* lancer les commandes **```F2 > Stop Rtcm3```** & **```F2 > Start Rtcm3```** pour redémarrer le service avec la nouvelle configuration.

![cmd_rtcm3](https://jancelin.github.io/docs-centipedeRTK/assets/images/cmd_stop_rtcm.png)
![cmd_rtcm3](https://jancelin.github.io/docs-centipedeRTK/assets/images/cmd_start_rtcm.png)

### Vérifier que la connexion avec le caster fonctionne

* Se rendre dans le dossier **```/rtkbase/rover/Test_Base2caster```**
* Clic droit sur le fichier `**```rtkrcv.conf```** > **```Edit```**
* Modifier la ligne 106 : **```:@caster.centipede.fr:2101/BASE:```** en changeant le nom de la base par la vôtre (attention conserver le **:** à la fin : **```@caster.centipede.fr:2101/FOOO:```**
* Enregistrer **```ctrl s```**

![cmd_rtcm3conf](https://jancelin.github.io/docs-centipedeRTK/assets/images/cmd_rtkrcvconf.png)

* Cliquez sur **```F2 > RTK reveiver OFF```** puis **```F2 > RTK reveiver ON```**

![cmd_rtcm3](https://jancelin.github.io/docs-centipedeRTK/assets/images/param/cmd_rtkrcv1.png)

* Taper **```status 1```** Entrer & Vérifier que vous avez des valeurs sur la ligne **```# of rtcm messages rover: ```**

> ex : **```# of rtcm messages rover: 1004(43),1005(2),1006(2),1012(43),1019(19),1020(14),1042(8),1045(29),1046(29),1077(44),1087(44),1097(44),1127(44)```**

![cmd_rtcm3](https://jancelin.github.io/docs-centipedeRTK/assets/images/param/cmd_rtkrcv2.png) 

* Si l'étape précédente est OK alors votre base GNSS RTK fonctionne bien avec le [caster Centipede](http://caster.centipede.fr:2101).
* Pour sortir taper: **```shutdown```** 


* Déclarer maintenant votre Base sur le Réseau Centipède pour quelle soit visible de tous et bénéficier d'un alerte mail en cas de défaillance.
