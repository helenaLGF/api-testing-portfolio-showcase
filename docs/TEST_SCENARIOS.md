# API Test Scenarios

## Overview

The current automated test suite validates three REST API operations using Java and JUnit.

HTTP responses are simulated to ensure deterministic and isolated tests.

## Scenario 1 — Retrieve a post

**HTTP method:** GET  
**Endpoint:** `/posts/1`

**Objective:** Verify that the client can retrieve an existing post.

**Checks:**
- The GET request is sent to the expected endpoint.
- The HTTP response status is validated.
- The response body is processed.
- The returned JSON data is checked.

**Expected HTTP status:** 200 OK

## Scenario 2 — Create a post

**HTTP method:** POST  
**Endpoint:** `/posts`

**Objective:** Verify that the client can submit a new post.

**Checks:**
- The POST request is sent to the expected endpoint.
- The JSON request payload is validated.
- The response is successfully processed.
- The returned data is checked.

The test validates the configured successful creation response.

## Scenario 3 — Delete a post

**HTTP method:** DELETE  
**Endpoint:** `/posts/1`

**Objective:** Verify that the client can request deletion of a post.

**Checks:**
- The DELETE request is sent to the expected endpoint.
- The HTTP response status is validated.
- The response is handled without expecting a response body.

**Expected HTTP status:** 204 No Content

## Execution

The scenarios are automated with JUnit.

HTTP interactions are simulated using Spring MockRestServiceServer.

This ensures that the tests can run without relying on a live external API.
