Version 0.6 - Version Debug - fonctions expérimentales.

Ceci est la version améliorée Windows de l'application Android, une retouche graphique a été effectuée, elle est fonctionnelle et non limitée.

Version Béta pour test.
Izypower Titan Buddy - version Windows (v0.6.0)
Installation

Decompressez ce fichier ZIP dans un dossier (par ex. \IsypowerBuddy).
Double-cliquez sur "Izypower Titan Buddy.exe".
Au premier lancement, Windows SmartScreen peut afficher "Windows a protégé votre ordinateur" :
cliquez sur "Informations complémentaires" puis "Exécuter quand même".
Si le pare-feu Windows demande l'autorisation, cochez "Réseaux privés" et autorisez :
c'est nécessaire pour trouver vos Titans et micro-onduleurs Deye sur le réseau local.
Astuce : clic droit sur l'exe > "Envoyer vers" > "Bureau (créer un raccourci)".

Le PC doit être connecté au même réseau (box / WiFi) que vos appareils.
Vos réglages sont conservés entre deux lancements.

Signal WiFi du PC
Sur Windows 11, l'affichage du nom et du signal WiFi du PC demande que la
"Localisation" soit activée (Paramètres > Confidentialité et sécurité > Localisation).
Le signal WiFi des Titans s'affiche dans tous les cas.

Nouveautés au 01/11/2026:
zyTitanBuddy Desktop v6 – Nouveau tableau de bord
Version Béta Debug - Certaines actions ne sont pas encore complètement fonctionnelles. MQTT par broker local -PID

Le remplacement de l'IP du broker sur les appareils Izypower fait perdre temporairement le cloud constructeur. Pour le récupérer, il suffit de réassocier les appareils perdus dans l'application officielle Izypower Cloud.

La nouvelle version v6 de l'application de bureau est prête ! Cette mise en majuscule globale repense l'interface pour l'adapter dynamiquement à toutes les tailles d'écran, tout en intégrant un système test de régulation PID.

🖥️ Adaptabilité de l'affichage (Responsive Design)
Sur un grand écran, l'onglet Global affiche désormais 4 colonnes côte à côte :

Bilan énergétique

Titans

Flux temps réel

Commandes PID

Écrans moyens : 2 colonnes.

Petits écrans : 1 colonne.

Confort visuel : Les cartes s'ajustent automatiquement à la hauteur de la fenêtre pour éliminer tout besoin de défilement vertical (no-scroll). L'application s'ouvre désormais plus grande, et en mode maximisé sur les grands écrans.

Graphismes vectoriels : Tout est rendu en vectoriel pour garantir un affichage parfaitement net en Full HD, 2K et 4K.

📦 Contenu de la mise en page & des onglets
Bilan énergétique : Production solaire, consommation de la maison, réseau et batteries. Chaque donnée possède son code couleur dédié :

🟢 Vert : Surplus / réinjection

🔵 Bleu : Charge

🟠 Orange : Consommation de la maison

🔴 Rouge : Importation réseau

Indicateurs inclus : Taux d'autoconsommation, autonomie, totaux journaliers et graphique de la dernière heure.

Titans : Une jauge circulaire pour l'état de charge global (%), suivie d'une carte détaillée par Titan (charge, puissance, température, signal Wi-Fi et état de chaque Link). Un clic sur une carte ouvre la page dédiée du Titan.

Flux temps réel : Lignes animées reliant les panneaux solaires, les Titans, la maison, le réseau et le chargeur VE. La vitesse des flux s'accélère dynamiquement en fonction de la puissance transitée.

Commandes PID : Interrupteur Marche/Arrêt, sélecteur Auto/Manuel, puissance cible sur le réseau, bande morte (deadband) et paramètres avancés. En cours d'exécution, affichage en direct de l'écart par rapport à la cible, de l'ordre envoyé à chaque Titan, d'un graphique de suivi et des journaux d'activité (logs).

🧪 État des tests & Vérifications
Ce qui a été testé : Validation avec deux Titans simulés, un compteur simulé, des panneaux solaires et un chargeur VE, testé sur 3 résolutions de fenêtres différentes. Tous les tests automatiques de l'application passent avec succès.

Ce qui n'a pas été testé :

Aucun test physique réalisé sur un véritable PC Windows ou avec votre matériel réel en conditions réelles.

Les remontées de données des Titans ont été simulées, mais pas leurs réponses effectives aux ordres de régulation.

⚙️ Attention ! Fonctionnement du système de régulation PID - expérimental -
Sécurité par défaut : La régulation est désactivée par défaut ; rien ne change tant que vous ne l'activez pas manuellement.

Comportement en mode test :

L'activation bascule les Titans en mode "Temps réel" et leur transmet des ordres de charge ou de décharge.

La puissance est répartie proportionnellement à la capacité des batteries .

La désactivation remet les batteries en mode "Autoconsommation".

Contrainte technique : L'application doit rester ouverte sur le bureau pour que la boucle de régulation active continue de tourner.

⚠️ Avertissement avant utilisation
Avant de confier le pilotage complet à l'application :

Surveillez attentivement les premières minutes lors de l'activation de la régulation.

Vérifiez que la puissance réseau se maintient bien proche de votre cible et que les Titans s'exécutent correctement en suivant les consignes de la boucle PID.






https://github.com/MarcoCMG/izy_titan_buddy_windows/releases/download/IzyTitanBuddy/IzyPowerBuddy_v0.6_Windows_x64_v6.zip
