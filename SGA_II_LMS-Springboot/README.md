# Library Management System

A Spring Boot application that performs CRUD operations to manage books and authors in a library.

## Summary

This project is a web-based Library Management System built using Spring Boot. It showcases basic Create, Read, and Update functionalities for two main entities: Book and Author, which are linked through a one-to-many relationship.

## Key Features

- Add, view, and edit author information  
- Add, view, and edit book details  
- Browse all books written by a specific author  
- Special feature: Display a list of books along with their respective authors using an inner join query  
- Input validation and error handling on forms  
- A responsive user interface designed with Bootstrap  

## Technology Stack

- Java 17  
- Spring Boot 2.7.x  
- Spring Data JPA  
- Spring MVC  
- In-memory H2 Database  
- JSP for rendering views  
- Maven as the build tool  
- Bootstrap 4.5.2 for styling the front-end  

## Requirements

- JDK 17 or newer  
- Maven 3.6+  
- Any modern IDE (e.g., IntelliJ IDEA, Eclipse, VS Code)  

## How to Get Started

### Clone the Repository

```bash
git clone https://github.com/Shalu-Bhati/library-management-system.git
cd library-management-system
```

### Build and Run the Application

```bash
mvn clean install
mvn spring-boot:run
```

You can access the app at `http://localhost:8081`.

### Accessing the Database

The system uses an in-memory H2 database preloaded with sample data. To access the H2 console:

```
http://localhost:8081/h2-console
```

Database connection settings:
- JDBC URL: `jdbc:h2:mem:testdb`  
- Username: `sa`  
- Password: *(empty)*  

## Project Structure

```
spring-boot-crud-app/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── example/
│   │   │           └── springbootcrudapp/
│   │   │               ├── config/
│   │   │               ├── controller/
│   │   │               ├── dto/
│   │   │               ├── entity/
│   │   │               ├── exception/
│   │   │               ├── repository/
│   │   │               └── service/
│   │   ├── resources/
│   │   └── webapp/
│   │       └── WEB-INF/
│   │           └── views/
│   └── test/
│       └── java/
└── pom.xml
```

## Data Model Relationships

- **Author** has a one-to-many relationship with **Book**
  - One author can write multiple books
  - Each book is associated with exactly one author

## How to Use the Application

1. **Home Page**
   - Start from the homepage to navigate between book and author management sections

2. **Author Management**
   - View all authors: Click "View All Authors"
   - Add new author: Click "Add New Author"
   - Edit existing author: Click "Edit" next to the author
   - View author profile: Click "View" next to the author
   - See books by the author: Click "Books" next to the author

3. **Book Management**
   - View all books: Click "View All Books"
   - Add a new book: Click "Add New Book"
   - Edit a book: Click "Edit" next to the book
   - View book details: Click "View" next to the book

4. **Special Feature**
   - View a combined list of books and their authors using an SQL inner join: Click "Books with Authors"

## License

This project is distributed under the MIT License. For more information, see the LICENSE file included in the repository.

## Credits

- Spring Framework Team  
- Bootstrap Developers  
- H2 Database Contributors  
