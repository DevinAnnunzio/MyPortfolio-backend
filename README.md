# Personal Website Backend

## Overview

This project is a **Spring Boot** backend application for a personal website that serves as both a professional resume and a platform where people can hire my services. The site supports three user roles: **Me**, **Customer**, and **Guest**.

It uses **JDBC** to connect to a **PostgreSQL** database and leverages **Spring Security** with **JWT** tokens for secure authentication and authorization.

The frontend will be built with **Angular**, which will consume the REST APIs exposed by this backend.

---

## Features

- RESTful API built with **Spring Web**
- Database access using **Spring JDBC** and **PostgreSQL**
- Secure authentication & authorization using **Spring Security** and **JWT (OAuth2 Resource Server)**
- Role-based access control for:
  - `ME` (full admin access)
  - `CUSTOMER` (can browse and hire services)
  - `GUEST` (read-only access to public info)
- Designed for deployment on **AWS**
- Uses **Java 17** 
- Project managed with **Maven**

---

## Technologies & Dependencies

- **Spring Boot** (backend framework)
- **Spring Web** (`spring-boot-starter-web`) — REST API support
- **Spring Security** (`spring-boot-starter-security`) — authentication and authorization
- **Spring Security OAuth2 Resource Server** (`spring-boot-starter-oauth2-resource-server`) — JWT token validation
- **Spring JDBC** (`spring-boot-starter-jdbc`) — database interaction via JDBC
- **PostgreSQL JDBC Driver** (`org.postgresql:postgresql`) — connects to PostgreSQL database
- **Java 17** — LTS version for production stability
- **Angular** (frontend framework, separate project)

---

## User Roles & Permissions

| Role      | Description                                         | Permissions                                      |
| --------- | ------------------------------------------------- | ------------------------------------------------|
| `ME`      | Site owner/admin                                   | Full control: manage content, view and respond to customers, edit services |
| `CUSTOMER`| Users who hire services                            | Can browse services, book/hire, manage their bookings and profiles |
| `GUEST`   | Unauthenticated visitors                          | Read-only access to resume and public service info |

---

## Setup & Installation

### Prerequisites

- Java 17 installed on your system
- Maven installed
- PostgreSQL database setup and running
- Angular CLI (for frontend)
- AWS account (optional, for deployment)

---

### Backend Setup

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/personal-website-backend.git
cd personal-website-backend
