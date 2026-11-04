# CI/CD Pipeline

## Objective

Automate the execution of API client tests and make test results accessible through a published Allure report.

## CI platform

GitHub Actions.

The workflow runs on a GitHub-hosted ubuntu-latest runner.

## Pipeline stages

### 1. Checkout

The workflow checks out the project source repository.

### 2. Java setup

Java 25 is configured using the Amazon Corretto distribution.

Maven dependency caching is enabled.

### 3. Test execution

The workflow executes:

mvn clean test

JUnit runs the automated test suite.

### 4. Allure report generation

The workflow generates the HTML report using:

mvn io.qameta.allure:allure-maven:3.1.0:report

### 5. Report publication

The generated report is copied to the deployment directory.

Wrangler deploys the static website to Cloudflare Pages.

### 6. Test result traceability

The public portfolio displays execution metadata, including:

- Workflow run number.
- Execution date.
- Commit identifier.
- Runner information.
- Link to the latest Allure report.

## Infrastructure transparency

The CI runner is provided and managed by GitHub.

Cloudflare Pages is used to host the public report.

The source repository remains private. The public showcase does not expose private workflow files or source code.

## Public resources

- Portfolio: https://api-testing-portfolio.pages.dev/
- Allure report: https://api-testing-portfolio.pages.dev/report/
