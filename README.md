# Versla

Versla is a legacy undergraduate web application project developed as a learning-oriented prototype for online classified listings. The system follows a traditional Java EE architecture using JSP, Servlets, DAO-based persistence, and a MySQL backend.

This repository is preserved and documented as an academic project artifact from an earlier stage of software engineering training.

## Formal Academic Summary

### Abstract
Versla is an undergraduate-level web application project developed to understand foundational full-stack web engineering concepts using Java EE technologies. The project models a simplified classified listing platform with role-based interaction for users and moderators. The implementation combines JSP-based views, a servlet controller, DAO-centric persistence, and MySQL database integration.

### Problem Statement
Traditional local buying and selling scenarios require a structured digital interface that allows users to view and publish listings under organized categories. This project addresses that need through a minimal classified system where moderators curate taxonomy and users interact with listing workflows.

## Academic Context

- Project type: Undergraduate mini project (legacy coursework)
- Domain: Classified advertisements and category-based item listing
- Period: Summer 2018
- Intent: Demonstrate end-to-end web development fundamentals with MVC-style separation

## Project Objective

The primary objective of Versla was to design and implement a basic web platform where:

- Users can register and log in
- Moderators can log in and manage listing taxonomy
- Categories and subcategories can be created with image upload support
- Item data can be organized and managed through relational tables

## Technology Stack

- Language: Java
- Web layer: JSP, Servlet API (Java EE)
- Persistence layer: JDBC with DAO pattern
- Database: MySQL
- Front-end: HTML, CSS, Bootstrap 3, jQuery
- Packaging style: Eclipse Dynamic Web Project structure

## Repository Structure

```text
Versla/
  src/com/wise/versla/
    controller/    # Servlet controllers
    dao/           # Data access objects (JDBC queries)
    dto/           # Data transfer / model classes
    util/          # DB and date utilities
  WebContent/
    *.jsp          # JSP views
    image/         # Static assets
    category/      # Uploaded category images
    subCategory/   # Uploaded subcategory images
    WEB-INF/       # Deployment descriptor and libs
```

## Functional Overview

### User Module
- User registration
- User login

### Moderator Module
- Moderator login
- Category creation with image upload
- Subcategory creation with image upload

### Listing/Data Module
- DAO classes for CRUD-style database operations
- Item, category, subcategory, user, and moderator data models

## Architectural Notes

The application follows a classic layered pattern:

1. Presentation Layer (JSP)
2. Controller Layer (Servlet)
3. Persistence Layer (DAO + JDBC)
4. Database Layer (MySQL)

This reflects common undergraduate-era Java web architecture before modern frameworks became standard in student projects.

## Local Setup (Legacy Environment)

This project is intended to run in an older Java EE setup.

1. Install JDK 8 (or a compatible legacy JDK).
2. Use Eclipse IDE with Dynamic Web Project support.
3. Configure Apache Tomcat (8.x recommended).
4. Configure MySQL and create a database named `versla`.
5. Update DB connection details in `src/com/wise/versla/util/DBUtility.java`.
6. Review and update image upload base path in `WebContent/WEB-INF/web.xml`:
   - `context-param` named `imageupload`
7. Add required servlet/JSP libraries and Apache Commons FileUpload dependencies.
8. Deploy on Tomcat and open the app through the server context path.

## Legacy Status and Limitations

This codebase is intentionally preserved close to its original undergraduate form. It includes legacy design and implementation choices, for example:

- MD5-based hashing in old authentication flow
- Hard-coded local paths in deployment configuration
- Monolithic servlet logic in parts of request handling
- Minimal validation and error reporting by current standards

These limitations are retained for academic traceability and historical context.

## Learning Outcomes Demonstrated

- Building an MVC-style Java web application
- Integrating JSP front-end with servlet controllers
- Implementing DAO abstractions over JDBC
- Handling multipart file uploads in Java web applications
- Organizing relational entities and server-side workflows

