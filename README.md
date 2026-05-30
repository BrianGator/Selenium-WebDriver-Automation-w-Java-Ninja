# Selenium WebDriver Automation with Java - Ninja Edition

## Project Name
**Selenium WebDriver Automation Framework - Ninja Plus** - A comprehensive Java-based automation testing framework for web applications using Selenium WebDriver with advanced testing capabilities.

## Description
This project is an extensive learning and implementation resource for Selenium WebDriver automation using Java. It covers fundamental Java concepts through advanced automation testing patterns, including REST API automation, cross-browser testing, data-driven testing, and CI/CD integration.

**Written by Brian McCarthy**

---

## Table of Contents
- [Languages & Technologies](#languages--technologies)
- [Methodologies Used](#methodologies-used)
- [Core Functions & Components](#core-functions--components)
- [Project File Structure](#project-file-structure)
- [Key Features Implemented](#key-features-implemented)
- [Code Methodologies & Examples](#code-methodologies--examples)
- [REST API Automation Guide](#rest-api-automation-guide)
- [How to Use](#how-to-use)
- [All Testing Types with Descriptions](#all-testing-types-with-descriptions)
- [Dependencies](#dependencies)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)
- [Additional Resources](#additional-resources)

---

## Languages & Technologies

### Primary Language
- **Java** - 100% (Core language for all automation testing)
  - JDK 11 or higher
  - Object-Oriented Programming (OOP)
  - Exception Handling
  - Collections Framework
  - Streams & Lambdas

### Testing Frameworks & Libraries
- **Selenium WebDriver 4.x** - Web browser automation
- **TestNG 7.x** - Testing framework with advanced features
- **REST-Assured** - REST API testing
- **Log4j2** - Logging framework
- **Extent Reports** - HTML test reporting
- **Apache POI** - Excel file handling
- **Gson** - JSON serialization/deserialization
- **Maven 3.6+** - Build automation tool
- **Jenkins** - CI/CD integration

### IDE & Tools
- IntelliJ IDEA or Eclipse
- Git for version control
- Maven for dependency management

---

## Methodologies Used

### 1. **Page Object Model (POM)**
Separates UI elements from test logic, making tests maintainable and scalable.

### 2. **Data-Driven Testing**
Uses external data sources (Excel, CSV, DataProviders) to run tests with multiple datasets.

### 3. **Behavior-Driven Development (BDD)**
Tests written in business-readable format describing expected behaviors.

### 4. **Test-Driven Development (TDD)**
Writing tests before implementing features to ensure quality and design.

### 5. **Continuous Integration/Continuous Deployment (CI/CD)**
Automated test execution in Jenkins pipelines for every code commit.

### 6. **Cross-Browser Testing**
Testing application functionality across multiple browsers (Chrome, Firefox, Edge, Safari).

### 7. **Parallel Test Execution**
Running multiple tests simultaneously to reduce overall test execution time.

### 8. **Exception Handling & Custom Assertions**
Robust error handling and custom assertions for meaningful test failures.

### 9. **Logging Best Practices**
Comprehensive logging at different levels (INFO, DEBUG, ERROR) for test debugging.

### 10. **REST API Automation**
Testing backend services and APIs alongside UI automation for complete integration testing.

---

## Core Functions & Components

### WebDriver Management
- `WebDriverFactory` - Factory pattern for browser initialization
- `BrowserFactory` - Multi-browser support configuration
- `DriverManager` - Singleton pattern for driver management

### Page Object Model Classes
- `BasePage` - Base class for all page objects
- `LoginPage` - Example page object with element locators and methods
- `HomePage` - Dashboard and main application page
- `SearchPage` - Search functionality page object

### Test Base Classes
- `BaseTest` - Base test class with setup/teardown
- `DataProviderUtil` - Data provider configurations
- `TestListener` - TestNG listener for event handling

### Utility Classes
- `CommonUtilities` - Common helper methods
- `WaitUtil` - Explicit and implicit wait implementations
- `JavaScriptUtil` - JavaScript execution utilities
- `ExcelUtil` - Excel file handling
- `APIUtil` - REST API testing utilities
- `DatabaseUtil` - Database operations

### Reporting & Logging
- `ExtentReportManager` - Extent Reports configuration
- `Log4jConfig` - Log4j2 logging setup
- `TestReport` - Custom reporting utilities

### Configuration Management
- `config.properties` - Environment and browser configurations
- `log4j2.xml` - Logging configuration

---

## Project File Structure

```
Selenium-WebDriver-Automation-w-Java-Ninja/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com/
│   │   │   │   ├── automation/
│   │   │   │   │   ├── base/
│   │   │   │   │   │   ├── BaseTest.java           # Base test class with setup/teardown
│   │   │   │   │   │   ├── BasePage.java           # Base page object class
│   │   │   │   │   │   └── DriverManager.java      # WebDriver lifecycle management
│   │   │   │   │   │
│   │   │   │   │   ├── factory/
│   │   │   │   │   │   └── WebDriverFactory.java   # Browser factory implementation
│   │   │   │   │   │
│   │   │   │   │   ├── pages/
│   │   │   │   │   │   ├── LoginPage.java          # Login page object
│   │   │   │   │   │   ├── HomePage.java           # Home page object
│   │   │   │   │   │   └── SearchPage.java         # Search page object
│   │   │   │   │   │
│   │   │   │   │   ├── utils/
│   │   │   │   │   │   ├── CommonUtilities.java    # Common utilities
│   │   │   │   │   │   ├── WaitUtil.java           # Wait strategies
│   │   │   │   │   │   ├── JavaScriptUtil.java     # JavaScript execution
│   │   │   │   │   │   ├── ExcelUtil.java          # Excel handling
│   │   │   │   │   │   ├── APIUtil.java            # REST API utilities
│   │   │   │   │   │   └── DatabaseUtil.java       # Database operations
│   │   │   │   │   │
│   │   │   │   │   ├── config/
│   │   │   │   │   │   ├── PropertyFileReader.java # Config file reader
│   │   │   │   │   │   └── config.properties       # Configuration file
│   │   │   │   │   │
│   │   │   │   │   ├── listeners/
│   │   │   │   │   │   └── TestListener.java       # TestNG event listener
│   │   │   │   │   │
│   │   │   │   │   ├── report/
│   │   │   │   │   │   └── ExtentReportManager.java # Extent Reports manager
│   │   │   │   │   │
│   │   │   │   │   └── constants/
│   │   │   │   │       ├── Constants.java          # Application constants
│   │   │   │   │       └── BrowserType.java        # Browser enums
│   │   │   │   │
│   │   │   │   └── S01-S51/                        # Section-wise learning modules
│   │   │   │       ├── S01_JavaBasics/            # Java fundamentals
│   │   │   │       ├── S06_SeleniumSetup/         # Selenium setup
│   │   │   │       ├── S09_Locators/              # Element locators
│   │   │   │       └── ... (S10-S51 sections)
│   │   │
│   │   └── resources/
│   │       ├── config.properties                   # Test configuration
│   │       ├── log4j2.xml                          # Logging configuration
│   │       ├── testdata.xlsx                       # Test data file
│   │       └── application.properties              # App properties
│   │
│   └── test/
│       ├── java/
│       │   └── com/
│       │       └── automation/
│       │           ├── tests/
│       │           │   ├── LoginTests.java         # Login test suite
│       │           │   ├── SearchTests.java        # Search test suite
│       │           │   ├── APITests.java           # API automation tests
│       │           │   └── IntegrationTests.java   # Integration tests
│       │           │
│       │           ├── dataproviders/
│       │           │   ├── LoginDataProvider.java  # Login test data
│       │           │   └── APIDataProvider.java    # API test data
│       │           │
│       │           └── listeners/
│       │               └── TestListener.java       # Test event listener
│       │
│       └── resources/
│           ├── testng.xml                          # TestNG configuration
│           ├── testng-parallel.xml                 # Parallel execution config
│           └── test-data/
│               ├── login_data.xlsx                 # Login test data
│               └── api_test_data.json              # API test data
│
├── S01-S05/                                        # Java fundamentals and OOP concepts
├── S06-S08/                                        # Selenium WebDriver basics and setup
├── S09-S11/                                        # Element locator strategies
├── S12-S20/                                        # Web element interactions and advanced features
├── S21-S26/                                        # TestNG framework and annotations
├── S27-S29/                                        # TestNG parameters and data-driven testing
├── S30-S33/                                        # Reporting and logging infrastructure
├── S34-S37/                                        # Advanced automation patterns
├── S38-S44/                                        # Build management and CI/CD
├── S45-S51/                                        # Interview questions and advanced Java concepts
├── Tests/                                          # Comprehensive test suite
├── pom.xml                                         # Maven POM configuration
├── Jenkinsfile                                     # Jenkins CI/CD pipeline
├── .gitignore                                      # Git ignore file
├── LICENSE                                         # Apache License 2.0
└── README.md                                       # Project documentation

```

---

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
- ✅ REST API automation with REST-Assured
- ✅ Complete API testing guide with examples

---

## Code Methodologies & Examples

### 1. Page Object Model (POM) Implementation

#### Example: LoginPage.java
```java
public class LoginPage extends BasePage {
    
    // Element locators
    private By emailInput = By.id("email");
    private By passwordInput = By.id("password");
    private By loginButton = By.xpath("//button[@class='btn-login']");
    private By errorMessage = By.className("error-msg");
    
    public LoginPage(WebDriver driver) {
        super(driver);
    }
    
    // Page-specific methods
    public void enterEmail(String email) {
        sendKeys(emailInput, email);
    }
    
    public void enterPassword(String password) {
        sendKeys(passwordInput, password);
    }
    
    public HomePage clickLogin() {
        click(loginButton);
        return new HomePage(driver);
    }
    
    public String getErrorMessage() {
        return getText(errorMessage);
    }
    
    public LoginPage login(String email, String password) {
        enterEmail(email);
        enterPassword(password);
        clickLogin();
        return this;
    }
}
```

**How it works**: 
- Encapsulates all login-related elements and methods in one class
- Makes tests more readable and maintainable
- Reduces code duplication across test files
- Easy to update element locators in one place

---

### 2. Data-Driven Testing with TestNG DataProvider

#### Example: LoginTest.java
```java
public class LoginTest extends BaseTest {
    
    private LoginPage loginPage;
    
    @BeforeMethod
    public void setUp() {
        loginPage = new LoginPage(driver);
    }
    
    @DataProvider(name = "loginData")
    public Object[][] getLoginData() {
        return new Object[][] {
            { "user1@test.com", "password123", true },
            { "user2@test.com", "password456", true },
            { "invalid@test.com", "wrongpass", false },
            { "user3@test.com", "pass789", true }
        };
    }
    
    @Test(dataProvider = "loginData")
    public void testLoginWithMultipleCredentials(String email, String password, boolean expectedSuccess) {
        loginPage.login(email, password);
        
        if (expectedSuccess) {
            Assert.assertTrue(loginPage.isHomePageDisplayed(), "Login failed for: " + email);
        } else {
            Assert.assertTrue(loginPage.getErrorMessage().contains("Invalid"), "Error message not displayed");
        }
    }
}
```

**How it works**:
- `@DataProvider` method provides multiple test data sets
- Same test executes with different data each time
- Reduces code duplication for similar test scenarios
- Easy to add more test cases by updating the data array

---

### 3. Wait Strategies Implementation

#### Example: WaitUtil.java
```java
public class WaitUtil {
    
    private WebDriver driver;
    private WebDriverWait wait;
    private static final int DEFAULT_TIMEOUT = 10;
    
    public WaitUtil(WebDriver driver) {
        this.driver = driver;
        this.wait = new WebDriverWait(driver, Duration.ofSeconds(DEFAULT_TIMEOUT));
    }
    
    // Explicit Wait for element visibility
    public void waitForElementVisibility(By locator) {
        wait.until(ExpectedConditions.visibilityOfElementLocated(locator));
    }
    
    // Explicit Wait for element clickability
    public void waitForElementClickability(By locator) {
        wait.until(ExpectedConditions.elementToBeClickable(locator));
    }
    
    // Explicit Wait for element presence
    public void waitForElementPresence(By locator) {
        wait.until(ExpectedConditions.presenceOfElementLocated(locator));
    }
    
    // Custom wait for text to be present
    public void waitForText(By locator, String text) {
        wait.until(ExpectedConditions.textToBePresentInElementLocated(locator, text));
    }
    
    // Implicit wait
    public void setImplicitWait(int seconds) {
        driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(seconds));
    }
}
```

**How it works**:
- Explicit waits provide precise control over wait conditions
- Reduces `NoSuchElementException` and stale element exceptions
- More reliable than implicit waits
- Better performance as it waits only until condition is met

---

### 4. TestNG Annotations & Listeners

#### Example: TestListener.java
```java
public class TestListener implements ITestListener {
    
    private static final Logger logger = LoggerFactory.getLogger(TestListener.class);
    private ExtentTest test;
    
    @Override
    public void onTestStart(ITestResult result) {
        logger.info("Test Started: " + result.getMethod().getMethodName());
        test = ExtentReportManager.createTest(result.getMethod().getMethodName());
    }
    
    @Override
    public void onTestSuccess(ITestResult result) {
        logger.info("Test Passed: " + result.getMethod().getMethodName());
        test.pass("Test passed successfully");
    }
    
    @Override
    public void onTestFailure(ITestResult result) {
        logger.error("Test Failed: " + result.getMethod().getMethodName());
        test.fail(result.getThrowable());
        
        // Take screenshot on failure
        try {
            String screenshot = CommonUtilities.takeScreenshot(driver, result.getMethod().getMethodName());
            test.addScreenCaptureFromPath(screenshot);
        } catch (IOException e) {
            logger.error("Failed to capture screenshot: " + e.getMessage());
        }
    }
    
    @Override
    public void onTestSkipped(ITestResult result) {
        logger.warn("Test Skipped: " + result.getMethod().getMethodName());
        test.skip("Test skipped");
    }
}
```

**How it works**:
- Implements `ITestListener` interface from TestNG
- Automatically captures test lifecycle events
- Logs test execution details
- Captures screenshots on failures
- Updates Extent Reports with test results

---

### 5. Exception Handling & Custom Assertions

#### Example: Custom Assertions
```java
public class CustomAssertions {
    
    public static void assertElementDisplayed(WebElement element, String errorMessage) {
        try {
            Assert.assertTrue(element.isDisplayed(), errorMessage);
        } catch (NoSuchElementException e) {
            Assert.fail("Element not found: " + errorMessage);
        }
    }
    
    public static void assertTextPresent(String actualText, String expectedText, String errorMessage) {
        try {
            Assert.assertTrue(actualText.contains(expectedText), 
                errorMessage + "\nExpected: " + expectedText + "\nActual: " + actualText);
        } catch (Exception e) {
            Assert.fail("Text comparison failed: " + e.getMessage());
        }
    }
    
    public static void assertPageTitle(WebDriver driver, String expectedTitle) {
        String actualTitle = driver.getTitle();
        Assert.assertEquals(actualTitle, expectedTitle, 
            "Page title mismatch. Expected: " + expectedTitle + ", Actual: " + actualTitle);
    }
}
```

**How it works**:
- Wraps standard assertions with meaningful error messages
- Handles exceptions gracefully
- Provides detailed assertion failure information
- Makes test failures easier to debug

---

### 6. Logging Implementation with Log4j2

#### Example: log4j2.xml Configuration
```xml
<?xml version="1.0" encoding="UTF-8"?>
<Configuration>
    <Appenders>
        <Console name="Console" target="SYSTEM_OUT">
            <PatternLayout pattern="%d{yyyy-MM-dd HH:mm:ss} [%t] %-5p %c{1} - %m%n"/>
        </Console>
        
        <RollingFile name="File" fileName="logs/automation.log"
            filePattern="logs/automation-%d{yyyy-MM-dd}-%i.log.gz">
            <PatternLayout pattern="%d{yyyy-MM-dd HH:mm:ss} [%t] %-5p %c{1} - %m%n"/>
            <Policies>
                <TimeBasedTriggeringPolicy interval="1" modulate="true"/>
                <SizeBasedTriggeringPolicy size="100MB"/>
            </Policies>
        </RollingFile>
    </Appenders>
    
    <Loggers>
        <Logger name="com.automation" level="INFO"/>
        <Root level="INFO">
            <AppenderRef ref="Console"/>
            <AppenderRef ref="File"/>
        </Root>
    </Loggers>
</Configuration>
```

**Usage in code**:
```java
private static final Logger logger = LoggerFactory.getLogger(LoginTest.class);

public void testLogin() {
    logger.info("Starting login test");
    logger.debug("Entering email: user@test.com");
    logger.error("Login failed: " + exception.getMessage());
}
```

**How it works**:
- Logs are written to both console and file
- Rolling files prevent log file size explosion
- Different log levels (INFO, DEBUG, ERROR) for detailed tracking
- Helps in debugging and troubleshooting

---

## REST API Automation Guide

### Overview
REST API automation is essential for modern testing as it provides:
- Backend validation independent of UI
- Performance testing capabilities
- Data integrity verification
- Faster test execution

### 1. REST-Assured Setup

#### Dependencies in pom.xml
```xml
<dependency>
    <groupId>io.rest-assured</groupId>
    <artifactId>rest-assured</artifactId>
    <version>5.3.0</version>
</dependency>

<dependency>
    <groupId>com.google.code.gson</groupId>
    <artifactId>gson</artifactId>
    <version>2.10.1</version>
</dependency>
```

---

### 2. APIUtil Class - Utility Methods

#### Example: APIUtil.java
```java
public class APIUtil {
    
    private static final Logger logger = LoggerFactory.getLogger(APIUtil.class);
    private static final String BASE_URL = "https://api.example.com";
    
    // GET request
    public static Response getRequest(String endpoint) {
        logger.info("Making GET request to: " + BASE_URL + endpoint);
        return given()
            .contentType(ContentType.JSON)
            .when()
            .get(BASE_URL + endpoint)
            .then()
            .log().all()
            .extract()
            .response();
    }
    
    // POST request with request body
    public static Response postRequest(String endpoint, Object body) {
        logger.info("Making POST request to: " + BASE_URL + endpoint);
        return given()
            .contentType(ContentType.JSON)
            .body(body)
            .when()
            .post(BASE_URL + endpoint)
            .then()
            .log().all()
            .extract()
            .response();
    }
    
    // POST request with JSON string
    public static Response postRequestWithJson(String endpoint, String jsonBody) {
        logger.info("Making POST request with JSON to: " + BASE_URL + endpoint);
        return given()
            .contentType(ContentType.JSON)
            .body(jsonBody)
            .when()
            .post(BASE_URL + endpoint)
            .then()
            .log().all()
            .extract()
            .response();
    }
    
    // PUT request
    public static Response putRequest(String endpoint, Object body) {
        logger.info("Making PUT request to: " + BASE_URL + endpoint);
        return given()
            .contentType(ContentType.JSON)
            .body(body)
            .when()
            .put(BASE_URL + endpoint)
            .then()
            .log().all()
            .extract()
            .response();
    }
    
    // DELETE request
    public static Response deleteRequest(String endpoint) {
        logger.info("Making DELETE request to: " + BASE_URL + endpoint);
        return given()
            .contentType(ContentType.JSON)
            .when()
            .delete(BASE_URL + endpoint)
            .then()
            .log().all()
            .extract()
            .response();
    }
    
    // Request with headers
    public static Response getRequestWithHeaders(String endpoint, Map<String, String> headers) {
        logger.info("Making GET request with headers to: " + BASE_URL + endpoint);
        return given()
            .contentType(ContentType.JSON)
            .headers(headers)
            .when()
            .get(BASE_URL + endpoint)
            .then()
            .log().all()
            .extract()
            .response();
    }
    
    // Request with authentication
    public static Response getRequestWithAuth(String endpoint, String username, String password) {
        logger.info("Making authenticated GET request to: " + BASE_URL + endpoint);
        return given()
            .contentType(ContentType.JSON)
            .auth().basic(username, password)
            .when()
            .get(BASE_URL + endpoint)
            .then()
            .log().all()
            .extract()
            .response();
    }
    
    // Request with Bearer token
    public static Response getRequestWithToken(String endpoint, String token) {
        logger.info("Making GET request with token to: " + BASE_URL + endpoint);
        return given()
            .contentType(ContentType.JSON)
            .header("Authorization", "Bearer " + token)
            .when()
            .get(BASE_URL + endpoint)
            .then()
            .log().all()
            .extract()
            .response();
    }
}
```

---

### 3. Complete API Test Examples

#### Example 1: Basic GET Request Test
```java
public class UserAPITest {
    
    private static final Logger logger = LoggerFactory.getLogger(UserAPITest.class);
    private APIUtil apiUtil = new APIUtil();
    
    @Test
    public void testGetAllUsers() {
        logger.info("Test: Get all users");
        
        Response response = APIUtil.getRequest("/users");
        
        // Assertions
        Assert.assertEquals(response.getStatusCode(), 200, "Status code should be 200");
        Assert.assertTrue(response.getContentType().contains("application/json"), "Content type should be JSON");
        
        // Extract and verify response body
        List<Integer> userIds = response.jsonPath().getList("id");
        Assert.assertTrue(userIds.size() > 0, "User list should not be empty");
        
        logger.info("Test passed - Retrieved " + userIds.size() + " users");
    }
    
    @Test
    public void testGetUserById() {
        logger.info("Test: Get user by ID");
        
        int userId = 1;
        Response response = APIUtil.getRequest("/users/" + userId);
        
        // Assertions
        Assert.assertEquals(response.getStatusCode(), 200);
        Assert.assertEquals(response.jsonPath().getInt("id"), userId);
        Assert.assertNotNull(response.jsonPath().getString("name"));
        
        logger.info("Test passed - Retrieved user: " + response.jsonPath().getString("name"));
    }
}
```

**Explanation**:
- `getRequest()` makes a GET request and returns Response object
- `getStatusCode()` retrieves HTTP status code
- `jsonPath()` allows XPath-like syntax to extract JSON values
- `Assert` statements validate expected results

---

#### Example 2: POST Request with Request Body
```java
public class PostCreationAPITest {
    
    @Test
    public void testCreateNewPost() {
        logger.info("Test: Create new post");
        
        // Create request body
        String requestBody = "{\n" +
            "  \"title\": \"Test Post\",\n" +
            "  \"body\": \"This is a test post\",\n" +
            "  \"userId\": 1\n" +
            "}";
        
        Response response = APIUtil.postRequestWithJson("/posts", requestBody);
        
        // Assertions
        Assert.assertEquals(response.getStatusCode(), 201, "Status code should be 201 (Created)");
        Assert.assertNotNull(response.jsonPath().getInt("id"), "Post ID should not be null");
        Assert.assertEquals(response.jsonPath().getString("title"), "Test Post");
        
        int postId = response.jsonPath().getInt("id");
        logger.info("Test passed - Post created with ID: " + postId);
    }
    
    @Test
    public void testCreatePostWithObject() {
        logger.info("Test: Create post using object");
        
        // Create object using POJO
        PostData post = new PostData();
        post.setTitle("New Post");
        post.setBody("Post content");
        post.setUserId(1);
        
        Response response = APIUtil.postRequest("/posts", post);
        
        Assert.assertEquals(response.getStatusCode(), 201);
        Assert.assertNotNull(response.jsonPath().getInt("id"));
        
        logger.info("Test passed - Post created successfully");
    }
}
```

**PostData POJO Class**:
```java
public class PostData {
    private String title;
    private String body;
    private int userId;
    
    // Getters and Setters
    public String getTitle() { return title; }
    public void setTitle(String title) { this.title = title; }
    
    public String getBody() { return body; }
    public void setBody(String body) { this.body = body; }
    
    public int getUserId() { return userId; }
    public void setUserId(int userId) { this.userId = userId; }
}
```

---

#### Example 3: PUT Request with Update
```java
public class UpdateAPITest {
    
    @Test
    public void testUpdatePost() {
        logger.info("Test: Update post");
        
        int postId = 1;
        String updateBody = "{\n" +
            "  \"id\": " + postId + ",\n" +
            "  \"title\": \"Updated Title\",\n" +
            "  \"body\": \"Updated content\",\n" +
            "  \"userId\": 1\n" +
            "}";
        
        Response response = APIUtil.putRequest("/posts/" + postId, updateBody);
        
        // Assertions
        Assert.assertEquals(response.getStatusCode(), 200, "Status code should be 200");
        Assert.assertEquals(response.jsonPath().getString("title"), "Updated Title");
        
        logger.info("Test passed - Post updated successfully");
    }
}
```

---

#### Example 4: DELETE Request
```java
public class DeleteAPITest {
    
    @Test
    public void testDeletePost() {
        logger.info("Test: Delete post");
        
        int postId = 1;
        Response response = APIUtil.deleteRequest("/posts/" + postId);
        
        // Assertions - DELETE typically returns 200 or 204
        Assert.assertTrue(response.getStatusCode() == 200 || response.getStatusCode() == 204,
            "Status code should be 200 or 204");
        
        logger.info("Test passed - Post deleted successfully");
    }
}
```

---

#### Example 5: API Testing with Authentication
```java
public class AuthenticatedAPITest {
    
    @Test
    public void testAuthenticatedRequest() {
        logger.info("Test: Authenticated API request");
        
        String username = "testuser";
        String password = "testpass123";
        
        Response response = APIUtil.getRequestWithAuth("/protected/data", username, password);
        
        Assert.assertEquals(response.getStatusCode(), 200);
        Assert.assertNotNull(response.jsonPath().getString("data"));
        
        logger.info("Test passed - Authenticated request successful");
    }
    
    @Test
    public void testTokenBasedAuth() {
        logger.info("Test: Token-based API request");
        
        // First, get the token
        String loginBody = "{\"email\": \"user@test.com\", \"password\": \"pass123\"}";
        Response loginResponse = APIUtil.postRequestWithJson("/auth/login", loginBody);
        
        Assert.assertEquals(loginResponse.getStatusCode(), 200);
        String token = loginResponse.jsonPath().getString("token");
        
        // Use token for subsequent requests
        Response dataResponse = APIUtil.getRequestWithToken("/protected/data", token);
        
        Assert.assertEquals(dataResponse.getStatusCode(), 200);
        logger.info("Test passed - Token-based authentication successful");
    }
}
```

---

#### Example 6: Data-Driven API Testing
```java
public class DataDrivenAPITest extends BaseTest {
    
    @DataProvider(name = "apiTestData")
    public Object[][] getAPITestData() {
        return new Object[][] {
            { 1, "POST", "New Title", "New Body" },
            { 2, "POST", "Another Title", "Another Body" },
            { 3, "PUT", "Updated Title", "Updated Body" }
        };
    }
    
    @Test(dataProvider = "apiTestData")
    public void testAPIWithMultipleData(int id, String method, String title, String body) {
        logger.info("Test: API with data - ID: " + id + ", Method: " + method);
        
        String requestBody = "{\n" +
            "  \"title\": \"" + title + "\",\n" +
            "  \"body\": \"" + body + "\"\n" +
            "}";
        
        Response response;
        
        if ("POST".equals(method)) {
            response = APIUtil.postRequestWithJson("/posts", requestBody);
            Assert.assertEquals(response.getStatusCode(), 201);
        } else if ("PUT".equals(method)) {
            response = APIUtil.putRequest("/posts/" + id, requestBody);
            Assert.assertEquals(response.getStatusCode(), 200);
        }
        
        logger.info("Test passed for ID: " + id);
    }
}
```

---

#### Example 7: Response Validation & Assertion
```java
public class ResponseValidationTest {
    
    @Test
    public void testResponseValidation() {
        logger.info("Test: Response validation");
        
        Response response = APIUtil.getRequest("/users/1");
        
        // Validate status code
        response.then().statusCode(200);
        
        // Validate response body contains expected fields
        response.then()
            .body("id", notNullValue())
            .body("name", equalTo("John Doe"))
            .body("email", containsString("@"));
        
        // Validate headers
        response.then()
            .header("Content-Type", containsString("application/json"));
        
        // Validate response time
        response.then()
            .time(lessThan(2000L)); // Should respond in less than 2 seconds
        
        logger.info("Test passed - Response validation successful");
    }
    
    @Test
    public void testMultipleFieldValidation() {
        logger.info("Test: Multiple field validation");
        
        Response response = APIUtil.getRequest("/posts/1");
        
        response.then()
            .statusCode(200)
            .body("id", equalTo(1))
            .body("userId", equalTo(1))
            .body("title", notNullValue())
            .body("body", notNullValue());
        
        logger.info("Test passed - All fields validated");
    }
}
```

---

### 4. REST API Best Practices & Tips

#### Tip 1: Centralize Base URL Configuration
```java
// In config.properties
api.base.url=https://api.example.com
api.timeout=5000

// In code
String baseUrl = PropertyFileReader.getProperty("api.base.url");
int timeout = Integer.parseInt(PropertyFileReader.getProperty("api.timeout"));
```

#### Tip 2: Create Reusable Request Models
```java
public class APIRequest {
    private String endpoint;
    private String method;
    private Object body;
    private Map<String, String> headers;
    
    // Builder pattern
    public static APIRequest builder() {
        return new APIRequest();
    }
    
    public APIRequest withEndpoint(String endpoint) {
        this.endpoint = endpoint;
        return this;
    }
    
    public APIRequest withMethod(String method) {
        this.method = method;
        return this;
    }
    
    public APIRequest withBody(Object body) {
        this.body = body;
        return this;
    }
    
    public APIRequest withHeaders(Map<String, String> headers) {
        this.headers = headers;
        return this;
    }
}

// Usage
Response response = APIUtil.executeRequest(
    APIRequest.builder()
        .withEndpoint("/users")
        .withMethod("GET")
        .withHeaders(headersMap)
        .build()
);
```

#### Tip 3: Handle Different Response Types
```java
@Test
public void testDifferentResponseTypes() {
    // JSON Response
    Response jsonResponse = APIUtil.getRequest("/users/1");
    String name = jsonResponse.jsonPath().getString("name");
    
    // XML Response
    Response xmlResponse = APIUtil.getRequest("/data");
    String xmlValue = xmlResponse.xmlPath().getString("root.element");
    
    // Plain Text Response
    Response textResponse = APIUtil.getRequest("/text-data");
    String textContent = textResponse.asString();
}
```

#### Tip 4: Implement Retry Logic for API Tests
```java
public class APIRetryUtil {
    
    private static final int MAX_RETRIES = 3;
    private static final int RETRY_DELAY = 1000; // milliseconds
    
    public static Response executeWithRetry(Callable<Response> request) throws Exception {
        int attempts = 0;
        Exception lastException = null;
        
        while (attempts < MAX_RETRIES) {
            try {
                return request.call();
            } catch (Exception e) {
                lastException = e;
                attempts++;
                if (attempts < MAX_RETRIES) {
                    Thread.sleep(RETRY_DELAY);
                }
            }
        }
        
        throw lastException;
    }
    
    // Usage
    @Test
    public void testWithRetry() throws Exception {
        Response response = APIRetryUtil.executeWithRetry(() -> 
            APIUtil.getRequest("/unstable-endpoint")
        );
    }
}
```

#### Tip 5: Mock API Responses for Testing
```java
// Using WireMock or similar tools
@Test
public void testWithMockedAPI() {
    // Mock endpoint response
    WireMock.stubFor(get(urlEqualTo("/users/1"))
        .willReturn(aResponse()
            .withStatus(200)
            .withBody("{\"id\": 1, \"name\": \"John\"}")
            .withHeader("Content-Type", "application/json")));
    
    Response response = APIUtil.getRequest("/users/1");
    Assert.assertEquals(response.getStatusCode(), 200);
}
```

#### Tip 6: Extract & Reuse Response Values
```java
@Test
public void testExtractAndReuse() {
    // Create post
    Response createResponse = APIUtil.postRequest("/posts", postData);
    int postId = createResponse.jsonPath().getInt("id");
    
    // Update post using extracted ID
    String updateBody = "{\"title\": \"Updated\"}";
    Response updateResponse = APIUtil.putRequest("/posts/" + postId, updateBody);
    Assert.assertEquals(updateResponse.getStatusCode(), 200);
    
    // Delete post using extracted ID
    Response deleteResponse = APIUtil.deleteRequest("/posts/" + postId);
    Assert.assertEquals(deleteResponse.getStatusCode(), 200);
}
```

#### Tip 7: Performance Testing with APIs
```java
@Test
public void testAPIPerformance() {
    long startTime = System.currentTimeMillis();
    
    Response response = APIUtil.getRequest("/users");
    
    long endTime = System.currentTimeMillis();
    long duration = endTime - startTime;
    
    Assert.assertTrue(duration < 2000, "API response should be under 2 seconds. Actual: " + duration + "ms");
    logger.info("API response time: " + duration + "ms");
}
```

#### Tip 8: API Test Data Management
```java
public class APITestDataManager {
    
    // Create test data via API
    public static int createTestUser(UserData userData) {
        Response response = APIUtil.postRequest("/users", userData);
        return response.jsonPath().getInt("id");
    }
    
    // Delete test data via API
    public static void deleteTestUser(int userId) {
        APIUtil.deleteRequest("/users/" + userId);
    }
    
    // Setup: Create test data
    @BeforeMethod
    public void setup() {
        testUserId = APITestDataManager.createTestUser(testUserData);
    }
    
    // Teardown: Clean test data
    @AfterMethod
    public void cleanup() {
        APITestDataManager.deleteTestUser(testUserId);
    }
}
```

---

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

# Run API tests only
mvn test -Dtest=*APITest

# Run with detailed logging
mvn test -X
```

---

## All Testing Types with Descriptions

### 1. **Unit Testing**
- **Description**: Tests individual components/methods in isolation
- **Tools**: JUnit, TestNG assertions
- **Use Case**: Validating utility functions, helper methods
- **Example**: Testing string manipulation, calculations
- **Sample Code**:
```java
@Test
public void testStringUtility() {
    String result = StringUtil.capitalize("hello");
    Assert.assertEquals(result, "Hello");
}
```

### 2. **Functional Testing**
- **Description**: Tests complete workflows and business functions
- **Tools**: Selenium WebDriver, TestNG
- **Use Case**: Login flows, form submissions, searches
- **Example**: End-to-end user journeys
- **Sample Code**:
```java
@Test
public void testLoginWorkflow() {
    loginPage.login("user@test.com", "password123");
    Assert.assertTrue(homePage.isDisplayed());
}
```

### 3. **Smoke Testing**
- **Description**: Quick tests verifying basic functionality
- **Tools**: TestNG with @Test annotation
- **Use Case**: Pre-deployment validation
- **Example**: Application startup, main page loads
- **Sample Code**:
```java
@Test(groups = "smoke")
public void testApplicationStartup() {
    driver.navigate().to("https://www.example.com");
    Assert.assertTrue(driver.getTitle().contains("Example"));
}
```

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

---

## Dependencies
- **Selenium WebDriver**: Web automation framework
- **TestNG**: Testing framework with advanced features
- **REST-Assured**: REST API testing library
- **Log4j2**: Logging framework
- **Extent Reports**: Advanced HTML reporting
- **Gson**: JSON processing
- **Apache POI**: Excel file handling
- **Maven**: Build tool

---

## Documentation
- Extensive inline code comments
- Javadoc documentation for all classes
- Example test cases in each section
- Best practices and design patterns
- Complete REST API automation guide with real-world examples

---

## Contributing
1. Follow existing code structure
2. Add tests for new features
3. Update documentation
4. Submit pull requests with clear descriptions

---

## License
This project is licensed under the Apache License 2.0. See LICENSE file for details.

---

## Author
**Written by Brian McCarthy**

Created for comprehensive Selenium WebDriver automation learning and reference, with emphasis on modern testing practices, REST API automation, and CI/CD integration.

---

## Additional Resources
- [Selenium Official Documentation](https://www.selenium.dev/documentation/)
- [TestNG Documentation](https://testng.org/doc/)
- [REST-Assured GitHub](https://github.com/rest-assured/rest-assured)
- [Java Documentation](https://docs.oracle.com/en/java/)
- [Log4j2 Documentation](https://logging.apache.org/log4j/2.x/)
- [Maven Official Documentation](https://maven.apache.org/guides/)
