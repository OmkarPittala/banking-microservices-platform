# Banking Microservices Platform

A cloud-native banking platform designed using modern microservices architecture principles. The system demonstrates how enterprise banking applications can be built using scalable, secure, and event-driven services.

## Overview

This project simulates a modern banking ecosystem supporting:

* Customer Management
* Account Management
* Transaction Processing
* Notification Services
* API Gateway Routing
* Event-Driven Communication
* Authentication & Authorization

The platform is designed using domain-driven microservices and follows enterprise architecture patterns commonly used in large-scale banking environments.
## System Architecture

```mermaid
flowchart LR
    Client[Web / Mobile Client] --> Gateway[API Gateway]

    Gateway --> Customer[Customer Service]
    Gateway --> Account[Account Service]
    Gateway --> Transaction[Transaction Service]

    Customer --> CustomerDB[(PostgreSQL)]
    Account --> AccountDB[(PostgreSQL)]
    Transaction --> TransactionDB[(PostgreSQL)]

    Transaction --> Kafka[Apache Kafka]
    Kafka --> Notification[Notification Service]
    Notification --> MongoDB[(MongoDB)]

    Gateway --> Auth[Spring Security / OAuth]
    Config[Config Server] --> Customer
    Config --> Account
    Config --> Transaction
    Config --> Notification

Services included:

* Customer Service
* Account Service
* Transaction Service
* Notification Service
* API Gateway
* Config Server

Communication:

* REST APIs
* Apache Kafka Events

## Technology Stack

### Backend

* Java
* Spring Boot
* Spring Cloud
* Spring Security
* Hibernate

### Messaging

* Apache Kafka

### Database

* PostgreSQL
* MongoDB
* Redis

### Cloud & DevOps

* Docker
* Kubernetes
* Jenkins
* AWS Concepts

### Testing

* JUnit
* Mockito

## Key Features

* Customer onboarding
* Account creation and management
* Fund transfers
* Transaction history
* Event-driven notifications
* Role-based security
* Distributed configuration
* Service discovery

## Future Enhancements

* AI-powered customer assistant
* Fraud detection workflows
* Open Banking APIs
* Real-time analytics dashboard

## Project Status

Currently under active development as a portfolio project demonstrating enterprise Java Full Stack and Microservices architecture.
