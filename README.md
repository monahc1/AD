# Projet JDBC avec PostgreSQL

Ce projet illustre l'utilisation de **JDBC (Java Database Connectivity)** pour se connecter à une base de données **PostgreSQL** et manipuler des données via une application Java Standalone. L'objectif est de créer une base de données, une table, et d'effectuer des opérations de base (insertion et lecture de données) à l'aide de JDBC.

## Technologies et Versions Utilisées

- **Java**: Version 17 (ou toute version compatible)
- **PostgreSQL**: Version 16.6
- **JDBC Driver**: Version 42.7.5
- **IDE**: VSCode (Visual Studio Code)
- **Système d'exploitation**: Windows (version utilisée : Windows 10/11)

## Pré-requis

Avant de démarrer, assurez-vous que les logiciels suivants sont installés sur votre machine :

1. **PostgreSQL** (version 16.6)
   - Téléchargez et installez PostgreSQL depuis le site officiel : [PostgreSQL Downloads](https://www.postgresql.org/download/)
   - Assurez-vous que le serveur PostgreSQL est en cours d'exécution et que vous pouvez y accéder via `psql`.

2. **Java JDK** (version 17 ou supérieure)
   - Téléchargez et installez le JDK Java à partir de [Oracle JDK](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html) ou utilisez OpenJDK.

3. **JDBC Driver pour PostgreSQL**
   - Téléchargez le driver JDBC pour PostgreSQL depuis [Maven Repository](https://mvnrepository.com/artifact/org.postgresql/postgresql/42.6.0) ou ajoutez-le à votre projet via Maven ou Gradle.

## Configuration de la Base de Données

1. **Installation de PostgreSQL**
   - Suivez les étapes d'installation de PostgreSQL pour Windows, incluant la configuration d'un mot de passe pour l'utilisateur `postgres`.
   
2. **Création de la Base de Données et de la Table**
   Une fois PostgreSQL installé et en cours d'exécution, ouvrez le terminal `psql` et exécutez les commandes suivantes pour créer une base de données et une table :
   
   ```sql
   CREATE DATABASE testdb;
   \c testdb;
   
   CREATE TABLE users (
       id SERIAL PRIMARY KEY,
       name VARCHAR(100),
       email VARCHAR(100) UNIQUE
   );
