# HotelWebApp
### Vue d'ensemble
Ce projet est une application de réservation d'hôtel développée en utilisant ReactJS pour le front-end et Spring Boot pour le back-end. L'application propose deux rôles : Admin et Utilisateur. Chaque rôle a des fonctionnalités spécifiques décrites ci-dessous.

### Demo
https://github.com/gems77/HotelWebApp/assets/119235391/ea5f7f74-b19b-4dcd-9b83-80fd74755611

## Caractéristiques
###  Role Admin
#### Les administrateurs disposent des autorisations suivantes :
```
Voir toutes les réservations
Annuler une réservation
Ajouter de nouvelles chambres
Mettre à jour les détails d'une chambre
Supprimer des chambres
```
### Rôle de l'utilisateur
#### Les utilisateurs disposent des autorisations suivantes :
```
Réserver une chambre
Voir leurs réservations
```
### Technologies Utilisées
Front-end: ReactJS, Redux, Axios
Back-end: Spring Boot, Spring Security, JPA, Hibernate
Database: MySQL

### Installation
###### Conditions préalables - Assurez-vous que les éléments suivants sont installés :
Node.js
npm or yarn
Java (JDK 11 or above)
MySQL

#### Configuration de l'interface
##### Naviguez jusqu'au répertoire frontend :
```
cd frontend/HotelWebApp
```
##### Installer les dépendances :
```
npm install
```
##### Démarrer le serveur de développement :
```
npm start
```

### Configuration du back-end
##### Naviguez jusqu'au répertoire du backend :
```
cd backend/HotelWebApplication
```

##### Configurez la connexion à la base de données dans src/main/resources/application.properties :
```
spring.datasource.url=jdbc:mysql://localhost:3306/hotel_booking
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

##### Construire le projet :
```
./mvnw clean install
```
##### Exécutez l'application Spring Boot :
```
./mvnw spring-boot:run
``` 
### Usage
Inscrivez-vous en tant qu'utilisateur ou connectez-vous si vous avez déjà un compte.
Les administrateurs peuvent accéder au tableau de bord pour gérer les salles et les réservations.
Les utilisateurs peuvent consulter les salles disponibles et effectuer des réservations.

### API Endpoints
##### Admin Endpoints
GET /api/admin/bookings - View all bookings
DELETE /api/admin/bookings/{bookingId} - Cancel a booking
POST /api/admin/rooms - Add a new room
PUT /api/admin/rooms/{roomId} - Update room details
DELETE /api/admin/rooms/{roomId} - Delete a room
##### User Endpoints
POST /api/user/bookings - Book a room
GET /api/user/bookings - View user bookings
