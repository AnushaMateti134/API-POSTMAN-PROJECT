Manual-API-Testing-Project
# Manual API Testing Project — Postman

## Project Overview

This project demonstrates manual REST API testing using **Postman** and the public practice API [JSONPlaceholder](https://jsonplaceholder.typicode.com/).

The project covers positive testing, negative testing, CRUD operations, response validation, data type validation, HTTP status codes, response headers, and basic performance checks.

The objective is to practice real-world QA testing techniques, document test cases, analyze API behavior, and prepare a reproducible testing portfolio.

## Tools and Technologies

- **Postman** — API requests, collection management, and test execution
- **JavaScript** — Postman response assertions
- **REST API / HTTP** — GET, POST, PUT, PATCH, DELETE, and OPTIONS
- **JSON** — Request and response data formats
- **Microsoft Excel** — Test cases and execution reports
- **GitHub** — Version control and project documentation

## API Under Test

- **API Name:** JSONPlaceholder
- **Base URL:** `https://jsonplaceholder.typicode.com`
- **API Type:** Public fake REST API for testing and learning
- **Authentication:** Not required for the endpoints used in this project

## Test Scope

### 1. Users
- Retrieve all users
- Retrieve a user by ID
- Test non-existing and invalid user IDs
- Create users
- Update users using PUT and PATCH
- Delete users
- Validate user fields, email format, and data types

### 2. Posts
- Retrieve all posts
- Retrieve a post by ID
- Filter posts by user ID
- Create, update, partially update, and delete posts
- Validate response structure and required fields

### 3. Comments
- Retrieve comments
- Filter comments by post ID
- Retrieve comments by ID
- Test invalid comment IDs
- Validate response fields and data types

### 4. Negative and Error-Handling Tests
- Invalid endpoints and resource IDs
- Missing or invalid request fields
- Invalid data types
- Malformed JSON
- Missing or incorrect content-type headers
- Empty request bodies
- Invalid query parameters

### 5. Response Validation
- HTTP status codes
- JSON response structure
- Required fields and data types
- Response headers
- Response time threshold checks
- CRUD response validation

## HTTP Methods Covered

| Method | Purpose |
|---|---|
| GET | Retrieve resources |
| POST | Create resources |
| PUT | Replace or update a resource |
| PATCH | Partially update a resource |
| DELETE | Delete a resource |
| OPTIONS | Inspect supported request options |

## Automated Assertions in Postman

Although this is primarily a manual API testing project, Postman's JavaScript assertions are used to verify expected response behavior.

Examples include:

- Validate HTTP status codes
- Verify that a response is an array or object
- Check required fields
- Validate data types
- Compare returned values with request data
- Verify filtered results
- Check response content type
- Measure response time against a defined threshold

## Execution Summary

The latest supplied Postman Collection Runner screenshot reported:

| Metric | Result |
|---|---:|
| Assertions executed | 101 |
| Passed assertions | 101 |
| Failed assertions | 0 |
| Skipped assertions | 0 |
| Execution errors | 0 |
| Average response time | 366 ms |
| Run duration | 31.688 seconds |

**Important:** These numbers represent assertions reported by Postman, not 101 distinct requests. Some requests displayed “No tests found,” meaning they returned responses without executing assertion checks. Therefore, the figures should not be interpreted as complete validation of every request.

## Project Files

The repository is intended to contain the following files:

```text
Manual-API-Testing-Project/
├── Postman/
│   └── Manual_API_Testing_Project.json
├── Test-Cases/
│   └── Manual_API_Test_Cases.xlsx
├── Test-Execution/
│   └── API_Test_Execution_Report.xlsx
├── Screenshots/
└── README.md
```

The Postman collection JSON should be exported from Postman and added to the `Postman/` folder. The Excel files should be added to their corresponding folders.

## How to Run the Tests

1. Install and open Postman.
2. Download or clone this GitHub repository.
3. Import `Postman/Manual_API_Testing_Project.json` into Postman.
4. Open the imported collection.
5. Confirm that request URLs are correct.
6. Select the collection's **Run** option.
7. Execute the collection using the Collection Runner.
8. Review passed and failed assertions, HTTP status codes, response bodies, and response times.
9. Compare results against the test cases and record any findings.

## Important Limitations

JSONPlaceholder is a simulated API intended for practice and demonstration.

- Create, update, and delete operations are simulated.
- Changes generally do not persist as they would in a production database.
- Its validation rules may differ from those of a real application.
- A response status alone does not prove that an API behaves correctly; results must be compared with defined requirements.

Any unexpected behavior observed during testing should be documented as an observation or mock API limitation unless a confirmed requirement violation has been established.

## Learning Outcomes

This project demonstrates practice with:

- REST API fundamentals
- Positive and negative test scenarios
- CRUD testing
- Request parameters, headers, and JSON bodies
- Response validation using Postman assertions
- Test case design and execution reporting
- Basic defect analysis
- Test documentation and GitHub portfolio organization

## Future Improvements

- Add a formal API requirements document.
- Improve assertion coverage for requests currently showing “No tests found.”
- Add a dedicated defect log with reproducible steps and evidence.
- Organize Postman environments and reusable variables.
- Add additional APIs with authentication and stricter validation rules.
- Introduce automated collection execution through Newman.

## Author

ANUSHA MATETI

This project was created for learning and demonstrating manual API testing skills using Postman.
