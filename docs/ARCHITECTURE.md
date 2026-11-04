# Technical Architecture

## Overview

The project separates the API client from its automated tests.

## Main components

### Post.java

Represents the data model used by the API client.

### PostApiClient.java

Encapsulates HTTP operations performed through Spring RestClient.

Responsibilities:
- Building HTTP requests.
- Calling the relevant endpoints.
- Processing HTTP responses.
- Mapping response data.

### PostApiClientTest.java

Contains the automated tests for the API client.

It uses:
- JUnit for test execution.
- MockRestServiceServer for simulated HTTP interactions.
- AssertJ for assertions.
- JSONPath for JSON validation.
- Allure for test reporting.

## Simplified interaction flow

JUnit test
    |
    v
PostApiClientTest
    |
    v
PostApiClient
    |
    v
Spring RestClient
    |
    v
MockRestServiceServer
    |
    v
Simulated HTTP response
    |
    v
Assertions and Allure results

## Design considerations

The HTTP client logic is separated from the test logic.

The tests do not require a live external service, making execution predictable and independent of network availability.
