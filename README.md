# Library Basics API Testing Project

This project demonstrates API testing and automation using Postman and Newman against the Library APIs.

The collection performs end-to-end validation for:

- Add a Book
- Get Book Details
- Delete a Book

The project also demonstrates:
- Request chaining
- Pre-request scripts
- Assertions and validations
- JSON schema validation
- Response time validation
- Newman execution with HTML reporting

---

# Environment Configuration

Separate Postman environment files are used for QA and UAT execution.
The main difference between environments is the `base_url`.

---

# Prerequisites

Install the following:
## Install Newman
## Install Newman HTML Extra Reporter

# Execution Commands

## Run in UAT Environment


```
newman run Library.basics.postman_collection.json -e UAT.postman_environment.json -r htmlextra
```

---

## Run in QA Environment

```
newman run Library.basics.postman_collection.json -e QA.postman_environment.json -r htmlextra
```

---

# HTML Reports

Execution reports are generated using the `htmlextra` reporter.

Generated reports include:

* Request execution summary
* Passed / Failed tests
* Response details
* Assertion results
* Response timings



---

# API Workflow Covered

## 1. Add Book API

* Creates a new book
* Generates dynamic ISBN
* Stores generated Book ID

## 2. Get Book API

* Retrieves created book using Book ID
* Validates response data
* Performs schema validation

## 3. Delete Book API

* Deletes created book
* Validates successful deletion
* Performs schema validation

---

# Concepts Demonstrated

* REST API Testing
* CRUD Operations
* Postman Collection Variables
* Environment Variables
* Global Variables
* Pre-request Scripts
* Test Scripts
* JSON Schema Validation
* Response Assertions
* Dynamic Data Handling
* Request Chaining
* Newman CLI Execution
* HTML Reporting

---

# Notes

* `base_url` is maintained separately for QA and UAT environments for easier execution and maintenance.
* Random ISBN values are generated during execution to avoid duplicate data issues.
* The collection is designed to support automated execution using Newman.
* Newman HTML Extra reports for QA and UAT executions are attached separately.

##Newman html screenshot sample

###QA ENVIRONMENT
<img width="1012" height="852" alt="image" src="https://github.com/user-attachments/assets/711e982d-4d51-4edb-872b-985422acef81" />



```
```
