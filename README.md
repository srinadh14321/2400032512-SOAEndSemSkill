# Round-Robin Load Balancing at API Gateway

**End-Semester Skill Examination Project**

A Spring Boot microservices project demonstrating service discovery and Round-Robin load balancing using Spring Cloud Netflix Eureka and Spring Cloud Gateway.

## Project Overview

This project demonstrates how incoming client requests can be distributed across multiple instances of a Driver Service through an API Gateway.

Eureka Server acts as a service registry, allowing services to register themselves and enabling the Gateway to discover available instances dynamically.

## Technologies Used

- Java 17
- Spring Boot 3.4.4
- Spring Cloud 2024.0.1
- Spring Cloud Netflix Eureka
- Spring Cloud Gateway
- Spring Cloud LoadBalancer
- Maven
- REST API

## Project Architecture

```text
                 Client
                   |
                   v
             API Gateway
              Port 8080
                   |
            Round-Robin
                   |
          Eureka Discovery
                   |
          Eureka Server
             Port 8761
                   |
          -----------------
          |       |       |
        Driver  Driver  Driver
        8081    8082    8083
```

## Project Components

| Component | Port | Purpose |
|---|---:|---|
| Eureka Server | 8761 | Service registration and discovery |
| API Gateway | 8080 | Routes incoming requests |
| Driver Instance 1 | 8081 | Handles driver requests |
| Driver Instance 2 | 8082 | Handles driver requests |
| Driver Instance 3 | 8083 | Handles driver requests |

## Current Implementation Status

- [x] Eureka Server configuration
- [x] Eureka Dashboard running on port 8761
- [ ] Driver Service implementation
- [ ] Three Driver Service instances
- [ ] API Gateway configuration
- [ ] Round-Robin load distribution testing

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/srinadh14321/2400032512-SOAEndSemSkill.git
```

### 2. Open the project

Import the `eureka-server` folder into Spring Tool Suite as an existing Maven project.

### 3. Run Eureka Server

Run `EurekaServerApplication.java` as a Spring Boot application.

### 4. Open Eureka Dashboard

Visit:

http://localhost:8761

## Expected Outcome

The completed implementation will demonstrate dynamic service discovery and Round-Robin request distribution across multiple Driver Service instances.

## Author

**K. Srinadh**

B.Tech – Computer Science and Engineering

KL University

GitHub: [srinadh14321](https://github.com/srinadh14321)

---

*End-Semester Skill Examination Project*
