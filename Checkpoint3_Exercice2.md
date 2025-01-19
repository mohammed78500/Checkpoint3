Partie 1 : Gestion des utilisateurs

Q.2.1.1 Sur le serveur, créer un compte pour ton usage personnel.

![Capture d'écran 2025-01-17 121714](https://github.com/user-attachments/assets/689979b6-865d-4c64-b16f-66fe927f08fe)

Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?

Je peux utiliser un mot de passe fort,limiter les droits d'accès,configurer un SSH,faire des mises à jour,utiliser un pare-feu,faire une surveillance des journaux

Partie 2 : Configuration de SSH

Q.2.2.1 Désactiver complètement l'accès à distance de l'utilisateur root.

![Capture d'écran 2025-01-17 130321](https://github.com/user-attachments/assets/9765abbd-8e98-4e3c-9f3f-807ca473133d)

Q.2.2.2 Autoriser l'accès à distance à ton compte personnel uniquement

![Capture d'écran 2025-01-17 132009](https://github.com/user-attachments/assets/18a1fbbb-37f4-4f92-a759-1c3920951c27)

Q.2.2.3 Mettre en place une authentification par clé valide et désactiver l'authentification par mot de passe

Partie 3 : Analyse du stockage

Q.2.3.1 Quels sont les systèmes de fichiers actuellement montés ?

![Capture d'écran 2025-01-17 153403](https://github.com/user-attachments/assets/942a2d6d-b8e2-4ab8-8fff-391da5f5e05d)

Q.2.3.2 Quel type de système de stockage ils utilisent ?

![Capture d'écran 2025-01-17 153444](https://github.com/user-attachments/assets/eaa50072-c565-4ef1-82e6-545645f41ab4)

Q.2.3.3 Ajouter un nouveau disque de 8,00 Gio au serveur et réparer le volume RAID

![Capture d'écran 2025-01-18 232903](https://github.com/user-attachments/assets/713ff5ce-3243-434d-a7f4-7dff0de871a3)

![Capture d'écran 2025-01-19 000215](https://github.com/user-attachments/assets/960a1f06-c30b-4162-9bb0-6f77eefb0dea)

Q.2.3.4 Ajouter un nouveau volume logique LVM de 2 Gio qui servira à héberger des sauvegardes. Ce volume doit être monté automatiquement à chaque démarrage dans l'emplacement par défaut : /var/lib/bareos/storage.

Q.2.3.5 Combien d'espace disponible reste-t-il dans le groupe de volume ?

Partie 4 : Sauvegardes

Q.2.4.1 Expliquer succinctement les rôles respectifs des 3 composants bareos installés sur la VM

Il y bareos-dir qui est un composant principal qui gère l'ensemble du système de sauvegarde.Il permet de planifier les travaux de sauvegarde,il gère les clients et les ressources et supervise l'ensemble du processus de sauvegarde et de restauration.Il est responsable de la coordination entre les différents composants

Il y a bareos-sd il est chargé de la gestion des données de sauvegarde.Il reçoit les données de sauvegarde et il est aussi responsable de la récupération des données lors des restaurations

Il y a bareos-fd il est installé sur machines que l 'on souhaite sauvegarder.Il collecte les données à sauvegader et les envoie au bareos-dir pour qu'elles soient traitées et stockées par le bareos-sd.Il gère aussi les demandes de restauration des données
Partie 5 : Filtrage et analyse réseau

Q.2.5.1 Quelles sont actuellement les règles appliquées sur Netfilter ?

Q.2.5.2 Quels types de communications sont autorisées ?

Q.2.5.3 Quels types sont interdit ?

Q.2.5.4 Sur nftables, ajouter les règles nécessaires pour autoriser bareos à communiquer avec les clients bareos potentiellement présents sur l'ensemble des machines du réseau local sur lequel se trouve le serveur.

Partie 6 : Analyse de logs

Q.2.6.1 Lister les 10 derniers échecs de connexion ayant eu lieu sur le serveur en indiquant pour chacun :

La date et l'heure de la tentative
L'adresse IP de la machine ayant fait la tentative
