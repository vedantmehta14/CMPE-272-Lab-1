# Lab Assignment 1 – Spring Boot and RESTful Web Services  

## Author  
**Name:** Vedant Tushar Mehta  
**Student ID:** 018207436  

## Objective  
The goal of this assignment is to create a RESTful web service using Spring Boot. This includes setting up a Spring Boot project, creating REST endpoints, and testing the application.  

## Tools and Technologies  
- Java (Version 11 or above)  
- Spring Boot (Version 2.7.0 or the latest stable version)  
- MAVEN  
- Postman (or any REST client)  

## Features Implemented  
1. **Model Class:**  
   - Created a `Greeting` class to hold an ID and content for the greeting message.  
2. **Controller Class:**  
   - Implemented a `GreetingController` class with a `/greeting` endpoint that:  
     - Returns a default greeting (`Hello, World!`) when no name is provided.  
     - Accepts a query parameter (`name`) to return a custom greeting.  
3. **Main Application Class:**  
   - Configured the `SimpleRestServiceApplication` as the main entry point for running the application.  

## Steps to Run the Application  
1. **Project Setup**:  
   - Initialize a Spring Boot project on [Spring Initializr](https://start.spring.io/).  
   - Configure the project with the following settings:  
     - **Project Type:** Maven  
     - **Language:** Java  
     - **Spring Boot Version:** 2.7.0  
     - **Dependencies:** Spring Web  
     - **Packaging:** JAR  
   - Download and unzip the project. Import it into your preferred IDE as a Maven project.  

2. **Run the Application**:  
   - Open a terminal and navigate to the project directory.  
   - Build the project using the following Maven command:  
     ```bash
     mvn clean install
     ```  
   - Run the application using:  
     ```bash
     mvn spring-boot:run
     ```  
   - Alternatively, you can build the JAR file and execute it:  
     ```bash
     java -jar target/simple-rest-service-0.0.1-SNAPSHOT.jar
     ```  
   - The application will be available at [http://localhost:8080](http://localhost:8080).  

3. **Test the Application**:  
   - Open Postman or any REST client.  
   - Perform the following GET requests:  
     1. **Default Greeting**: [http://localhost:8080/greeting](http://localhost:8080/greeting)  
        - Response:  
          ```json
          {
              "id": 1,
              "content": "Hello, World!"
          }
          ```  
     2. **Custom Greeting**: [http://localhost:8080/greeting?name=John](http://localhost:8080/greeting?name=John)  
        - Response:  
          ```json
          {
              "id": 2,
              "content": "Hello, John!"
          }
          ```  

## Testing Notes  
1. **Whitelabel Error Page**:  
   - Accessing the root URL ([http://localhost:8080](http://localhost:8080)) confirms the server is running, but no route is mapped to the root.  
2. **GET Requests**:  
   - Both default and custom greetings were tested successfully using Postman.  

## Deliverables  
1. **Source Code**: Complete implementation of the Spring Boot project.  
2. **Screenshots**: Evidence of server running and successful responses from the `/greeting` endpoint.  
