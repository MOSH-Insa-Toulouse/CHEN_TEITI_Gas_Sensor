# CHEN_TEITI_Gas_Sensor

## Introduction

Dans le cadre du PTP �Innovative Smart System�, le module intitul� �SMART DEVICES� int�gre les notions de capteurs, de micro-contr�leurs, d�open source hardware et de r�alisation de fichiers de conceptions de cartes �lectroniques sous KiCad. Les enseignements de ce module ont pour objectif de fournir les outils n�cessaires pour la conception et la r�alisation d�une carte �lectronique pouvant communiquer les informations  d�un capteur sur un r�seau bas d�bit tel que LoRa.

Le but de ce projet est alors de concevoir un shield arduino compos� d�un �tage d�adaptation d�imp�dance pour un capteur de gaz qui devra �tre capable d�envoyer des informations sur le r�seau The Thing Networks.
Ce document pr�sente nos d�marches afin de r�aliser les fichiers de conception KiCad de ce shield.

## R�alisation

L�objectif du projet est de r�aliser un sch�ma �lectrique int�grant un capteur de gaz capable d�envoyer les informations sur le r�seau The Thing Networks � travers un module LoRa. Dans un premier temps, nous avons dessin� le sch�matique avec tous les composants n�cessaire � la r�alisation du montage d�adaptation. Ensuite nous avons d�fini le routage entre les diff�rents composants.

### Sch�matique

D�abord nous avons travaill� dans la partie de cr�ation des symboles pour LTC1050 et RN_Breakout2483. Les deux composants ont �t� r�alis� pendant le cours TD. Ensuite nous avons dessin� le sch�ma �lectrique. Pour le sch�ma �lectrique, nous avons utilis� une r�sistance qui repr�sente le capteur de gaz. Apr�s avoir fini de faire le capteur de gaz, nous avons fait le montage d�adaptation d�imp�dance avec l�amplificateur LTC1050. Puis nous avons utilis� le symbole RN_Breakout2483 pour le module LoRa. Quand le sch�ma a �t� cr��, nous l�avons connect� � l�arduino uno.

![alt text][logo1]

[logo1]: https://github.com/MOSH-Insa-Toulouse/CHEN_TEITI_Gas_Sensor/blob/master/schema_capteur.PNG "Sch�ma"

![alt text][logo2]

[logo2]: https://github.com/MOSH-Insa-Toulouse/CHEN_TEITI_Gas_Sensor/blob/master/schema_lora.PNG "RN_Breakout"


### Layout

Avant de r�aliser le routage, nous avons d�fini les r�gles de conception de la carte suivant les param�tres suivants :

![alt text][logo3]

[logo3]: https://github.com/MOSH-Insa-Toulouse/CHEN_TEITI_Gas_Sensor/blob/master/design_rules.PNG "Design Rules"

Ensuite, nous avons import� les composants � partir de la netlist cr�� pr�c�demment depuis le sch�matique.

![alt text][logo4]

[logo4]: https://github.com/MOSH-Insa-Toulouse/CHEN_TEITI_Gas_Sensor/blob/master/pcb_one_face.PNG "PCB"

Enfin, nous avons dessin� les pistes afin de connecter les composants selon le sch�matique.

### Visualisation 3D

![alt text][logo5]

[logo5]: https://github.com/MOSH-Insa-Toulouse/CHEN_TEITI_Gas_Sensor/blob/master/3D_one_face.PNG "3D"

## Conclusion

Nous avons appris � utiliser le logiciel KiCad afin de r�aliser le sch�matique ainsi que le layout d�un circuit �lectronique. Ce circuit permet d�adapter l�utilisation d�un capteur de gaz avec une arduino uno et de transmettre les mesures sur le r�seau The Thing Networks � l�aide d�un module LoRa.
Cependant nous avons rencontr� des difficult�s sur le routage des composants. Les consignes demandaient de dessiner les pistes sur la face du dessus de la carte, mais nous avons d� en mettre une sur la face du dessous entre la broche GND du module RN_Breakout2483 et la broche GND de l�arduino.

