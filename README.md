This repository is my day-to-day learning log as I build backend development skills in Java — from core Spring concepts all the way through Spring Boot, databases, security, and eventually full microservices and real projects.

I'm a 3rd-year CSE student learning backend development hands-on. Instead of just watching tutorials, I'm rebuilding every concept myself, breaking things, debugging them, and writing down what I actually understood — not just copying code.

## Roadmap

Following [Spring 6 & Spring Boot 3 (Telusko / Navin Reddy)](https://www.udemy.com/course/spring-5-with-spring-boot-2/) on Udemy, in this order:

| # | Topic | Status |
|---|-------|--------|
| 02 | Spring Core (IoC & DI) | 🟡 In Progress |
| 03 | Spring Boot | ⬜ Not Started |
| 04 | Spring MVC | ⬜ Not Started |
| 05 | Spring Data JPA (incl. Hibernate basics) | ⬜ Not Started |
| 06 | Spring REST | ⬜ Not Started |
| 07 | Spring Security (JWT) | ⬜ Not Started |
| 08 | Microservices | ⬜ Not Started |
| 09 | Docker & Cloud Deployment | ⬜ Not Started |
| 10 | Projects | ⬜ Not Started |

*(This table gets updated as I progress — folders are only created once I actually start that topic. Hibernate isn't a separate stop here since the course folds it into Spring Data JPA — I'll cover it there rather than as its own early section.)*

---

## 📁 Current Progress

- **02-Spring-Core**
  - `01-Spring-Introduction` — Basic Spring Framework setup: `ApplicationContext`, XML bean configuration, and a simple bean (`alien`) wired and called through Spring's IoC container.
---
## 🛠️ Technologies

- Java
- Maven
- Spring Framework / Spring Boot
- Hibernate / JPA *(upcoming)*
- MySQL *(upcoming)*
- Docker *(upcoming)*
- Git & GitHub
- IntelliJ IDEA

---

## 🎯 Projects I Plan to Build

- A small REST API using Spring Boot
- A CRUD app with Spring Boot + JPA + MySQL
- A secured API with Spring Security
- A basic microservices setup with 2+ services talking to each other
(More added as I go)

---

## 📚 My Learning Approach

- Learn a concept → build a tiny working example myself → break it on purpose → fix it → write down what I learned.
- Every topic folder has its own `README.md` covering: what I learned, code I wrote, bugs I hit, and what's next.
- Progress here is daily/weekly, not always polished — this is a learning log, not a portfolio piece (yet).

---

## 📂 Folder Structure

```
Java-Backend-Learning-series/
├── README.md
├── .gitignore
│
├── 02-Spring-Core/
│   ├── 01-Spring-Introduction/
│   │   ├── README.md
│   │   ├── pom.xml
│   │   └── src/
│   └── 02-Dependency-Injection/   (coming soon)
│
├── 03-Spring-Boot/        (coming soon)
├── 04-Spring-MVC/         (coming soon)
├── 05-Spring-Data-JPA/    (coming soon — Hibernate covered here)
├── 06-Spring-REST/        (coming soon)
├── 07-Spring-Security/    (coming soon)
├── 08-Microservices/      (coming soon)
├── 09-Docker-Cloud/       (coming soon)
└── 10-Projects/           (coming soon)
```

Folders are added gradually as I actually learn each topic — this isn't a pre-built skeleton, it grows with my progress.
