# Système de Monitoring pour Ruche Connectée | Projet Arduino (PEIP2)

Développement d'un système embarqué de surveillance apicole réalisé en binôme avec **Yassine MHIMDAT** dans le cadre d'un projet technique de deuxième année à **Polytech Marseille**.

---

### Présentation du Projet
L'objectif était de concevoir un objet technique autonome capable de surveiller la santé et l'activité d'une colonie d'abeilles. Le système permet l'acquisition de données environnementales en temps réel et la gestion d'alertes de sécurité.

> **Contrainte :** Projet réalisé en un temps limité (une semaine) incluant la conception, le câblage sur breadboard et la programmation.

---

### Spécificités Techniques (Hardware)
Le prototype repose sur une architecture Arduino et intègre les composants suivants :

* **Capteur DHT11 :** Monitoring précis de la température et du taux d'humidité interne de la ruche.
* **Capteur de Monoxyde de Carbone (CO) :** Détection préventive d'incendies ou d'émissions de gaz nocifs à proximité immédiate.
* **Barrière Laser & Photorecepteur :** Système de comptage des flux (entrées/sorties des abeilles) basé sur l'interruption d'un faisceau laser calibré sur une plage de valeurs spécifique.
* **Interface LCD :** Affichage dynamique des mesures en temps réel.
* **Système d'Alerte LED :** Indicateur visuel passant au rouge en cas de dépassement des seuils critiques (température excessive, humidité hors plage ou détection de CO).

---

### Fonctionnement Logiciel
Le programme gère l'analyse constante des données environnementales par rapport à des seuils définis manuellement :

1. **Analyse des Plages de Valeurs :** Traitement des signaux analogiques et numériques pour assurer une lecture stable.
2. **Gestion des Événements :** Incrémentation automatique du compteur de passages lors de la coupure du faisceau laser.
3. **Sécurité & Alerting :** Comparaison continue des relevés avec les valeurs de référence pour déclencher l'alerte visuelle (LED) en cas d'anomalie.
