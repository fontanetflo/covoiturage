# Mon covoiturage — V3

Application personnelle de suivi des journées de covoiturage, véhicules et règlements.

## Fonctionnalités
- Trajets par date et véhicule (Ma voiture, Terrence, Laura).
- Historique filtrable par voiture et statistiques.
- Participation mensuelle modifiable, calcul au prorata des jours du lundi au vendredi.
- Paiements partiels ou complets et solde restant.
- PIN à 4 chiffres pour verrouiller l'interface sur cet appareil.
- Chargement GitHub au démarrage et synchronisation automatique après les modifications.
- Affichage de la date et de l'heure de la dernière synchronisation réussie.
- Export/import JSON local.

## Installation GitHub Pages
Remplacer `index.html` dans le dépôt, puis vérifier Settings → Pages : branche `main`, dossier `/ (root)`.

## Connexion GitHub
Dans Paramètres de l'application, renseigner le propriétaire, le dépôt, `main`, `data.json` et le token GitHub Fine-grained. Le token doit être limité à ce dépôt avec Contents: Read and write. Cliquer sur « Enregistrer la connexion ».

Le token est conservé dans le stockage local du navigateur afin de ne pas être ressaisi à chaque ouverture. Il peut être effacé depuis les paramètres. Le PIN est également propre à cet appareil.

## À savoir
- `data.json` est stocké en clair dans le dépôt public : toute personne connaissant le dépôt peut le lire.
- Le PIN ne protège que l'ouverture de l'interface sur cet appareil. Il ne constitue pas une protection des données du dépôt.
- Le token conservé dans le navigateur est accessible au code JavaScript exécuté sur le même site. Ne pas utiliser cette approche si le dépôt contient des données sensibles.
- La synchronisation automatique fonctionne lorsque l'application est ouverte et que l'appareil est connecté à Internet.
- Une sauvegarde locale exportée est recommandée périodiquement.
- Les anciens trajets de la V2 sont repris localement ; ceux sans véhicule identifié sont affectés à « Ma voiture ».
