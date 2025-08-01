# CMI SOAP Service

## Description
Service web SOAP développé avec Spring Boot pour la gestion des produits bancaires. Ce projet démontre l'implémentation d'un service SOAP avec Spring Web Services et JPA pour la persistance des données.

## Technologies utilisées
- **Spring Boot 3.0.6**
- **Spring Web Services** - Pour l'implémentation SOAP
- **Spring Data JPA** - Pour la persistance des données
- **MySQL** - Base de données
- **JAXB** - Pour la génération des classes à partir des XSD
- **Lombok** - Pour réduire le code boilerplate
- **Maven** - Gestion des dépendances

## Prérequis
- Java 17 ou supérieur
- Maven 3.6 ou supérieur
- MySQL 8.0 ou supérieur

## Installation et démarrage
1. Clonez le projet
2. Configurez la base de données MySQL
3. Exécutez les commandes suivantes :
   ```bash
   mvn clean compile
   mvn spring-boot:run
   ```
4. Le service sera disponible sur le port **8888**

## Endpoints SOAP
- **WSDL** : `http://localhost:8888/ws/products.wsdl`
- **Service Endpoint** : `http://localhost:8888/ws`

## Structure du projet
```
src/
├── main/
│   ├── java/
│   │   └── com/example/demosoap/
│   │       ├── gen/           # Classes générées par JAXB
│   │       ├── config/        # Configuration Spring
│   │       ├── endpoint/      # Endpoints SOAP
│   │       └── service/       # Services métier
│   └── resources/
│       ├── xsd/              # Schémas XSD
│       └── application.properties
```

## Tests
Pour tester le service SOAP, vous pouvez utiliser :
- SoapUI (projet inclus : `demosoap-soapui-project.xml`)
- Postman
- Curl avec des requêtes SOAP

## Fichiers de test SoapUI
Le projet contient des fichiers XML de test :
- `account.xml`
- `customer.xml` 
- `transaction.xml`
‣浣⵩潳灡�