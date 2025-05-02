# 📊 API Testing with Apache JMeter

## 📄 Overview

This project demonstrates RESTful API testing using Apache JMeter. It validates complete CRUD operations (Create, Read, Update, Delete) through sequential test cases and includes parameterized data handling using CSV files.

The tests include:
- POST: Create data using static and CSV-driven payloads
- GET: Fetch and verify data
- PUT: Update field in the data
- DELETE: Remove data and confirm deletion

---

## 🛠️ Tools & Technologies

| Tool           | Description                                  |
|----------------|----------------------------------------------|
| Apache JMeter  | Performance and API testing tool             |
| CSV Data Set Config | Used for parameterization of POST requests |
| JSON Server / Mock API | Sample API for testing             |
| Git & GitHub   | Version control and assignment submission     |

---

## 🧪 Test Plan Structure

The `Test Plan_Assignment_2.jmx` includes the following components:

### Thread Group
- **CRUD Operations Group**: Sequential execution of API tests.

### Samplers
- **POST Request**:
  - Sends static JSON data
  - Also sends data from CSV file using CSV Data Set Config
- **GET Request**:
  - Retrieves data using ID from POST response
  - Validates data values
- **PUT Request**:
  - Update fields in the data
- **DELETE Request**:
  - Deletes the data using ID
- **GET (After DELETE)**:
  - Ensures data no longer exists (empty/null response)

### Listeners (for each request type)
- **View Results Tree**: Visualizes request/response details.
- **Summary Report**: Displays performance metrics.

###  Configuration Elements
- **HTTP Header Manager** – Sets content-type to `application/json`
- **User-Defined Variables** – Base URL, token, user ID, etc.

###  Post-Processors
- **JSON Extractor** – Extracts data like `token` from response

###  Assertions
- **Response Assertion** – Ensures correct HTTP status codes (e.g., 200, 201)
- **Duration Assertion** – Optional, to assert performance limits

---

## 🧾 How to Use

### 🧰 Prerequisites

- Download & install [Apache JMeter](https://jmeter.apache.org/download_jmeter.cgi)
- Clone this GitHub repository
- Start a mock API server (e.g., using `json-server`) or configure the API URL in the test plan


