# API Test Scenarios

## Overview

The project currently implements three automated REST API test scenarios using Java and JUnit.

The tests focus on HTTP request handling, response validation and JSON processing.

## Scenario 1 — Retrieve a post (GET)

**Objective:** Verify that the API client can retrieve an existing post.

- HTTP method: GET
- Endpoint: `/posts/1`
- Expected status: `200 OK`
- Expected behavior:
  - The response is successfully received.
  - The JSON response is deserialized.
  - The returned post contains the expected data.

## Scenario 2 — Create a post (POST)

**Objective:** Verify that the API client can submit a new post.

- HTTP method: POST
- Endpoint: `/posts`
- Request body: JSON
- Expected status: `201 Created`
- Expected behavior:
  - The request contains the expected JSON payload.
  - The server accepts the creation request.
  - The response is correctly processed.

## Scenario 3 — Delete a post (DELETE)

**Objective:** Verify that the API client can delete a post.

- HTTP method: DELETE
- Endpoint: `/posts/1`
- Expected status: `204 No Content`
- Expected behavior:
  - The DELETE request is correctly sent.
  - The response status is validated.
  - The empty response is handled correctly.

## Test implementation

The tests use:

- JUnit Jupiter
- Spring RestClient
- MockRestServiceServer
- AssertJ

Mock HTTP responses allow the client behavior to be tested in an isolated and repeatable environment.

## Current scope

These scenarios validate the API client's HTTP behavior.

They do not claim to constitute a complete security test suite or a live end-to-end test against a production API.
