# Test Strategy

## 1. Objective

The objective is to validate the behavior of a Java REST API client through automated tests.

The tests focus on HTTP interactions, request construction, response handling and data validation.

## 2. Testing scope

The current suite covers three HTTP operations:

- GET: retrieve a resource.
- POST: submit a resource for creation.
- DELETE: request resource deletion.

The tests are designed to be deterministic and repeatable.

## 3. Test approach

The project uses isolated HTTP tests.

MockRestServiceServer simulates HTTP responses, allowing the client to be tested without depending on an external API or network availability.

This approach makes it possible to verify:

- HTTP method and endpoint.
- Request payload where applicable.
- HTTP response status.
- Response processing.
- JSON data and expected values.

## 4. Test framework and assertions

- JUnit Jupiter: test execution and lifecycle.
- Spring RestClient: HTTP communication.
- MockRestServiceServer: simulated HTTP interactions.
- AssertJ: readable assertions.
- JSONPath: JSON response inspection.
- Allure: test execution reporting.

## 5. Test design principles

- Isolation: tests do not depend on a live external API.
- Repeatability: responses are controlled by the test.
- Readability: test names and assertions describe expected behavior.
- Maintainability: test logic is separated from client implementation.
- Traceability: Allure provides a structured execution report.

## 6. Current limitations

The current suite is a focused API client test suite.

It is not a complete end-to-end test suite, performance test campaign or penetration test.

Additional scenarios can be introduced as the project evolves.
