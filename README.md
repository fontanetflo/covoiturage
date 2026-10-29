
# 🚗 Mon covoiturage

Petite application web personnelle permettant de suivre les journées de covoiturage, calculer sa participation financière et gérer les règlements mensuels.

## Fonctionnalités

- Enregistrer une journée de covoiturage avec sa date.
- Éviter les doublons de dates.
- Calculer automatiquement la participation au prorata des jours ouvrés du mois.
- Consulter le montant dû chaque mois.
- Enregistrer des règlements complets ou partiels.
- Suivre les montants déjà payés et le solde restant.
- Conserver l'historique des trajets et des paiements.
- Exporter et importer une sauvegarde au format JSON.

## Règles de calcul

La participation mensuelle de référence est de **40 CHF**.

Le calcul est effectué selon la formule :

Participation par trajet = Participation mensuelle / Nombre de jours ouvrés du mois

Montant mensuel dû = Participation par trajet × Nombre de journées de covoiturage.

Les jours ouvrés correspondent aux jours du lundi au vendredi. Les jours fériés ne sont pas déduits.

Le montant de référence peut être modifié dans les paramètres.

## Installation et hébergement

L'application est entièrement autonome et fonctionne avec HTML, CSS et JavaScript.

Aucune installation, base de données ou serveur n'est nécessaire.

### Hébergement avec GitHub Pages

1. Créer un dépôt GitHub.
2. Ajouter le fichier `index.html` à la racine du dépôt.
3. Ouvrir **Settings → Pages**.
4. Sélectionner **Deploy from a branch**.
5. Choisir la branche `main` et le dossier `/ (root)`.
6. Enregistrer et attendre la publication.

L'application sera accessible depuis l'adresse fournie par GitHub Pages.

## Stockage des données

Les données sont enregistrées localement dans le navigateur grâce au `localStorage`.

Aucun compte utilisateur ni serveur externe n'est nécessaire.

**Important :**
- Les données ne sont pas automatiquement synchronisées entre plusieurs appareils.
- Il est recommandé d'exporter régulièrement une sauvegarde JSON.
- Une sauvegarde peut être restaurée à tout moment depuis les paramètres.

## Compatibilité

- iPhone / Safari
- Android / Chrome
- Windows / Chrome, Edge, Firefox
- macOS / Safari, Chrome

Application responsive, utilisable sur smartphone et ordinateur.

---

Projet personnel de suivi du covoiturage.
