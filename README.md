# SpringBootDevelopment


-Apache Maven 
  - software project management tool that makes the software development process simpler and also unifies the development process.

-Spring Initializer
  - a web-based tool that's used to create Spring Boot projects.

- LOGGERS
```
Logging can be used to monitor your application flow, and it is a good way to capture unexpected errors in your program code.
The logger.info method prints a logging message in the console
There are seven different levels of logging: TRACE, DEBUG, INFO, WARN, ERROR, FATAL, and OFF
If we set the logging level to DEBUG, we can see log messages from levels that are log level DEBUG or higher
```

-Types of Classes in DI
```
 - A service is a class that can be used (this is the dependency).
 - The client is a class that uses the dependency. (model)
 - The injector passes the dependency (the service) to the dependent class (the client). (controller)
```


- In Spring Boot, all HTTP requests are handled by controller classes.
  - @RequestMapping annotation, defines the endpoint that the method is mapped to.

- The HAL format 
  - provides a set of conventions for expressing hyperlinks in JSON and it makes your RESTful web service easier to use for frontend developers
  
If you want to use different path naming, you can use the @RepositoryRestResouce annotation in your repository class
Query parameters are annotated with the @Param annotation.
The@Configuration and @EnableWebSecurity annotations switch off the default web security configuration, and we can define our own configuration in this class.
In our security configuration class, we have to define that Spring Security should use users from the database instead of in-memory users.

We should never save the password as plain text to the database. Therefore, we should define a password hashing algorithm.

You can find bcrypt calculators or generators from the internet if you type plain text password and

We can also use Postman and basic authentication

After successful authentication, the requests sent by the client should always contain the JWT that was received in the authentication

The getToken method that handles the login functionality

Spring Security's configure method defines which paths are secured and which are not secured. In the authentication process, we are using filters that allow us to perform some operations before a request goes to the controller or before a response is sent to a client

You can implement IO exceptions in the AuthEntryPoint when the user types the wrong password

The CORS filter intercepts requests, and if these are identified as cross-origin, it adds proper headers to the request.

You can use @DisplayName annotation to give a more descriptive name to your test case

If you are going to use your own server, the easiest way to deploy the Spring Boot application is to use an executable Java ARchive (JAR) file

You can build your project using the mvn clean install command

You have to the change the database connection definition in the application.properties file to the values from the JawsDB Connection Info page

You can also connect to the JawsDB database using HeidiSQL.

You use AWS Amplify to deploy frontend

Docker is a container platform that makes software development, deployment, and shipping easier.

Containers are lightweight and executable software packages that include everything that is needed to run software

You can test that the build has executed correctly by running the JAR file with the following command: java -jar .\cardatabase-0.0.1-SNAPSHOT.jar

With the -t argument, we can give a name to our container

You can check that a new mariadb container exists by typing the docker image ls command

docker run –name cardb -e MYSQL_ROOT_PASSWORD=your_pwd –e MYSQL_DATABASE=cardb mariadb command sets the root user password and creates a new database
