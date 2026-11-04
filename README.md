# API Testing Automation Portfolio

**Personal project | QA Automation | REST API Testing**

An independent Java project demonstrating API test automation, test design, reporting and continuous integration.

**Author:** Helena Le Goff  
**GitHub:** https://github.com/helenaLGF  
**Live portfolio:** https://api-testing-portfolio.pages.dev/

---

## Project overview

This project demonstrates the implementation of automated REST API client tests using Java.

It covers the testing lifecycle, from test design and HTTP request validation to automated execution and reporting.

The project is independently developed and does not contain source code from any employer or client.

## Technology stack

| Technology | Purpose |
|---|---|
| Java 25 | Programming language |
| Maven | Build and dependency management |
| JUnit 6 | Automated test framework |
| Spring RestClient | HTTP client |
| MockRestServiceServer | HTTP request/response simulation |
| AssertJ | Readable assertions |
| JSONPath | JSON response validation |
| Allure | Test reporting |
| GitHub Actions | Continuous integration |
| Cloudflare Pages | Public report hosting |

## Test coverage

The current automated suite contains three main scenarios:

| HTTP method | Scenario | Expected result |
|---|---|---|
| GET | Retrieve an existing post | 200 OK |
| POST | Create a post | Successful creation response |
| DELETE | Delete a post | 204 No Content |

See [Test Scenarios](docs/TEST_SCENARIOS.md) for details.

## Technical documentation

- [Test Strategy](docs/TEST_STRATEGY.md)
- [Test Scenarios](docs/TEST_SCENARIOS.md)
- [Architecture](docs/ARCHITECTURE.md)
- [CI/CD Pipeline](docs/CI_CD.md)
- [Project Scope and Limitations](docs/PROJECT_SCOPE.md)

## Continuous integration

The project uses GitHub Actions to automate test execution.

The workflow:
1. Checks out the source repository.
2. Configures Java 25.
3. Runs Maven tests.
4. Generates an Allure HTML report.
5. Publishes the report to Cloudflare Pages.

The CI execution uses a GitHub-hosted ubuntu-latest runner.

## Live results

**Portfolio website:**  
https://api-testing-portfolio.pages.dev/

**Latest Allure report:**  
https://api-testing-portfolio.pages.dev/report/

## Source code and transparency

The implementation is maintained in a separate private GitHub repository.

This public repository provides project documentation and technical explanations. It does not redistribute private source code.

The CI runner is provided by GitHub. Cloudflare Pages hosts the publicly accessible portfolio and test report.

## About this project

This project is part of my ongoing professional development in QA Automation, API testing and CI/CD.

It demonstrates my approach to test design, automation, maintainability and test result reporting.

---

*Independent personal project — QA Automation.*

## Related resources

- **Live portfolio:** https://api-testing-portfolio.pages.dev/
- **Allure report:** https://api-testing-portfolio.pages.dev/report/
- **Public showcase repository:** https://github.com/helenaLGF/api-testing-portfolio-showcase
- **Author's GitHub profile:** https://github.com/helenaLGF


## Architecture diagram

The following diagram illustrates the API testing workflow:

![API Testing Architecture](docs/architecture.mmd)

See [the architecture documentation](docs/ARCHITECTURE.md) for details.

