# STEP5_API_TESTING.md
API testing for NS-ETHIODIGITAL

## Overview
This file describes the testing strategy for backend APIs, including tools, test cases, and expected outcomes.

## Tools
- Postman / Insomnia for manual API testing
- Automated tests via Jest, Mocha, or Pytest
- CI/CD integration for automated testing

## Test Cases

1. **User Management APIs**
   - Register, login, password reset
   - Role assignment and permissions

2. **Exam APIs**
   - Create, update, delete exams
   - Add/remove items from Item Bank
   - Publish exams for students

3. **Responses & Results APIs**
   - Submit student responses
   - Auto-grading MCQ/TF
   - Retrieve results

4. **Security / Authorization**
   - Unauthorized access should be rejected
   - Role-based access verified

## Notes
- Document request payloads and response formats
- Include edge cases and invalid inputs
- Optional: generate API documentation automatically (Swagger / OpenAPI)
