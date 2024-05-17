
## World Database Restful API
World-Database Restful API by 'Hibernate Haunters' consisting of Imogen, Murad, Mamoon, Irina, Oliver and Daniel👋.


## Project Overview
This project creates a Java application that uses an SQL database containing a list of countries and cities, along with other details. 
This application allows users to query certain fields within the database, following the Spring architecture layout: Entities -> Repository -> Service -> Controller.


## Acceptance Criteria
- Interact with the MySQL World Database
- Use Spring JPA to connect and communicate with the Database
- Use basic CRUD operations
- Provide multiple types of search methods
- Implement the service layer in your application
- Expose RESTful endpoints for client interaction


## Dependencies
- JDK 21
- Spring Boot Starter Data JPA
- Spring Boot Starter Web
- Spring Boot Starter Test (for testing with JUnit and Mockito)
- MySQL Connector/J (for MySQL database connectivity)
- Spring Boot DevTools (for development convenience - OPTIONAL)


## How to Use the Project 

Setup: Ensure you have Java installed on your system. 

    Fork this repository
    Clone the forked repository and import it into yout preferred Java IDE
    Add your contributions (code or documentation)
    Commit and push
    Wait for pull request to be merged

## MySQL Database Connection
- Install MySQL: If you don't have MySQL installed, download and install it from the official website
- For instructions on setting up the MySQL World database, [click here](https://dev.mysql.com/doc/world-setup/en/)
- Configure Spring Boot Application: Update your application.properties file with the MySQL database connection details
  (Please message us privately to gain access to the application property details)

## Using the RESTful API with Postman
- Install Postman: Download and install Postman from the official website.
- Start Spring Boot Application: Make sure your Spring Boot application is running.
- Create a New Request in Postman: Open Postman and create a new request.
- Select HTTP Method and Enter URL: Choose the appropriate HTTP method (GET, POST, etc.) and enter the endpoint URL (e.g., http://localhost:8080/countries).
- Send Request and View Response: Click "Send" to send the request and view the response from the server.

## How to use the Program 

Open the project directory: "Hibernate Haunters" and open the class "App". Ensure the spring boot application is running:

```
  public static void main(String[] args) {
        SpringApplication.run(HibernateHauntersApplication.class, args);
    }
```
Within the main method you can query the SQL database withthe following methods within the bean. Comment out the methods you dont require.
```
            logger.info(String.valueOf(worldService.findCountryWithMostCity()));
            List<CityEntity> result = worldService.find5SmallestDistrictsOfCity("Noord-Holland");
            logger.info(String.valueOf(worldService.returnNumOfCities()));
            logger.info(String.valueOf(result));
            logger.info(cityService.getAllCities().toString());
            logger.info(countryService.getCountryByCode("ABW").toString());
            logger.info(countrylanguageService.getAllCountryLanguages().toString());
```

You can use any combination or frequency of these methods, and by running the program the results of each search will be shown in the console.

To enhance maintainability we created logging functionality using java.util.logging. Our colour-coded logger allows you to easily track the flow of the program, record the state when an important event happens and capture errors or exceptions that occur during runtime. This can be used through the Log class and it's static methods.


##  

📫 If you encounter any bugs, please open up an issue to let us know.
Alternatively, we welcome suggestions for any updates or improvements you would like to see! 
