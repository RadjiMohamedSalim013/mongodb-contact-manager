Voici le fichier `README.md` modifié sans la section "Contribuer" et "License" :

```markdown
# MongoDB Contact Manager
Ce projet est un exercice de manipulation de données dans MongoDB, où nous gérons une collection de contacts. L'objectif est de pratiquer l'insertion, la mise à jour, la lecture et la suppression de documents dans une base de données MongoDB représentant des contacts avec des informations telles que le nom, prénom, âge, et email.




## Fonctionnalités

- Créer une base de données MongoDB appelée **"contact"**.
- Créer une collection **"contactlist"** pour stocker les contacts.
- Insérer des documents représentant des contacts avec des informations comme le nom, prénom, âge, et e-mail.
- Effectuer des opérations de lecture, mise à jour et suppression sur les contacts.
- Utiliser des requêtes MongoDB pour interroger et filtrer les données des contacts.

## Structure des données

Chaque contact est représenté par un document dans la collection "contactlist" avec les champs suivants :
- **nom** : Le nom de famille du contact.
- **prénom** : Le prénom du contact.
- **email** : L'email du contact.
- **âge** : L'âge du contact.

Exemple de document :

```json
{
  "nom": "Radji",
  "prénom": "Mohamed Salim",
  "email": "radjimohamed013@gmail.com",
  "âge": 10
}
```

## Requêtes

Voici un exemple des requêtes MongoDB utilisées dans ce projet :

- **Afficher tous les contacts** :
```js
db.contactlist.find().pretty();
```

- **Afficher un contact spécifique par ID** :
```js
db.contactlist.find({ _id: ObjectId("votre_id") }).pretty();
```

- **Afficher tous les contacts ayant un âge supérieur à 18** :
```js
db.contactlist.find({ age: { $gt: 18 } }).pretty();
```

- **Afficher les contacts ayant un âge supérieur à 18 et dont le nom contient "ah"** :
```js
db.contactlist.find({ age: { $gt: 18 }, name: /ah/i }).pretty();
```

- **Mettre à jour le prénom d'un contact** :
```js
db.contactlist.updateOne(
  { prénom: "Kefi Seif" },
  { $set: { prénom: "Kefi Anis" } }
);
```

- **Supprimer les contacts ayant un âge inférieur à 5 ans** :
```js
db.contactlist.deleteMany({ age: { $lt: 5 } });
```

## Installation et Prérequis

1. Installez MongoDB sur votre machine si ce n'est pas déjà fait.
2. Ouvrez votre terminal ou ligne de commande et connectez-vous à MongoDB avec la commande suivante :
```bash
mongo
```
3. Créez la base de données et la collection avec les commandes fournies ci-dessus.
4. Vous pouvez ensuite ajouter, interroger, mettre à jour ou supprimer des contacts selon les instructions.
