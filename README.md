# CHEN_TEITI_Gas_Sensor

## Introduction

Dans le cadre du PTP “Innovative Smart System”, le module intitulé “SMART DEVICES” intègre les notions de capteurs, de micro-contrôleurs, d’open source hardware et de réalisation de fichiers de conceptions de cartes électroniques sous KiCad. Les enseignements de ce module ont pour objectif de fournir les outils nécessaires pour la conception et la réalisation d’une carte électronique pouvant communiquer les informations  d’un capteur sur un réseau bas débit tel que LoRa.

Le but de ce projet est alors de concevoir un shield arduino composé d’un étage d’adaptation d’impédance pour un capteur de gaz qui devra être capable d’envoyer des informations sur le réseau The Thing Networks.
Ce document présente nos démarches afin de réaliser les fichiers de conception KiCad de ce shield.

## Réalisation

L’objectif du projet est de réaliser un schéma électrique intégrant un capteur de gaz capable d’envoyer les informations sur le réseau The Thing Networks à travers un module LoRa. Dans un premier temps, nous avons dessiné le schématique avec tous les composants nécessaire à la réalisation du montage d’adaptation. Ensuite nous avons défini le routage entre les différents composants.

### Schématique

D’abord nous avons travaillé dans la partie de création des symboles pour LTC1050 et RN_Breakout2483. Les deux composants ont été réalisé pendant le cours TD. Ensuite nous avons dessiné le schéma électrique. Pour le schéma électrique, nous avons utilisé une résistance qui représente le capteur de gaz. Après avoir fini de faire le capteur de gaz, nous avons fait le montage d’adaptation d’impédance avec l’amplificateur LTC1050. Puis nous avons utilisé le symbole RN_Breakout2483 pour le module LoRa. Quand le schéma a été créé, nous l’avons connecté à l’arduino uno.

![alt text][logo1]

[logo1]: https://github.com/MOSH-Insa-Toulouse/CHEN_TEITI_Gas_Sensor/blob/master/schema_capteur.PNG "Schéma"

![alt text][logo2]

[logo2]: https://github.com/MOSH-Insa-Toulouse/CHEN_TEITI_Gas_Sensor/blob/master/schema_lora.PNG "RN_Breakout"


### Layout

Avant de réaliser le routage, nous avons défini les règles de conception de la carte suivant les paramètres suivants :

![alt text][logo3]

[logo3]: https://github.com/MOSH-Insa-Toulouse/CHEN_TEITI_Gas_Sensor/blob/master/design_rules.PNG "Design Rules"

Ensuite, nous avons importé les composants à partir de la netlist créé précédemment depuis le schématique.

![alt text][logo4]

[logo4]: https://github.com/MOSH-Insa-Toulouse/CHEN_TEITI_Gas_Sensor/blob/master/pcb_one_face.PNG "PCB"

Enfin, nous avons dessiné les pistes afin de connecter les composants selon le schématique.

### Visualisation 3D

![alt text][logo5]

[logo5]: https://github.com/MOSH-Insa-Toulouse/CHEN_TEITI_Gas_Sensor/blob/master/3D_one_face.PNG "3D"

## Conclusion

Nous avons appris à utiliser le logiciel KiCad afin de réaliser le schématique ainsi que le layout d’un circuit électronique. Ce circuit permet d’adapter l’utilisation d’un capteur de gaz avec une arduino uno et de transmettre les mesures sur le réseau The Thing Networks à l’aide d’un module LoRa.
Cependant nous avons rencontré des difficultés sur le routage des composants. Les consignes demandaient de dessiner les pistes sur la face du dessus de la carte, mais nous avons dû en mettre une sur la face du dessous entre la broche GND du module RN_Breakout2483 et la broche GND de l’arduino.

