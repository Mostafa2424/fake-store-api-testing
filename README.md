# Fake Store API Testing 

This repository contains a Postman API test collection for the Fake Store API.
It validates authentication and product-management workflows through positive,
negative, validation, and error-handling test scenarios.

## Project Overview

- **API under test:** Fake Store API
- **Testing type:** API testing
- **Tool:** Postman
- **Collection:** [`collections/fake-store-api-tests.json`](./collections/fake-store-api-tests.json)
- **Scope:** Authentication and product CRUD operations

## Tested Areas

| Module         | Scenarios covered                                       |
| -------------- | ------------------------------------------------------- |
| Authentication | Login, current user, and registration                   |
| Products       | Get all products, get product by ID, invalid product ID |
| Create product | Valid creation, missing required fields, missing stock  |
| Update product | Update product details and validate response data       |
| Delete product | Delete product and validate an empty response           |

## Test Coverage

The collection includes:

- HTTP status-code validation
- JSON response validation
- Response header validation
- Access-token validation
- Environment-variable token chaining
- Positive and negative test scenarios
- Validation and error-response checks

## How to Run

1. Import `collections/fake-store-api-tests.json` into Postman.
2. Create a Postman environment.
3. Set the `baseUrl` variable to the Fake Store API base URL.
4. Run the collection using **Collection Runner** or Newman.
5. Review the test results and assertions.

## Example Validations

- Login returns `200` and provides an access token.
- The access token is saved as an environment variable.
- `/auth/me` returns the authenticated user’s email.
- Product creation returns `201`.
- Invalid product creation returns `422` and an error object.
- A non-existent product returns `404` with `NOT_FOUND`.
- Product deletion returns `204` with an empty response body.

## Skills Demonstrated

- API test design
- REST API testing
- Positive and negative testing
- Request chaining
- Environment variables
- Response assertions
- Error-handling validation
- Postman Collection Runner
