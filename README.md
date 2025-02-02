
Overview
The ProductCatalogueServiceProxy is a Spring Boot application that acts as a proxy for managing product catalogs. It uses Spring Boot for the backend service, with support for various functionalities like JPA integration with MySQL, Redis caching, and Eureka client for service discovery.

Technologies & Dependencies

The project is built using Maven and includes the following key dependencies:

- **Spring Boot**: The foundation of the application, including starters like ‘spring-boot-starter-web for building web applications, ‘spring-boot-starter-data-jpa’ for JPA support, and ‘spring-boot-starter-test’ for testing.
- **Lombok**: A library used to reduce boilerplate code by generating getters, setters, constructors, etc.
- **JPA**: Integrated with ‘spring-data-jpa’ for database interaction.
- **MySQL**: A relational database used to store data, with the ‘mysql-connector-j’ driver.
- **Spring Cloud Netflix Eureka Client**: Provides service discovery using Netflix's Eureka service registry.
- **Jedis and Spring Data Redis**: Integrated for Redis support, used for caching and data storage.

Dependencies

- **Spring Boot**: ‘3.2.2’
- **Spring Data JPA**: ‘3.3.4’
- **MySQL Connector**: ‘8.3.0’
- **Spring Cloud Netflix Eureka Client**: ‘4.1.0’
- **Jedis (Redis Client)**: ‘5.2.0’
- **Spring Data Redis**: ‘3.3.4’
- **JUnit and Test Libraries**: ‘spring-boot-starter-test’, ‘assertj-core’, and ‘hamcrest’ for testing purposes.
- **Lombok**: Used to reduce boilerplate code.


Prerequisites
- Java 17
- Maven
- MySQL Database (or any compatible database)
- Redis Server (for caching)









Setup Instructions

•	Clone the Repository: Ensure that MySQL is running, and create a database that will be used by the application. 

•	Database Setup: Ensure that MySQL is running, and create a database that will be used by the application. For example:
1.	sql
2.	Copy
3.	CREATE DATABASE product_catalogue;

•	Configure application.properties: Add the necessary configurations for MySQL and Redis in the application.properties file:
o	properties
1.	Copy
2.	spring.datasource.url=jdbc:mysql://localhost:3306/product_catalogue
3.	spring.datasource.username=root
4.	spring.datasource.password=root_password
5.	spring.jpa.hibernate.ddl-auto=update

6.	spring.redis.host=localhost
7.	spring.redis.port=6379
•	Build the Project: Use Maven to build the project:
1.	bash
2.	Copy
3.	mvn clean install
•	Run the Application: After building the project, you can run the application using:
1.	bash
2.	Copy
3.	mvn spring-boot:run
•	Access the Application: Once the application is running, you can access it via http://localhost:8080.

