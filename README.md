# Spring Boot Application
This repository contains a simple Spring Boot application with a REST controller that exposes basic endpoints.

## Project Structure 
### Main Appilication Entry Point 
```bash
  package lk.ac.vau.fas;

  import org.springframework.boot.SpringApplication;
  import org.springframework.boot.autoconfigure.SpringBootApplication;
  
  @SpringBootApplication
  public class MyappApplication {
  
      public static void main(String[] args) {
          SpringApplication.run(MyappApplication.class, args);
      }
  }
```
### REST Controller
```bash
  package lk.ac.vau.fas.controller;

  import org.springframework.web.bind.annotation.GetMapping;
  import org.springframework.web.bind.annotation.RequestMapping;
  import org.springframework.web.bind.annotation.RestController;
  
  @RestController
  @RequestMapping("/app")
  public class AppController {
      
      @GetMapping("/msg")
      public String myMessage() {
          return "Hello SpringBoot";
      }
      
      @GetMapping("/name")
      public String myName() {
          return "My name is SpringBoot";
      }
  }
```
## What is Spring Boot?
Spring Boot is an open-source Java framework used to create stand-alone, production-ready Spring applications with minimal configuration. It simplifies the development of Spring-based applications by providing embedded servers, auto-configuration, and dependency management.

## What is Spring Boot MVC?

Spring Boot MVC (Model-View-Controller) is a module within Spring Boot that provides a structured way to develop web applications. It follows the MVC design pattern, where:

* Model represents data and business logic.
* View handles user interface rendering.
* Controller processes user requests and returns appropriate responses.

## How Spring Boot Works with MVC

1. Controller Layer: Handles HTTP requests and returns responses using `@RestController` and `@RequestMapping`.
2. Service Layer: Contains business logic and is typically marked with `@Service`.
3. Repository Layer: Manages database interactions using Spring Data JPA with `@Repository`.
4. View Layer: Uses Thymeleaf, JSP, or other template engines to display data to users.

Spring Boot provides built-in support for MVC through the `spring-boot-starter-web` dependency.

## Running the Application
To run the application, execute the following command:
```bash
  mvn spring-boot:run
```
Or, run the `main` method in `MyappApplication.java`.
The application will start on `http://localhost:8080`.

### API Endpoints

* GET /app/msg → Returns "Hello SpringBoot"
* GET /app/name → Returns "My name is SpringBoot"

## License
This project is licensed under the MIT License.

