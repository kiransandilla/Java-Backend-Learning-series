# 01 - Spring Introduction

*Following: [Spring 6 & Spring Boot 3 (Telusko / Navin Reddy)](https://www.udemy.com/course/spring-5-with-spring-boot-2/) — Spring Core section.*

## 📌 What I Learned

- What the Spring Framework is and why it exists — mainly to manage object creation and dependencies for you, instead of doing `new` everywhere manually.
- The core idea of **Inversion of Control (IoC)**: instead of my code creating objects, I hand that responsibility to Spring's container.
- How Spring's `ApplicationContext` works as the container that reads configuration and creates/manages objects (called **beans**) for me.
- How to configure a bean using an XML config file (`appli_context.xml`) instead of creating it manually in code.
- How to fetch a bean from the container using `context.getBean(...)`.

## 🧩 Concepts Covered

- **IoC Container** — the core engine of Spring that manages object lifecycles.
- **Bean** — any object that Spring creates and manages for you.
- **ApplicationContext** — the interface used to interact with the IoC container.
- **XML-based configuration** — declaring beans inside an XML file rather than annotations (this is the "old-school" way, useful for understanding what Spring Boot automates later).

## 💻 Code / Examples I Implemented

- `alien.java` — a simple class with one method, `code()`, that just prints a message. Used as the "bean" being managed by Spring.
- `appli_context.xml` — defines the `alien` bean so Spring knows to create it.
- `App.java` — the entry point. It:
  1. Creates an `ApplicationContext` using `ClassPathXmlApplicationContext`, pointing to `appli_context.xml`.
  2. Fetches the `alien` bean from the container using `getBean("alien")`.
  3. Calls `.code()` on it.

This is the simplest possible example of Spring managing an object for me instead of me writing `new alien()` directly.

## 🐛 Problems / Debugging Issues I Faced

- Hit a `<identifier> expected` / `illegal start of type` compile error early on — turned out to be a missing closing brace (`}`) for the `main` method. A good reminder to always match every opening brace with a closing one, especially when editing generated boilerplate.
- Ran into a `Cannot compile module... JVM target 5` error — my `pom.xml` had no `maven.compiler.release` property set, so Maven defaulted to an ancient Java target (5) that my installed JDK 25 couldn't compile down to. Fixed by adding:
  ```xml
  <maven.compiler.release>25</maven.compiler.release>
  ```
  to the `<properties>` block in `pom.xml`.
- Learned that IntelliJ's "Current File" run option greys out for files without a runnable `main` method (like `alien.java`) — that's expected behavior, not a bug.

## 💡 Important Things I Understood

- Spring's whole value proposition at this stage: **decoupling** — my `App.java` doesn't need to know how `alien` gets built, it just asks the container for it.
- XML config is verbose but makes the wiring very explicit, which helped me actually see what Spring Boot normally hides behind annotations.
- Maven's compiler settings matter a lot for cross-version compatibility — worth checking `pom.xml` early when JDK versions cause weird errors.

## ➡️ What I'll Learn Next

- Moving from XML-based configuration to **annotation-based configuration** (`@Component`, `@Autowired`, `@Configuration`).
- **Dependency Injection** in more depth — constructor injection vs setter injection (still within Spring Core, before moving to Spring Boot).
- Then: Spring Boot, where most of this manual setup gets automated.


