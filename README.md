# SystèmeNONincendie

| | |
|-|-|
|`Author` | Guinea Ana

## Description
  Ce projet consiste à réaliser un système intelligent de contrôle d’accès à une cuisine à l’aide d’une carte Arduino. L’accès est autorisé uniquement après l’introduction d’un code correct via un clavier (keypad), le système fournissant un retour visuel et sonore : une LED verte et un signal sonore pour un code valide, respectivement une LED rouge et un son spécifique pour un code incorrect. 
  En outre, le système intègre une fonction de sécurité en surveillant la température ambiante à l’aide d’un capteur. En cas de détection d’une température élevée, une alarme sonore d’incendie est déclenchée. Celle-ci peut être arrêtée par l’introduction du code correct, permettant ainsi une intervention contrôlée dans des situations gérables.
## Motivation
  J’ai choisi ce sujet car il combine de manière pratique et pertinente des concepts fondamentaux des systèmes embarqués, tels que l’interaction avec l’utilisateur, le contrôle d’accès et la surveillance de l’environnement. Ce projet permet d’appliquer concrètement la carte Arduino, en développant des compétences essentielles en programmation, en électronique et en intégration de capteurs.
  De plus, ce thème présente une utilité réelle, car il peut être appliqué à des systèmes de sécurité et d’automatisation de l’accès à un espace restreint, comme une cuisine ou une salle technique. L’ajout d’une fonction d’alarme en cas de température élevée apporte un aspect de sécurité supplémentaire, rendant le projet plus complexe et plus proche des applications réelles.
  Enfin, ce projet représente une opportunité de développer la pensée logique et d’apprendre à concevoir un système complet, allant du matériel au logiciel, de manière modulaire et facilement extensible.

## Architecture
  L’architecture du projet est construite autour d’une carte Arduino Uno, qui joue le rôle d’unité centrale de contrôle et de coordination de tous les composants. Elle reçoit les signaux des capteurs et du module de saisie du code, traite les informations et envoie des commandes vers les éléments de sortie tels que les LED, le buzzer et le servomoteur.
  La partie d’entrée du système est composée du clavier matriciel (keypad) utilisé pour saisir le code d’accès, ainsi que du capteur de température. Le clavier permet à l’utilisateur d’interagir directement avec le système en entrant un mot de passe, tandis que le capteur surveille en continu l’environnement afin de détecter d’éventuelles situations à risque, comme une augmentation anormale de la température.
  La partie de traitement est assurée par le microcontrôleur Arduino, qui exécute le programme principal. Celui-ci compare le code saisi avec le mot de passe prédéfini et analyse les valeurs provenant du capteur de température. En fonction de ces données, le système prend des décisions logiques et active soit le mode d’accès, soit le mode d’alarme.
  La partie de sortie est constituée des LED, du buzzer, du servomoteur et de l’écran LCD. La LED verte et le signal sonore indiquent un accès autorisé, tandis que la LED rouge et le son d’erreur signalent un code incorrect. En cas de température élevée, le système déclenche une alarme sonore continue, et le servomoteur peut contrôler l’ouverture ou la fermeture de la porte. L’écran LCD affiche des messages utiles pour l’utilisateur, comme la demande de code ou l’état du système.
  Dans l’ensemble, l’architecture du projet est modulaire et bien structurée, permettant une intégration fluide entre le matériel et le logiciel. Elle assure le fonctionnement d’un système automatisé de contrôle d’accès, avec des fonctions supplémentaires de sécurité pour la détection des situations d’urgence.
### Block diagram


<!-- Make sure the path to the picture is correct -->
![Block Diagram](schematics/block_diagram.png)

### Schematic

![Schematic](schematics/kicad_schematic.png)

### Components


<!-- This is just an example, fill in with your actual components -->

| Device | Usage | Price |
|--------|--------|-------|
| Activ Buzzer | Buzzer | [1.5 RON](https://www.optimusdigital.ro/ro/audio-buzzere/635-buzzer-activ-de-3-v.html?search_query=buzzer&results=61) |
| Push Button | Button | [1 RON](https://www.optimusdigital.ro/ro/butoane-i-comutatoare/1119-buton-6x6x6.html?search_query=buton&results=222) |
| Jumper Wires | Connecting components | [7 RON](https://www.optimusdigital.ro/ro/fire-fire-mufate/884-set-fire-tata-tata-40p-10-cm.html?search_query=set+fire&results=110) |
| Breadboard | Project board | [10 RON](https://www.optimusdigital.ro/ro/prototipare-breadboard-uri/8-breadboard-830-points.html?search_query=breadboard&results=145) |

### Libraries

<!-- This is just an example, fill in the table with your actual components -->

| Library | Description | Usage |
|---------|-------------|-------|
| [lib-name1](link-to-lib) | official description of the lib | Used for accesing the peripherals of the microcontroller  |
| [lib-name2](link-to-lib) | official description of the lib | Used for accesing the peripherals of the microcontroller  |

## Log

<!-- write every week your progress here -->

### Week 6 - 12 May

### Week 7 - 19 May

### Week 20 - 26 May


## Reference links

<!-- Fill in with appropriate links and link titles -->

[Tutorial 1](https://www.youtube.com/watch?v=wdgULBpRoXk&t=1s&ab_channel=BenEater)

[Article 1](https://www.explainthatstuff.com/induction-motors.html)

[Link title](https://projecthub.arduino.cc/)
