#  Employee Management System (EMS)

---

##  À propos du projet

**Employee Management System (EMS)** est une application **Full Stack** développée avec **Spring Boot (Backend)** et **React.js (Frontend)**.  
Elle permet de **gérer les employés** d’une entreprise à travers une interface simple, moderne et réactive.

 **Fonctionnalités principales :**
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
├── ems-backend/              # Partie Spring Boot (API REST)
│   ├── controller/            # Gère les requêtes HTTP (REST)
│   ├── dto/                   # Transfert d’objets EmployeeDto
│   ├── entity/                # Entité Employee (modèle JPA)
│   ├── exception/             # Gestion des erreurs personnalisées
│   ├── mapper/                # Conversion entre Entity et DTO
│   ├── repository/            # Interface JpaRepository
│   ├── service/               # Logique métier (interface + implémentation)
│   ├── pom.xml                # Fichier de configuration Maven
│   └── application.properties # Configuration de la base de données
│
├── ems-frontend/              # Partie React (interface utilisateur)
│   ├── components/            # Composants React (Employee, List, Footer, Header)
│   ├── service/               # Fichier Axios pour la communication API
│   ├── App.jsx                # Point d’entrée principal React
│   ├── main.jsx               # Chargement de ReactDOM
│   ├── package.json           # Dépendances NPM
│   └── vite.config.js         # Configuration Vite
│
└── README.md
```

---

##  Technologies utilisées

###  Frontend
-  **React.js (Vite)**
-  **Bootstrap 5**
-  **React Router DOM**
-  **Axios** (pour la communication avec l’API)

###  Backend
-  **Java 17**
-  **Spring Boot 3**
-  **Spring Data JPA + Hibernate**
-  **MySQL**
-  **Lombok**
-  **API RESTful**

---

##  Installation & Exécution

###  Backend (Spring Boot)

1. **Cloner le projet :**
   ```bash
   git clone https://github.com/Wissem1111/Employee-Management-System.git
   ```
2. **Ouvrir le dossier backend** dans *IntelliJ IDEA* ou *Eclipse*.
3. **Configurer la base de données** dans `application.properties` :
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/ems
   spring.datasource.username=root
   spring.datasource.password=root
   spring.jpa.hibernate.ddl-auto=update
   ```
4. **Lancer le projet Spring Boot :**
   ```bash
   mvn spring-boot:run
   ```
5. L’API sera disponible à l’adresse : **http://localhost:8080/api/employees**

---

### Frontend (React.js)

1. Ouvrir le dossier frontend :
   ```bash
   cd ems-frontend
   ```
2. Installer les dépendances :
   ```bash
   npm install
   ```
3. Lancer le serveur React :
   ```bash
   npm run dev
   ```
4. Ouvrir dans le navigateur : **http://localhost:3000**

---

## API Endpoints

| Méthode | Endpoint              | Description                       |
|----------|----------------------|-----------------------------------|
| POST     | `/api/employees`     |  Créer un employé                 |
| GET      | `/api/employees`     |  Récupérer tous les employés      |
| GET      | `/api/employees/{id}`|  Récupérer un employé par ID      |
| PUT      | `/api/employees/{id}`|  Mettre à jour un employé         |
| DELETE   | `/api/employees/{id}`|  Supprimer un employé             |

---

##  Exemple JSON

### Créer un employé
```json
{
  "firstName": "Ali",
  "lastName": "Ben Salah",
  "email": "ali.bensalah@example.com"
}
```

### Réponse
```json
{
  "id": 1,
  "firstName": "Ali",
  "lastName": "Ben Salah",
  "email": "ali.bensalah@example.com"
}
```

---

## Auteur

 **Wissem**  
Étudiant en ingénierie des télécommunications, passionné par le développement web et les technologies modernes.  

 [Portfolio](https://wissembagga.vercel.app/)  
 [GitHub](https://github.com/Wissem1111)

---

##  Licence

Ce projet est sous licence **MIT**.  
Vous êtes libre de l’utiliser, le modifier et le distribuer.

---

**N’oublie pas de laisser une étoile sur le dépôt si tu apprécies ce projet !**
