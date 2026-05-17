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
<img width="1013" height="747" alt="Block diagram-Guinea Ana" src="https://github.com/user-attachments/assets/afbde0ef-3069-4b3c-a9c0-5e469c1f391d" />


<!-- Make sure the path to the picture is correct -->
![Block Diagram](schematics/block_diagram.png)

### Schematic

[Schema Proiect.zip] [Schema Proiect.zip](https://github.com/user-attachments/files/27906854/Schema.Proiect.zip)





### Components


<!-- This is just an example, fill in with your actual components -->

| Device | Usage | Price |
|--------|--------|-------|
| Arduino Uno R3 | microcontrôleur principal, exécute tout le système | [40–80 RON](https://www.emag.ro/kit-de-pornire-super-pentru-arduino-pentru-placa-de-testare-uno-r3-motor-pas-cu-pas-servo-sg90-lcd-1602-cablu-de-legatura-tutorial-bk216/pd/DY9KSW3BM/?ref=ohs_buy_again_483369631) |
| Clavier matriciel 4x4 (keypad) | permet la saisie du code d’accès | [15–25 RON](https://www.emag.ro/kit-de-pornire-super-pentru-arduino-pentru-placa-de-testare-uno-r3-motor-pas-cu-pas-servo-sg90-lcd-1602-cablu-de-legatura-tutorial-bk216/pd/DY9KSW3BM/?ref=ohs_buy_again_483369631) |
| LED verte | indique que l’accès est autorisé | [1–2 RON](https://www.emag.ro/kit-de-pornire-super-pentru-arduino-pentru-placa-de-testare-uno-r3-motor-pas-cu-pas-servo-sg90-lcd-1602-cablu-de-legatura-tutorial-bk216/pd/DY9KSW3BM/?ref=ohs_buy_again_483369631) |
| LED rouge | indique que l’accès est refusé | [1-2 RON](https://www.emag.ro/kit-de-pornire-super-pentru-arduino-pentru-placa-de-testare-uno-r3-motor-pas-cu-pas-servo-sg90-lcd-1602-cablu-de-legatura-tutorial-bk216/pd/DY9KSW3BM/?ref=ohs_buy_again_483369631) |
| Résistances 220Ω (x2) | protègent les LED contre un courant excessif | [1-2 RON](https://www.emag.ro/kit-de-pornire-super-pentru-arduino-pentru-placa-de-testare-uno-r3-motor-pas-cu-pas-servo-sg90-lcd-1602-cablu-de-legatura-tutorial-bk216/pd/DY9KSW3BM/?ref=ohs_buy_again_483369631) |
| Buzzer | génère des signaux sonores d’alerte et de confirmation | [5-10 RON](https://www.emag.ro/kit-de-pornire-super-pentru-arduino-pentru-placa-de-testare-uno-r3-motor-pas-cu-pas-servo-sg90-lcd-1602-cablu-de-legatura-tutorial-bk216/pd/DY9KSW3BM/?ref=ohs_buy_again_483369631) |
| DHT11 temperature sensor | mesure la température ambiante | [10-20 RON](https://www.emag.ro/kit-de-pornire-super-pentru-arduino-pentru-placa-de-testare-uno-r3-motor-pas-cu-pas-servo-sg90-lcd-1602-cablu-de-legatura-tutorial-bk216/pd/DY9KSW3BM/?ref=ohs_buy_again_483369631) |
| LCD 16x2 display | affiche des messages pour l’utilisateur | [20-40 RON](https://www.emag.ro/kit-de-pornire-super-pentru-arduino-pentru-placa-de-testare-uno-r3-motor-pas-cu-pas-servo-sg90-lcd-1602-cablu-de-legatura-tutorial-bk216/pd/DY9KSW3BM/?ref=ohs_buy_again_483369631) |
| SG90 micro servo motor | ouvre et ferme mécaniquement la porte | [15-25 RON](https://www.emag.ro/kit-de-pornire-super-pentru-arduino-pentru-placa-de-testare-uno-r3-motor-pas-cu-pas-servo-sg90-lcd-1602-cablu-de-legatura-tutorial-bk216/pd/DY9KSW3BM/?ref=ohs_buy_again_483369631) |





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
