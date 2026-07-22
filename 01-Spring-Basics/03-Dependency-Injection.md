# Dependency Injection (DI)

## What is a Dependency?

A dependency is an object or class that another class needs to perform its work.

Example:

```java
class Car {
    Engine engine;
}
```

Here, `Engine` is the dependency.

---

## What is Dependency Injection?

Dependency Injection (DI) means Spring creates the required dependency and injects it into the class that needs it.

---

## Without DI

```java
Engine engine = new Engine();
```

---

## With DI

Spring creates the `Engine` Bean and injects it into `Car`.

---

## Difference Between IoC and DI

| IoC | DI |
|------|----|
| Spring controls object creation. | Spring injects the required dependency. |
| Answers: Who creates the object? | Answers: How does the object get its dependency? |

---

## Key Points

- DI reduces coupling.
- Spring performs dependency injection automatically.