# API Testing with Newman & GitHub Actions

Portfolio project demonstrating API test automation using **Postman collections**, **Newman** and **GitHub Actions**.

## What this project demonstrates

- Automated REST API validation with Postman/Newman
- Positive and negative test scenarios
- HTTP status, contract, payload and response-time assertions
- Parameterized base URL using collection variables
- Continuous testing on every push and pull request
- JUnit report generation as a GitHub Actions artifact

## Public API used

The suite runs against **JSONPlaceholder**, a public fake REST API intended for examples and testing. No private credentials, customer data or corporate endpoints are required.

## Test scenarios

| Scenario | Method | Expected result |
| --- | --- | --- |
| Retrieve a single post | GET | 200 + response contract validation |
| Filter posts by user | GET | 200 + non-empty list + user validation |
| Create a post | POST | 201 + payload validation |
| Request a non-existing post | GET | 404 |

## Project structure

```text
.
├── .github/
│   └── workflows/
│       └── newman-tests.yml
├── tests/
│   └── collection.json
├── .gitignore
├── package.json
└── README.md
```

## Run locally

```bash
npm install
npm test
```

## CI/CD

The GitHub Actions workflow runs automatically on pushes and pull requests to `main`. It installs Node.js dependencies, executes the Newman collection and uploads a JUnit report.

## QA skills highlighted

`API Testing` · `Postman` · `Newman` · `REST` · `JavaScript Assertions` · `GitHub Actions` · `CI/CD`

## Portfolio note

This repository is a sanitized portfolio project. All examples use public test data and a public API.
