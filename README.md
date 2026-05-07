# Selenium WebDriver Automation with Java - Ninja Edition

## Project Name
**Selenium WebDriver Automation Framework - Ninja Plus** - A comprehensive Java-based automation testing framework for web applications using Selenium WebDriver with advanced testing capabilities.

## Description
This project is an extensive learning and implementation resource for Selenium WebDriver automation using Java. It covers fundamental Java concepts through advanced automation testing patterns, including framework design, TestNG integration, reporting, data-driven testing, and CI/CD integration.

## Key Features Implemented
- ✅ Complete Selenium WebDriver setup and configuration
- ✅ Advanced element locator strategies (ID, Class, XPath, CSS Selectors)
- ✅ Browser compatibility testing (Chrome, Firefox, Edge, Safari)
- ✅ Explicit and Implicit wait handling
- ✅ Actions Class for advanced user interactions
- ✅ Window and iFrame switching
- ✅ JavaScript execution
- ✅ TestNG framework integration with annotations
- ✅ Data-driven testing with DataProviders
- ✅ Logging with Log4j2
- ✅ Extent Reports for advanced HTML reporting
- ✅ Page Object Model (POM) pattern implementation
- ✅ Parallel test execution
- ✅ Cross-browser testing with Selenium Grid
- ✅ Maven build management
- ✅ Jenkins CI/CD integration
- ✅ Database testing capabilities
- ✅ File upload and Windows authentication handling
- ✅ Event listener implementation
- ✅ Exception handling and custom assertions

## Project Structure
```
Selenium-WebDriver-Automation-w-Java-Ninja/
├── S01-S05/               # Java fundamentals and OOP concepts
├── S06-S08/               # Selenium WebDriver basics and setup
├── S09-S11/               # Element locator strategies
├── S12-S20/               # Web element interactions and advanced features
├── S21-S26/               # TestNG framework and annotations
├── S27-S29/               # TestNG parameters and data-driven testing
├── S30-S33/               # Reporting and logging infrastructure
├── S34-S37/               # Advanced automation patterns
├── S38-S44/               # Build management and CI/CD
├── S45-S51/               # Interview questions and advanced Java concepts
├── Tests/                 # Comprehensive test suite
├── pom.xml               # Maven configuration
└── README.md             # Project documentation
```

## Tasks
- Learn Java fundamentals through practical examples
- Understand OOP concepts applied to automation
- Master Selenium WebDriver API
- Implement Page Object Model pattern
- Create data-driven tests with TestNG
- Generate professional test reports
- Setup CI/CD pipelines with Jenkins
- Perform cross-browser testing
- Execute database testing
- Handle file uploads and authentication

## How to Use

### Prerequisites
- Java JDK 11 or higher
- Maven 3.6+
- Selenium WebDriver 4.x
- TestNG 7.x
- IDE: IntelliJ IDEA or Eclipse

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/BrianGator/Selenium-WebDriver-Automation-w-Java-Ninja.git
   cd Selenium-WebDriver-Automation-w-Java-Ninja
   ```

2. Install dependencies:
   ```bash
   mvn clean install
   ```

3. Run all tests:
   ```bash
   mvn test
   ```

4. Run specific test class:
   ```bash
   mvn test -Dtest=YourTestClassName
   ```

5. Run with specific browser:
   ```bash
   mvn test -Dbrowser=firefox
   ```

6. Generate Extent Reports:
   ```bash
   mvn test -DgenerateReport=true
   ```

### Configuration
- Update `config.properties` with your test environment details
- Configure browser options in `WebDriverFactory.java`
- Set logging levels in `log4j2.xml`

### Running Tests
```bash
# Run all tests
mvn clean test

# Run tests in parallel
mvn test -DthreadCount=3

# Run specific suite
mvn test -DsuiteXmlFile=testng.xml

# Run with specific group
mvn test -Dgroups=smoke
```

## All Testing Types with Descriptions

### 1. **Unit Testing**
- **Description**: Tests individual components/methods in isolation
- **Tools**: JUnit, TestNG assertions
- **Use Case**: Validating utility functions, helper methods
- **Example**: Testing string manipulation, calculations

### 2. **Functional Testing**
- **Description**: Tests complete workflows and business functions
- **Tools**: Selenium WebDriver, TestNG
- **Use Case**: Login flows, form submissions, searches
- **Example**: End-to-end user journeys

### 3. **Smoke Testing**
- **Description**: Quick tests verifying basic functionality
- **Tools**: TestNG with @Test annotation
- **Use Case**: Pre-deployment validation
- **Example**: Application startup, main page loads

### 4. **Regression Testing**
- **Description**: Tests to ensure new changes don't break existing features
- **Tools**: TestNG with multiple test cases
- **Use Case**: After bug fixes or feature additions
- **Example**: Full test suite execution

### 5. **Integration Testing**
- **Description**: Tests interaction between multiple components
- **Tools**: Selenium with multiple page objects
- **Use Case**: Testing API + UI integration
- **Example**: Database operations reflected in UI

### 6. **Data-Driven Testing**
- **Description**: Tests with multiple data sets
- **Tools**: TestNG DataProvider, Excel/CSV files
- **Use Case**: Testing same scenario with different inputs
- **Example**: Login with multiple user credentials

### 7. **Cross-Browser Testing**
- **Description**: Tests application on different browsers
- **Tools**: Selenium Grid, BrowserStack
- **Use Case**: Ensuring compatibility across browsers
- **Example**: Chrome, Firefox, Safari, Edge

### 8. **Performance Testing**
- **Description**: Tests application performance and load times
- **Tools**: JMeter, Selenium with timing assertions
- **Use Case**: Checking response times, throughput
- **Example**: Page load time validations

### 9. **API Testing**
- **Description**: Tests backend APIs and services
- **Tools**: REST-Assured, HttpClient
- **Use Case**: Validating API responses
- **Example**: Status codes, response validation

### 10. **Accessibility Testing**
- **Description**: Tests WCAG compliance and accessibility features
- **Tools**: Axe-core, WAVE
- **Use Case**: Ensuring application is accessible to all users
- **Example**: Screen reader compatibility

## Dependencies
- **Selenium WebDriver**: Web automation framework
- **TestNG**: Testing framework with advanced features
- **Log4j2**: Logging framework
- **Extent Reports**: Advanced HTML reporting
- **Gson**: JSON processing
- **Apache POI**: Excel file handling
- **Maven**: Build tool

## Documentation
- Extensive inline code comments
- Javadoc documentation for all classes
- Example test cases in each section
- Best practices and design patterns

## Contributing
1. Follow existing code structure
2. Add tests for new features
3. Update documentation
4. Submit pull requests with clear descriptions

## License
This project is licensed under the Apache License 2.0. See LICENSE file for details.

## Author
Created by Brian Gator for comprehensive Selenium WebDriver automation learning and reference.

## Additional Resources
- [Selenium Official Documentation](https://www.selenium.dev/documentation/)
- [TestNG Documentation](https://testng.org/doc/)
- [Java Documentation](https://docs.oracle.com/en/java/)
