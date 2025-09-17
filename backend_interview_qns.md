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




