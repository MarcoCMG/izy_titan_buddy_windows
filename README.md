# IsyPowerBuddy – Version Windows (v0.6.0 - v12)

Version bêta de test et de debug pour le monitoring local et le pilotage des installations solaires Isypower (Titans, Micro-onduleurs Deye, Compteur Intelligent et Borne de recharge EVSE).

### ⚠️ Note utile (Appareils Isypower)
> Le remplacement de l'adresse du broker MQTT dans les appareils Isypower est **temporaire**. Il suffit simplement de les supprimer puis de les réajouter dans l'application **IsypowerCloud** pour rétablir automatiquement la configuration d'origine.

---

## Installation & Prérequis

1. Décompressez le fichier ZIP dans un dossier dédié (par ex. `\IsypowerBuddy`).
2. Double-cliquez sur **`Izypower Titan Buddy.exe`**.
3. *Premier lancement :* Windows SmartScreen peut afficher une alerte de protection. Cliquez sur **« Informations complémentaires »** puis **« Exécuter quand même »**.
4. *Pare-feu Windows :* Si une demande d'autorisation apparaît, cochez **« Réseaux privés »** et autorisez l'accès (nécessaire pour détecter vos Titans et micro-onduleurs sur le réseau local).
5. *Astuce :* Clic droit sur l'exécutable > « Envoyer vers » > « Bureau (créer un raccourci) ».

> **Signal Wi-Fi du PC (Windows 11) :** L'affichage du nom et du signal Wi-Fi du PC nécessite que la **Localisation** soit activée (`Paramètres > Confidentialité et sécurité > Localisation`). Le signal Wi-Fi des Titans s'affiche dans tous les cas.

---

## Nouveautés de la Version v12 (Majeure)

### 1. Commandes MQTT intégrées pour les 3 appareils
Dans la section **« Appareils MQTT »**, un nouveau bouton **« Commandes »** ouvre une fenêtre de pilotage complète :
* **Général (3 appareils) :** Rafraîchissement ponctuel (2 minutes à la seconde) et redémarrage de l'appareil.
* **Borne de recharge :** Démarrer ou arrêter la charge, régler la puissance maximale (1 380 W à 7 360 W par paliers de 230 W), choisir le mode de contrôle (*Intelligent, Manuel, Hybride*) et les sources d'énergie autorisées.
* **Smart Meter :** Activation/désactivation du zéro injection (avec seuil), configuration des phases et mode de pilotage de la batterie.
* **Lecture des paramètres :** Permet de récupérer et d'afficher les réglages actuels de la borne et du compteur.
* *Retour d'état :* Chaque commande affiche sa réponse en direct (*« OK »*, *« Refusé »* avec la raison, ou *« Pas de réponse »* après 15 s). Lorsqu'un réglage est validé, l'application met automatiquement à jour l'affichage.

### 2. Sélecteur de rythme de rafraîchissement
Sur chaque fiche d'appareil MQTT, vous pouvez basculer entre deux modes :
* **« 2 min »** : Mode par défaut de l'appareil (économie de trafic).
* **« Permanente »** : Renvoie un rafraîchissement toutes les 105 s pour obtenir des données en flux continu chaque seconde. Ce choix est mémorisé au redémarrage de l'application. Un indicateur visuel vert (*« Rapide · encore 80 s »*) confirme l'état.

### 3. Choix du Compteur Réseau sur la page Globale
Dans le **« Bilan énergétique »**, un nouveau sélecteur **« Compteur réseau »** permet de choisir la source des données :
* Basculez au choix entre les informations issues de la **batterie T1** ou du **Smart Meter** récupéré via les appareils MQTT. La régulation globale utilise directement la source sélectionnée.

---

## Historique des Versions Récentes

### Release Notes – Version v9 & v10 & v11
* **Stabilité des Titans (Page Global) :** Fin des clignotements "Offline" en cas de coupure de communication. Maintien des dernières valeurs avec un indicateur orange (*"Pas de réponse depuis 35 s"*) et retour en mode "Offline" automatique après 5 minutes d'absence totale.
* **Bandeau Micro-onduleurs :** Ajout d'un bandeau compact sous les 4 colonnes (visible en Full HD) affichant la puissance temps réel, un mini-graphique sur 3 h, les détails PV1/PV2, tension, température et énergie totale.
* **Smart Meter & Borne EVSE :** Traduction complète en français des libellés et des échelles (puissances active/réactive/apparente, tensions, courants par phase, énergies, états de la borne et du relais).

---

## Rappel des Fonctionnalités du Tableau de Bord (v6+)

* **Responsive Design 4 Colonnes** (sur grands écrans) : Bilan énergétique, Titans, Flux temps réel et Commandes PID.
* **Régulation PID (Expérimental) :** Permet d'ajuster dynamiquement la charge/décharge des batteries par rapport à une puissance cible sur le réseau (désactivé par défaut).
https://github.com/MarcoCMG/izy_titan_buddy_windows/releases/download/IzyTitanBuddy/IzyPowerBuddy_v0.6_Windows_x64_v6.zip
