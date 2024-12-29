# Projet E-commerce Symfony

## Description

Ce projet implémente une boutique en ligne permettant aux utilisateurs d'acheter des produits. Il inclut des fonctionnalités de gestion des paniers, des utilisateurs et des commandes. Les rôles d'admin et de super admin permettent de gérer les produits et de consulter les commandes non achetées.

## Prérequis

Avant de commencer, assurez-vous d'avoir installé :

- PHP >= 7.2.5
- Composer
- Symfony CLI (optionnel mais recommandé)

### Installation des dépendances

Accédez au dossier du projet et installez les dépendances :

```bash
cd Symfonyecommerce
composer install
```

### Configuration de l'environnement

Dupliquez le fichier `.env` et renommez-le en `.env.local` pour personnaliser votre environnement local. Modifiez les paramètres de connexion à la base de données dans ce fichier.

```bash
cp .env .env.local
```

Dans le fichier `.env.local`, modifiez les paramètres de la base de données :

```ini
DATABASE_URL="mysql://username:password@127.0.0.1:3306/database_name?serverVersion=5.7"
```

### Création de la base de données

Créez la base de données en utilisant la commande suivante :

```bash
php bin/console doctrine:database:create
```

### Exécution des migrations

Si vous avez des migrations à appliquer, exécutez-les avec :

```bash
php bin/console doctrine:migrations:migrate
```

### Démarrer le serveur

Si vous utilisez Symfony CLI, vous pouvez démarrer un serveur de développement local :

```bash
symfony serve
```

Sinon, utilisez la commande PHP pour démarrer un serveur :

```bash
php -S 127.0.0.1:8000 -t public
```

Accédez à l'application via [http://127.0.0.1:8000](http://127.0.0.1:8000).

## Structure du projet

- **src/** : Contient les fichiers sources du projet (contrôleurs, entités, etc.).
- **templates/** : Contient les fichiers de templates Twig (vues).
- **public/** : Contient les fichiers publics accessibles, tels que les images, CSS et JS.
- **config/** : Contient les fichiers de configuration de Symfony.
- **migrations/** : Contient les fichiers de migration de la base de données.

## Entités

Les principales entités du projet sont :

- **Produit** : Représente un produit dans la boutique (nom, description, prix, stock, photo).
- **Utilisateur** : Représente un utilisateur de la boutique (nom, email, mot de passe, rôles).
- **Panier** : Contient les produits ajoutés par un utilisateur.
- **ContenuPanier** : Détaille le contenu d'un panier (produit, quantité, date).

## Auteurs

- **Victor Fernel** : [https://github.com/Wicoco]
- **Théo Jublou** : [https://github.com/IBookki]
