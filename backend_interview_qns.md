### Topics
1. JAVA concepts
2. Spring boot framework
3. Clean code principles
4. Microservice architecture
5. Test driven architecture
6. Event Driven architecture
7. Refactoring
8. Design Patterns
9. code smells


### JAVA CONCEPTS
1. What is the purpose of the static keyword?
- used to declare variables, methods, nested classes to belong to the class itself rather than instance of the class.

2. Explain OOP concepts in JAVA
- OOP is a programming paradigm that organizes software design around objects (instances of classes). 
  These objects can contain both data (fields or attributes) and behavior (methods or functions). 
  OOP aims to increase code reusability, scalability, and maintainability.

3. Mention and explain the principles of OOP
i) Inheritance 
    Definition: a concept that allows a class to inherit attributes and methods from another class.
    Goal: Promote code reuse and establish a relationship between classes.

ii) Polymorphism
    Definition: The ability for different classes to provide different implementations of the same method.
    Goal: Enable flexibility and scalability in code.

iii) Encapsulation    
    Definition: bundling data (variables) and the methods that operate on that data into a single unit, known as a class. Goal: It primarily aims to achieve data hiding and control access to an object's internal state. 
    * Getter methods (getVariableName()): These methods provide read-only access to the private variables.
    * Setter methods (setVariableName(newValue)): These methods provide controlled write access to the private variables. They can include validation logic to ensure that the data being set is valid and meets specific criteria before updating the variable.

iv) Abstraction
    Definition: Hiding unnecessary implementation details and exposing only the essential features.
    Goal: Focus on what an object does instead of how it does it.

4. What is the purpose of a class constructor?
- used to initalize an instance of a class

5. overloading & overriding
- overloading: allows a class to have multiple methods with the same name but dfft parameters
- overriding: allows a subclass to provide a specific implementation of a method that is already defined in its superclass. 

6. What are design patterns
- Design patterns are typical solutions to commonly occurring problems in software design. They are like pre-made blueprints that you can customize to solve a      recurring design problem in your code.

7. JAVA design patterns
- Creational, structural and behavioral

8. Explain the concept of try-with-resource
- automatically closes resources that implement autoCloseAble. prevents resource leaks

9. Describe garbage collection
- is an automatic cleaning system that finds and removes unused objects to free up memory
- ENTRYPOINT ["java","-jar","-Xms2g", "-Xmx2g", "-XX:+UseG1GC", "-XX:MaxGCPauseMillis=100","/app/app.jar"]

10. Reactive programming 
- is a programming paradigm focused on building asynchronous, non-blocking, event-driven systems that react to data changes or events as they happen.
- differs from imperative programming that focuses on sequential execution of commands

11. Clean code principles
- Focuses on writing software that is clear, readable, maintainable and efficient.
- popularized by Robert C. Martin ("Uncle Bob") in his book Clean Code: A Handbook of Agile Software Craftsmanship.
i) use meaningful names
ii) keep functions small and focused
iii) Avoid code duplication (DRY)
iv) Remove unnecessary complexity
v) SOLID principles

12) Explain SOLID principles
- Single Reponsibility: a module should be responsible for only one part of the softwares functionality
- Open/closed Principle: software entities (classes, fuunction) should be open for extension but closed for modification
- Liskov substitution: Subtypes must be substitutable for their base types without altering the correctness of the program.
- Interface segregation: Clients should not be forced to depend on interfaces they do not use
- Dependency inversion: High-level modules should not depend on low-level modules. Both should depend on abstractions

13) what are code smells?
- Code smells are symptoms of poor design or bad coding practices that may not be bugs, but can lead to bugs, complexity, or maintenance issues later on. 
  The term  was popularized by Martin Fowler in Refactoring: Improving the Design of Existing Code.
  Think of code smells like warning signs.

14) what are the types of code smells?
            1. Long Method
                Problem: A method that does too much or is hard to understand.
                Fix: Split into smaller, focused methods.

            2. Large Class
                Problem: A class that tries to do everything.
                Fix: Apply Single Responsibility Principle. Break it into smaller classes.  

            3. Duplicate Code
                Problem: Same code repeated in multiple places.
                Fix: Extract it into a method or utility class.  

            4. Feature Envy
                Problem: A method in one class relies too much on another class’s data.
                Fix: Move the method to the class it envies.  

            5. God Class (Blob)
                Problem: A central class that knows and does too much.
                Fix: Distribute responsibilities across smaller, cohesive classes.    

            6. Long Parameter List
                Problem: Methods or constructors with too many parameters.
                Fix: Use objects or builders to group parameters.  

            7. Switch Statements
                Problem: Repeated switch/if-else logic, often violating OOP.
                Fix: Use polymorphism (e.g. strategy pattern).  

            8. Speculative Generality
                Problem: Code written for future use cases that never come.
                Delete unused abstractions, parameters, and extension points.

            9. Data Clumps
                Groups of variables that appear together in many places.
                Encapsulate them into a class.

            10. Shotgun Surgery
                Making a small change requires edits in many places.
                Improve cohesion, encapsulate logic.

            11. Primitive Obsession
                Overusing primitives instead of small domain-specific types.
                Create value objects.

            12. Comments Smell
                Problem: Excessive or misleading comments. Often a sign of unclear code.
                Refactor code to be self-explanatory.

15. Tools to Detect Code Smells
- Java: SonarQube, PMD, Checkstyle, IntelliJ IDEA inspections
- JavaScript/TS: ESLint, JSHint
- Python: pylint, flake8
- C#: ReSharper, NDepend

16. How to Deal With Code Smells
- Recognize them early (during code review or testing)
- Refactor in small steps (one smell at a time)
- Write tests first to ensure behavior doesn't break
- Apply SOLID principles to guide structure





### Spring Boot 
1. What is Spring Boot?
- Spring Boot is built on top of the Spring framework to create stand-alone RESTful web applications
 with very minimal configuration and there is no need of external servers to run the application because it has embedded servers like Tomcat and Jetty etc.

2. What are the Spring Boot Starter Dependencies?
- Data JPA starter
- Web starter
- Security starter
- Test Starter
- Thymeleaf starter

3. What is Spring Initializr?
- Spring Initializer is a tool that helps us to create skeleton of spring boot project or project structure by providing a maven or gradle file to build the application. It set up the framework from scratch.

4. What are the basic Spring Boot Annotations?
- @RequestMapping: This annotation is used to map HTTP requests to a specific method in a controller.
- @RestController: This annotation is used to define a RESTful web service controller. 
- @SpringBootApplication: This is the main annotation used to bootstrap a Spring Boot application.
- @ResponseBody: Tells Spring to convert method return values (objects, data) directly into HTTP responses instead of rendering views.

5. What are Profiles in Spring?
- Spring Profiles are like different scenarios for the application depending on the environment.
- You define sets of configurations (like database URLs) for different situations (development, testing, production).

6. How can we check the environment properties in your Spring boot application?
- application.properties file

7. How to enable debugging log in the spring boot application?
- Add the logging level property to application.properties.
- Configure the log pattern to include useful information.
- Run the Spring Boot application.

8. What is dependency Injection and its types?
- Dependency Injection (DI) is a design pattern that enables us to produce loosely coupled components. 
  In DI, an object's ability to complete a task depends on another object. 
  There three types of dependency Injections.
   * Constructor injection
   * Setter injection
   * Field injection

9. What is an IOC container?
- An IoC (Inversion of Control) Container in Spring Boot is essentially a central manager for the application objects that controls the creation, 
  configuration, and management of dependency injection of objects (often referred to as beans), also referred to as a DI (Dependency Injection) container.






