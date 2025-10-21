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

