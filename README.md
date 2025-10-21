# Projet Hibernate - Gestion de Machines et Salles

## Description
Application Java utilisant Hibernate pour gérer des machines et des salles avec leurs relations.

## Structure
- **Entities** : `Machine`, `Salle`
- **Services** : `MachineService`, `SalleService`
- **DAO** : Implémentation générique avec `DaoImpl`

## Technologies
- Java 21
- Hibernate 5.6.9
- MySQL 8.0.29
- JUnit 4.13.2

## Base de données
- **Nom** : `base`
- **Tables** : `salles`, `Machine`
- **Relation** : Une salle peut contenir plusieurs machines (OneToMany)

## Tests Unitaires

### SalleServiceTest
✅ **5 tests réussis** (1 sec 501 ms)
- `testFindAll` - Récupération de toutes les salles
- `testFindById` - Recherche par ID
- `testCreate` - Création d'une salle
- `testDelete` - Suppression d'une salle
- `testUpdate` - Mise à jour d'une salle

### MachineServiceTest
✅ **5 tests réussis** (1 sec 480 ms)
- `testFindBetweenDate` - Recherche par période de dates
- `testFindById` - Recherche par ID
- `testCreate` - Création d'une machine
- `testDelete` - Suppression d'une machine
- `testUpdate` - Mise à jour d'une machine

## Fonctionnalités
- CRUD complet pour les machines et salles
- Recherche de machines par intervalle de dates
- Gestion des relations bidirectionnelles
- Transactions Hibernate automatiques

## Configuration
Fichier `Hibernate.cfg.xml` :
```xml
<property name="hibernate.connection.url">jdbc:mysql://localhost:3306/base</property>
<property name="hibernate.hbm2ddl.auto">update</property>
```

## Exécution
```bash
# Créer les tables (si nécessaire)
java test.CreateTables

# Lancer les tests
mvn test

# Exécuter l'application
java test.Test
```

## Résultats
Tous les tests passent avec succès, confirmant le bon fonctionnement des opérations CRUD et des requêtes Hibernate.

## Screenshots

<img width="1751" height="974" alt="image" src="https://github.com/user-attachments/assets/4ecba67a-df44-48ee-abbb-88fb18abb0e4" />
<img width="1776" height="729" alt="image" src="https://github.com/user-attachments/assets/f10629a0-e744-4ad8-8094-4e1f47008833" />
<img width="1776" height="729" alt="image" src="https://github.com/user-attachments/assets/da9c1ad6-813f-4fd8-a327-fb613ab4753c" />



