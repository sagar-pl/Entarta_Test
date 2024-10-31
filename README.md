
# Selenium TestNG POM Framework

This project is a **Selenium** automation framework designed with **TestNG** and the **Page Object Model (POM)** design pattern. It helps improve test structure, reusability, and maintainability for automated UI tests on web applications.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Setup](#setup)
- [Framework Structure](#framework-structure)
- [Executing Tests](#executing-tests)
- [Test Reports](#test-reports)

## Features

- **Page Object Model (POM)**: Separates web element locators and page methods, enhancing test readability and reusability.
- **TestNG Integration**: Manages test execution, assertions, parallel testing, and reporting.
- **Custom Reporting**: Generates detailed HTML reports of test execution.

## Requirements

- **Java Development Kit (JDK)** 11 or later
- **Maven** for project build and dependency management
- **IDE** such as Eclipse for development

## Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/sagar-pl/Entarta_Test.git
   cd selenium-testng-pom
   ```

2. **Install dependencies**:
   ```bash
   mvn clean install
   ```

## Framework Structure

The project structure follows the Page Object Model:

- **src/main/java**:
  - **pages**: Classes representing each page, encapsulating web elements and page-specific methods.
  - **utils**: Utility classes such as `WebDriverUtils` and `ConfigReader`.

- **src/test/java**:
  - **testcases**: Contains test classes that implement specific test scenarios.
  - **testdata**: Stores test data files (e.g., Excel, CSV, Properties) for data-driven testing.
  - **testng.xml**: Test suite configuration file for TestNG.

## Executing Tests

### 1. Run Tests Locally

To run all tests locally, use:
```bash
mvn test
```

### 2. Run Specific Test Suite

To execute a specific TestNG suite, specify the XML suite file:
```bash
mvn test -DsuiteXmlFile=testng.xml
```

Set `browser` to `chrome`, `firefox`, etc., for different browser environments.

## Test Reports

Upon test execution, reports are generated in `/test-output`:

- **TestNG Report**: Standard TestNG report.
- **Custom HTML Report**: If integrated, a more detailed HTML report (like Extent Reports) is available for better insights.
