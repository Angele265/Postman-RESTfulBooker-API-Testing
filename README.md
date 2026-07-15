# RESTful Booker API Testing with Postman

## Project Overview

This project demonstrates automated API testing of the RESTful Booker application using Postman.

The project covers the complete booking lifecycle, including authentication, booking creation, retrieval, update, partial update, deletion, and negative test scenarios.

The collection can be executed using:
- Postman Collection Runner
- Newman (Command Line)
- GitHub Actions (CI/CD)

---

## Technologies Used

- Postman
- Newman
- JavaScript (Postman Test Scripts)
- Node.js
- Git
- GitHub
- GitHub Actions

---

## Project Structure

```
Postman-RESTfulBooker-API-Testing/
│
├── collections/
│   └── RestfulBooker.postman_collection.json
│
├── environments/
│   └── QA.postman_environment.json
│
├── reports/
│
├── .github/
│   └── workflows/
│       └── postman-tests.yml
│
├── package.json
├── README.md
└── .gitignore
```

---

## Test Scenarios

### Authentication

- Generate authentication token

### Positive Test Cases

- Get all bookings
- Create booking
- Get booking by ID
- Update booking (PUT)
- Partial update booking (PATCH)
- Delete booking

### Negative Test Cases

- Get invalid booking ID
- Create booking with missing required data
- Update booking using an invalid token
- Delete a non-existing booking

---

## Features

- Environment variables
- Request chaining
- Dynamic booking ID storage
- Dynamic authentication token
- Automated assertions
- Response validation
- Response time validation

---

## Running the Tests in Postman

1. Import the collection.
2. Import the QA environment.
3. Select the QA environment.
4. Open Collection Runner.
5. Run the collection.

---

## Running the Tests with Newman

Install dependencies:

```bash
npm install
```

Run the collection:

```bash
npm test
```

Or directly:

```bash
newman run collections/RestfulBooker.postman_collection.json -e environments/QA.postman_environment.json
```

---

## Continuous Integration

This project includes a GitHub Actions workflow that automatically executes the Postman collection whenever code is pushed to the `main` branch.

---

## Expected Results

- All API requests execute successfully.
- Positive test cases pass.
- Negative test cases return the expected HTTP status codes.
- Newman reports successful execution.

---

## API Under Test

RESTful Booker

https://restful-booker.herokuapp.com

---

## Author

Angele Velda

QA Automation Engineer

GitHub: https://github.com/YOUR_GITHUB_USERNAME