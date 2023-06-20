Suiveur de ligne avec capteurs VL6180X

Ce projet consiste en un suiveur de ligne utilisant des capteurs VL6180X. Il permet à un robot de détecter et de suivre une ligne tracée au sol. Le code inclus dans ce dépôt GitHub est destiné à être utilisé avec une plateforme Arduino.

Configuration


Matériel requis
Arduino Uno
Capteurs VL6180X (3)
Servomoteurs (2)
Câblage nécessaire pour connecter les composants

Bibliothèques nécessaires
VL6180X : Bibliothèque pour les capteurs de distance VL6180X
Servo : Bibliothèque pour le contrôle des servomoteurs

Connexions
Capteur 1 (milieu) : Adresse I2C 0x39
Capteur 2 (droite) : Adresse I2C 0x49
Capteur 3 (gauche) : Adresse I2C 0x59
Servomoteur gauche : Connecté à la broche 6 de l'Arduino
Servomoteur droite : Connecté à la broche 4 de l'Arduino

Initialisation
Assurez-vous d'avoir installé les bibliothèques VL6180X et Servo dans votre environnement Arduino.
Câblez les capteurs VL6180X et les servomoteurs conformément aux connexions décrites ci-dessus.
Téléversez le code sur votre Arduino.
Utilisation
Le robot utilisera les capteurs VL6180X pour détecter la ligne et suivre son trajet. Les servomoteurs contrôleront les mouvements du robot en fonction des informations fournies par les capteurs.

Lorsque le capteur 1 détecte une distance inférieure à 145 mm, le robot ajuste sa direction en fonction des lectures des capteurs 2 et 3. Si le capteur 3 indique une distance plus petite que le capteur 2, le robot tourne à droite. Si le capteur 3 indique une distance plus grande que le capteur 2, le robot tourne à gauche.

Si le capteur 1 détecte une distance supérieure ou égale à 145 mm, le robot continue tout droit. Cependant, il prend également en compte les lectures des capteurs 2 et 3 pour effectuer des ajustements supplémentaires si nécessaire.

N'hésitez pas à explorer et à ajuster le code selon vos besoins spécifiques.

Auteur:
Ce projet a été développé par TALBI Yasser et OUBELKAS Bilal 
