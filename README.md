#  Employee Management System (EMS)

---

##  À propos du projet

**Employee Management System (EMS)** est une application **Full Stack** développée avec **Spring Boot (Backend)** et **React.js (Frontend)**.  
Elle permet de gérer les employés d’une entreprise à travers une interface simple et moderne.  

🧾 **Fonctionnalités principales :**
-  Ajouter un employé  
-  Modifier les informations d’un employé  
-  Supprimer un employé  
-  Afficher la liste de tous les employés  
-  Validation des champs côté frontend  

---

##  Structure du projet

```bash

Employee-Management-System/
│
├── ems-backend/             # Partie Spring Boot (API REST)
│   ├── controller/           # Gère les requêtes HTTP
│   ├── dto/                  # Transfert d’objets EmployeeDto
│   ├── entity/               # Entité Employee (JPA)
│   ├── exception/            # Gestion des erreurs personnalisées
│   ├── mapper/               # Conversion entre Entity et DTO
│   ├── repository/           # Interface JPARepository
│   ├── service/              # Logique métier (interface + implémentation)
│   ├── pom.xml               # Fichier de configuration Maven
│   └── application.properties
│
├── ems-frontend/             # Partie React (interface utilisateur)
│   ├── components/           # Composants React (Employee, List, Footer, Header)
│   ├── service/              # Fichier Axios pour la communication API
│   ├── App.jsx               # Point d’entrée principal React
│   ├── main.jsx              # Chargement de ReactDOM
│   ├── package.json          # Dépendances NPM
│   └── vite.config.js
│
└── README.md

**Technologies utilisées**
 *Frontend
     React.js (Vite)
     Bootstrap 5
     React Router DOM
     Axios (communication avec l’API)
 *Backend
     Java 17
     Spring Boot 3
     Spring Data JPA + Hibernate
     MySQL
     Lombok
     RESTful API
---

##  Installation & Exécution
### Backend (Spring Boot)

1. Cloner le projet :
   ```bash
   git clone https://github.com/Wissem1111/Employee-Management-System.git```
2. Ouvrir le dossier backend dans IntelliJ IDEA ou Eclipse.
3. Vérifier les configurations de la base de données dans application.properties :
   ```spring.datasource.url=jdbc:mysql://localhost:3306/ems
      spring.datasource.username=root
      spring.datasource.password=root
      spring.jpa.hibernate.ddl-auto=update```
4.Lancer le projet Spring Boot :
```mvn spring-boot:run```
5. L’API sera disponible à l’adresse :  http://localhost:8080/api/employees

### Frontend (React.js)

1. Ouvrir le dossier frontend/ :
```cd frontend```
2. Installer les dépendances :
```npm install```
3. Lancer le serveur React :
```npm start```
4.Ouvrir dans votre navigateur :  http://localhost:3000

### API Endpoints
```Méthode	 Endpoint	            Description
   POST	    /api/employees	      Créer un employé
   GET	    /api/employees	      Récupérer tous les employés
   GET	    /api/employees/{id}	  Récupérer un employé par ID
   PUT	    /api/employees/{id}	  Mettre à jour un employé
   DELETE	  /api/employees/{id}	  Supprimer un employé```

### Exemple JSON
**Créer un employé :
{
  "firstName": "Ali",
  "lastName": "Ben Salah",
  "email": "ali.bensalah@example.com"
}
**Réponse :
{
  "id": 1,
  "firstName": "Ali",
  "lastName": "Ben Salah",
  "email": "ali.bensalah@example.com"
}

