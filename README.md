# Restful-Booker API Test Automation

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Newman](https://img.shields.io/badge/Newman-CLI-blue?style=for-the-badge&logo=github)
![API Testing](https://img.shields.io/badge/API%20Testing-Automated-green?style=for-the-badge&logo=testing-library)

A complete Postman-based test automation project for the [Restful-Booker API](https://restful-booker.herokuapp.com), covering all major endpoints including authentication, CRUD operations, and health checks. Includes advanced test scenarios, environment variables, schema validations, and CI/CD integration.

---

## 📚 Table of Contents
- [Overview](#overview)
- [API Endpoints](#api-endpoints)
- [Test Coverage](#test-coverage)
- [Environment Setup](#environment-setup)
- [How to Run](#how-to-run)
- [Test Reports](#test-reports)
- [CI/CD Integration](#cicd-integration)
- [License](#license)

---

## 🚀 Overview

This project tests all major features of the Restful-Booker API:

- ✅ **Authentication**: Token-based login
- ✅ **Booking CRUD**: Create, Read, Update, Delete
- ✅ **Health Check**: API `/ping` check
- ✅ **Assertions**: 100+ functional, security & performance tests

---

## 🔗 API Endpoints

| Endpoint               | Method | Description                |
|------------------------|--------|----------------------------|
| `/auth`                | POST   | Generate token             |
| `/booking`             | GET    | Get all booking IDs        |
| `/booking`             | POST   | Create new booking         |
| `/booking/{id}`        | GET    | Get booking by ID          |
| `/booking/{id}`        | PUT    | Full update booking        |
| `/booking/{id}`        | PATCH  | Partial update booking     |
| `/booking/{id}`        | DELETE | Delete booking             |
| `/ping`                | GET    | Health check               |

---

## ✅ Test Coverage

- Functional Testing (status codes, headers, body, schemas)
- Security Testing (auth tokens, injection attempts)
- Performance Testing (response time thresholds)
- Negative Scenarios (invalid/missing data, error handling)

---

## ⚙️ Environment Setup

1. Install **[Postman](https://www.postman.com/downloads/)**  
2. Import the following:
   - Collection file: `collections/RestfulBooker.postman_collection.json`
   - Environment file: `environments/dev.postman_environment.json`
3. Set environment variable:  
   - `baseUrl = https://restful-booker.herokuapp.com`

---

## ▶️ How to Run

### 🟠 Option 1: Postman Runner (GUI)
1. Select collection
2. Click "Run"
3. Choose environment
4. Click **Start Run**

### 🟢 Option 2: Newman CLI
```bash
newman run collections/RestfulBooker.postman_collection.json -e environments/dev.postman_environment.json --reporters cli,html --reporter-html-export reports/report.html
