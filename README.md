# Projet Mob - IoT

Dans ce repertoire vous allez enregistrez les démarches que votre équipe suit
pour mettre en place une chaîne IoT fonctionnel.

Dans les fichiers `README.md` vous devez décrire en format Markdown chacune des étapes, pensez bien à la répartition des tâches dans votre équipe et si besoin créez d'autres repertoires.

Dans ce fichier décrivez bien chacune des étapes et si vous voulez détailler plus, utilisez des sous-dossiers.

## Équipe de 4 personnes
Notre équipe projet est composée par :

- Medhi TARZOUT - Capteurs/Arduino/STM32
- Cedric DE SA - Beaglebone/Cloud(Ubidots)/Thingy:91
- Julien BLANC-BRUDE - Cloud(TTN)/thingy:91
- Pierrick THOMAS - Beaglebone

## Description du Projet

Le sujet initial est dans le fichier [sujet.md](sujet.md)
Vous devez décrire ici les fonctionnalités et applications de la maquette que vous avez décidé d'implementer.

### Matériel
| Nombre         | Description        |
| ---         | :---         |
|         |         |
|         |         |
|         |         |
|         |         |

### Cas d'utilisation

## Répartition des tâches
Medhi : Arduino, récupération des valeurs des capteurs et envoi via nRF
Cedredic & Julien : Beaglebone, récéption des valeurs

### Suivi journalier

**Mercredi 05/01/2022** :
- Constitution des groupes
- Première prise en main des équipements
- Fait connaissance entre ETI/IRC

**Jeudi 06/01/2022** :
- Cour sur Lora
- TP Lora
- https://ide.mbed.com/compiler IDE (importer DISCO-L072CZ-LRWAN1 en tant que platforme & importer https://os.mbed.com/users/cdupaty/code/LORAWAN-TTN-CAYENNE-LM35/ )
- Fin TP Lora

**Vendredi 07/01/2022** :
- Code Arduino pour récupération des sensors
- Installation OS beaglebone
- Code Arduino emission des données
- Finalisation partie arduino

**Lundi 17/01/2022** :
- Code Arduino pour échange des données
- Debug Beaglebone 
- Poursuite cloud

**Mardi 18/01/2022** :
- Suite dysfonctionnement Beaglebone, utilisation d'un deuxième Arduino pour échange des données.
- Echange des données OK > Passage par Lora pour envoi sur Ubidot > connexion RX TX depuis le deuxieme arduino sur la carte Lora

**Mercredi 18/01/2022** :
- Code Arduino pour échange des données
- Debug Beaglebone 
- Poursuite cloud

**Jeudi 19/01/2022** :
- Cour sur LTE etc..
- Mbed Lorawan code pour envoi des données sur TTN
- Travail de recherche sur le lien série entre Arduino et STM32
- Envoi des données via le lien série OK
- Code python broker MQTT entre cloud ttn et ubidot
- Début de travail de dévellopement parsing de données

**Vendredi 20/01/2022** :
- Finalisation du code et présentation jalon 2
- Rédaction Github
- Paramétrage et prise en main du module Nordic Thingy:91 et du nRF Cloud

## Procédure de mise en place de votre chaîne IoT

- Prise en main des capteurs sur la carte Arduino Uno ou Mega via l'IDE propriétaire Arduino
- Récupération et téléversement du code disponible sur le repository GitHub dans le dossier "5. Arduino"
- Mise en place de la deuxième carte Arduino Nano et du récepteur nRF comme sur la photo repo dans le dossier "5. Arduino"
- Branchement du Arduino Nano en micro-USB à la passerelle Beaglebone (ou Rasberry Pi) en USB
- Configuration de la carte SD permettant de boot sur le Beaglebone Black (BBB)
- Intégration des librairies et codes python sur le cloud on premise disponible une fois après avoir installé et configuré le BBB
- Création d'un compte sur The Think Network (TTN) et Ubidots
- Fournir les label-ID et le token créé dans les plateformes cloud sur le code python de transfert de données
- Lancement des scripts python (tout est disponible dans le dossier "7. BBB")
- Récupération des données et présentation sous forme d'un dashboard via Ubidots

## Conclusions et recommandations

Le projet nous a permis de découvrir les éléments nécessaires pour créer une maquette d'un prototype viable sur le marché.
La découverte du module Nordic Thingy:91 et des protocoles LTE-M / LoRaWAN était un réel plus pour appréhender au mieux le projet.

## Bibliographie
- https://passionelectronique.fr/tutorial-nrf24l01/
- https://www.mikroe.com
- https://github.com/bjarne-hansen/py-nrf24
- https://docs.arduino.cc/hacking/hardware/PinMapping2560
- https://download.mikroe.com/documents/add-on-boards/click-shields/arduino-mega/arduno-mega-click-shield-manual-v100.pdf
- https://beagleboard.org/getting-started
