# 🚗 Mon covoiturage

Application web personnelle permettant de suivre les journées de covoiturage, les véhicules utilisés, les participations financières et les règlements mensuels.

## Fonctionnalités

* Enregistrement des journées de covoiturage.
* Sélection du véhicule utilisé : Ma voiture, Terrence ou Laura.
* Ajout, modification et désactivation des véhicules.
* Historique des trajets filtrable par véhicule.
* Statistiques d'utilisation par voiture.
* Calcul automatique de la participation mensuelle au prorata des jours ouvrés.
* Gestion des paiements complets et partiels.
* Suivi du solde restant à payer.
* Montant mensuel de référence modifiable dans les paramètres.
* Export et import de sauvegardes JSON.
* Synchronisation manuelle avec GitHub.
* Chiffrement des données avec AES-256-GCM.

## Calcul de la participation

Le montant mensuel de référence est de **40 CHF** par défaut.

Le calcul est effectué selon la formule :

`Participation journalière = Montant mensuel / Nombre de jours ouvrés du mois`

Les jours ouvrés correspondent aux jours du lundi au vendredi. Les jours fériés ne sont pas déduits.

Chaque journée enregistrée correspond à un aller-retour.

## Synchronisation et sécurité

Les données sont stockées localement dans le navigateur et peuvent être synchronisées manuellement avec GitHub.

Le fichier `data.json` contient uniquement les données chiffrées.

Le chiffrement repose sur :

* AES-256-GCM pour le chiffrement des données.
* PBKDF2 avec SHA-256 pour dériver la clé à partir du mot de passe.
* Un sel et un vecteur d'initialisation aléatoires.

La synchronisation nécessite un token GitHub disposant des droits de lecture et d'écriture sur le contenu du dépôt.

**Important :**

* Le token GitHub n'est pas intégré au code source.
* Le token est conservé uniquement en mémoire pendant la session.
* Le mot de passe de chiffrement n'est pas enregistré.
* La perte du mot de passe rend les données chiffrées irrécupérables.
* Le chiffrement protège la confidentialité des données, mais pas contre la suppression ou le remplacement du fichier sur GitHub en cas de compromission du token.

## Installation
