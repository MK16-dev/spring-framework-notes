Spring Framework Basics

These notes cover the fundamental concepts of the Spring Framework. They are intended for beginners and are written in a structured format suitable for learning, revision, and interview preparation.

1. What is Spring?
Definition

Spring is an open-source Java framework that simplifies enterprise application development. It provides a comprehensive programming and configuration model for building robust, scalable, and maintainable Java applications.

The primary responsibility of the Spring Framework is to create, manage, and provide objects (called Beans) whenever they are required.

Why was Spring created?

As Java applications became larger, developers faced several challenges:

Manual object creation became difficult to manage.
Classes became tightly coupled.
Dependency management increased application complexity.
Testing and maintenance became harder.

Spring addresses these challenges by managing object creation and dependencies automatically.

Without Spring

The programmer is responsible for creating and managing every object.

Student student = new Student();
With Spring

Spring creates, manages, and provides the required objects automatically.

Objects managed by Spring are known as Spring Beans.

Advantages of Spring
Reduces boilerplate code.
Promotes loose coupling.
Simplifies dependency management.
Makes applications easier to maintain and test.
Provides extensive support for enterprise application development.
2. Inversion of Control (IoC)
Definition

Inversion of Control (IoC) is a design principle in which the responsibility of creating and managing objects is transferred from the programmer to the Spring Framework.

Instead of creating objects manually using the new keyword, developers allow Spring to create and manage them.

Without IoC
Engine engine = new Engine();

The programmer creates the object.

With IoC

Spring creates and manages the object inside the IoC Container and provides it whenever required.

Real-Life Example

Imagine visiting a restaurant.

Without Spring, you buy the ingredients, cook the food, and serve yourself.

With Spring, you simply place an order. The restaurant prepares the food and serves it to you.

Similarly, Spring takes responsibility for creating and managing objects.

Key Points
Spring controls object creation.
Objects are managed inside the IoC Container.
Developers focus on business logic instead of object management.
3. IoC Container
Definition

The IoC Container is the core component of the Spring Framework.

It is responsible for:

Creating Spring Beans.
Storing Spring Beans.
Managing the lifecycle of Spring Beans.
Providing Beans whenever they are required by other components.

Without the IoC Container, Spring cannot perform Dependency Injection.

4. Spring Bean
Definition

A Spring Bean is an object that is created, managed, and maintained by the Spring IoC Container.

Example
Student student = new Student();

If the programmer creates this object, it is simply a normal Java object.

If Spring creates and manages the same object, it becomes a Spring Bean.

Key Points
Every Bean is an object.
Not every object is a Spring Bean.
A Bean must be managed by the Spring IoC Container.
5. Dependency
Definition

A Dependency is an object or class that another class requires in order to perform its work.

Example
class Car {

    Engine engine;

}

In this example, the Car class depends on the Engine class.

Therefore, Engine is the dependency.

6. Dependency Injection (DI)
Definition

Dependency Injection (DI) is a design pattern in which Spring creates the required dependency and injects it into the object that needs it.

Instead of creating dependencies manually, Spring automatically provides them.

Without Dependency Injection
class Car {

    Engine engine = new Engine();

}

The Car class creates its own dependency.

With Dependency Injection
@Component
class Engine {

}

@Component
class Car {

    @Autowired
    private Engine engine;

}

Spring creates the Engine Bean and injects it into the Car Bean.

Advantages
Loose coupling.
Better code reusability.
Easier unit testing.
Improved maintainability.
Simplified dependency management.
7. Difference Between IoC and Dependency Injection
Inversion of Control (IoC)	Dependency Injection (DI)
A principle that transfers object creation to Spring.	A technique used by Spring to provide required dependencies.
Answers "Who creates the object?"	Answers "How does an object receive its dependency?"
Implemented by the Spring IoC Container.	One of the ways Spring implements IoC.
8. Annotations
Definition

An Annotation is a special marker (starting with @) placed on classes, methods, fields, or constructors to provide metadata or instructions to the compiler or framework.

Annotations do not directly change the program's business logic but influence how frameworks such as Spring behave.

9. @Component
Definition

@Component tells Spring that a class should be treated as a Spring Bean.

During component scanning, Spring detects classes annotated with @Component, creates their objects, and registers them inside the IoC Container.

Purpose
Creates a Spring Bean.
Registers the Bean with the IoC Container.
Makes the Bean available for Dependency Injection.
10. @Autowired
Definition

@Autowired tells Spring to automatically inject an existing Spring Bean into another Bean.

It does not create a new object. It simply locates an appropriate Bean from the IoC Container and injects it.

Example
@Component
class Car {

    @Autowired
    private Engine engine;

}

When Spring creates the Car Bean, it automatically injects the existing Engine Bean.

Quick Revision
Spring is a Java framework that simplifies application development.
Spring manages objects through the IoC Container.
Objects managed by Spring are called Spring Beans.
IoC transfers the responsibility of object creation from the programmer to Spring.
Dependency Injection allows Spring to provide required dependencies automatically.
@Component creates and registers a Spring Bean.
@Autowired injects an existing Bean into another Bean.
Frequently Asked Interview Questions
What is the Spring Framework?
Why was Spring created?
What is Inversion of Control (IoC)?
What is the IoC Container?
What is a Spring Bean?
What is Dependency Injection?
Explain the difference between IoC and Dependency Injection.
What is an Annotation?
What does @Component do?
What does @Autowired do?
Does @Autowired create an object?
What happens if Spring cannot find a Bean to inject?
Conclusion

The Spring Framework simplifies Java application development by managing object creation, dependency management, and application configuration. Understanding concepts such as IoC, Dependency Injection, Beans, the IoC Container, and basic annotations forms the foundation for learning Spring Boot, Spring Data JPA, Spring Security, and other Spring ecosystem projects.
