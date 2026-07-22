# Inversion of Control (IoC)

## Definition

Inversion of Control (IoC) is a principle where the responsibility of creating and managing objects is transferred from the programmer to the Spring Framework.

---

## Without IoC

```java
Engine engine = new Engine();
```

The programmer creates the object.

---

## With IoC

Spring creates and manages the object.

---

## IoC Container

The IoC Container is responsible for:

- Creating Beans
- Storing Beans
- Managing Beans
- Providing Beans when needed

---

## Key Points

- IoC transfers control to Spring.
- The IoC Container manages Spring Beans.