# Selenium WebDriver Automation with Java - Ninja Showcase

A complete Selenium WebDriver automation guide and portfolio README using **Java**, **Selenium WebDriver 4**, **TestNG**, **Maven**, **Page Object Model**, **Page Factory**, **Log4j2**, **Extent Reports**, **Apache POI**, **REST Assured**, **Selenium Grid**, **Jenkins**, **GitHub**, **Cucumber BDD**, database validation, and framework design practices.

**Written by Brian McCarthy**

---

## Course Content Table of Contents

| Module # | Module Name | Module Details |
|---:|---|---|
| 1 | Selenium Introduction | Course outcome, why Selenium, Selenium WebDriver architecture, and how WebDriver communicates with browsers. |
| 2 | Setup and Installation | Java, Eclipse, Maven, Maven plugin setup, and system preparation for Selenium automation. |
| 3 | Java Data Types | Hello World, variables, default values, strings, string methods, arrays, and String vs StringBuilder concepts. |
| 4 | Classes and Methods | Java methods, return types, classes, object creation, and reusable code organization. |
| 5 | Getters, Setters, and Constructors | Encapsulation, `this` keyword, constructors, and Java object initialization. |
| 6 | In-Depth Java Review | Beginner Java reinforcement and interview-focused Java concepts. |
| 7 | Selenium WebDriver Setup | Selenium 4 Maven setup, first project creation, JavaDoc, and Selenium 4 syntax changes. |
| 8 | Browser Execution | Running tests on Chrome, Firefox, Edge, and Safari; Selenium Manager; driver setup. |
| 9 | Element Inspection | Chrome DevTools, Firefox DevTools, SelectorsHub, XPath generation, and disappearing elements. |
| 10 | Basic Locators | `id`, `name`, `xpath`, `linkText`, `partialLinkText`, `className`, and `tagName`. |
| 11 | CSS Selectors | CSS ID, class, multiple class, wildcard, child-node, and CSS locator strategies. |
| 12 | XPath Locators | Relative XPath, text, contains, starts-with, parent/sibling axes, and practical XPath design. |
| 13 | Web Elements | Click, type, clear, navigation, enabled/disabled state, radio buttons, checkboxes, dropdowns, lists, hidden elements. |
| 14 | Profiles and Options | Firefox profiles, ChromeOptions, browser extensions, and browser startup configuration. |
| 15 | Useful WebDriver Methods | `getText`, `getAttribute`, generic element methods, element presence, refactoring utilities. |
| 16 | Waits and Synchronization | Implicit waits, explicit waits, generic wait utilities, and wait-related interview questions. |
| 17 | Advanced Interactions | Calendars, autocomplete, dynamic dropdowns, additional examples, and screenshots. |
| 18 | JavaScript Execution | JavaScriptExecutor, window size, scroll into view, and JavaScript click. |
| 19 | Windows, Frames, and Alerts | Window switching, iframe switching, alert handling, and focus control. |
| 20 | Actions Class | Mouse hover, drag-and-drop, sliders, and pointer actions. |
| 21 | Keyboard Events | Keyboard simulation, key combinations, and Actions-based key events. |
| 22 | Selenium Exceptions | NoSuchElement, not-clickable, stale element, and element-not-interactable exceptions. |
| 23 | Automation Framework | Framework design, Page Object Model, object repository, Page Factory, and link validation. |
| 24 | Log4j2 Logging | Console logging, file logging, custom loggers, and test-case logging. |
| 25 | TestNG Setup | TestNG introduction, setup, plugin configuration, and JavaDoc. |
| 26 | TestNG Annotations and Asserts | `@Test`, hard asserts, soft asserts, method/class/suite/test annotations, and suites. |
| 27 | TestNG Advanced Features | Priorities, groups, dependent tests, disabled tests, timeouts, and preserving execution order. |
| 28 | TestNG Parameters and Parallel | XML parameters and parallel execution across tests, classes, and methods. |
| 29 | Parallel Practice | Practical multi-browser parallel execution with TestNG XML. |
| 30 | DataProviders | Running the same test with multiple data sets using TestNG `@DataProvider`. |
| 31 | ITestResult | Test status inspection and screenshots on failure. |
| 32 | TestNG Listeners | `IInvokedMethodListener`, `ITestListener`, `ISuiteListener`, and listener refactoring. |
| 33 | Reporter Logs and HTML Reports | TestNG reporter logs and generated HTML reports. |
| 34 | Extent Reports | Advanced HTML reporting, screenshots in reports, multiple tests, and POM reporting. |
| 35 | Data-Driven Testing | Excel setup, Apache POI, reading/writing Excel, and DataProviders with Excel data. |
| 36 | File Upload and Desktop Dialogs | File upload patterns using standard file inputs and OS-level dialog support where needed. |
| 37 | WebDriver Event Listener | Event-driven WebDriver logging and debugging concepts. |
| 38 | Selenium Grid | Hub/node concepts, RemoteWebDriver, cross-browser and cross-OS execution. |
| 39 | Maven Build Management | Maven features, repositories, POM, lifecycle, commands, profiles, and TestNG integration. |
| 40 | Git and GitHub | Local repositories, staging, commits, remotes, branches, conflict resolution, and cloning. |
| 41 | Jenkins CI | Jenkins setup, Java/Maven configuration, plugins, freestyle jobs, remote builds, scheduled builds. |
| 42 | Interview Preparation | Real-time Selenium WebDriver interview strategy and technical preparation. |
| 43 | Database Testing | JDBC, SQL database checks, MongoDB validation, and UI-to-database comparison. |
| 44 | Performance Timing | Single-user page timing, navigation timing, Stopwatch usage, and result logging. |
| 45 | Cucumber BDD | Gherkin, feature files, step definitions, runners, Cucumber options, and Selenium conversion. |
| 46 | Cloud Execution | Remote cloud browser execution concepts and provider configuration using safe environment variables. |
| 47 | Selenium IDE Basics | Selenium IDE, first scripts, generated WebDriver code, assert vs verify. |
| 48 | Conditional Statements and Loops | `if`, `switch`, `while`, `for`, and automation control-flow logic. |
| 49 | Static Keyword | Static methods, static fields, shared utilities, and framework design implications. |
| 50 | Java Practice Exercises | String manipulation, loops, reverse-string exercise, and interview problem solving. |
| 51 | Java OOP Concepts | Inheritance, access modifiers, abstract classes, interfaces, overloading, and overriding. |
| 52 | Exception Handling | Checked exceptions, runtime exceptions, properties files, and robust error handling. |
| 53 | Java Collections | ArrayList, LinkedList, Sets, Maps, and using collections in test data and framework code. |
| 54 | Conclusion | Next steps and final Selenium automation project guidance. |
| 55 | Legacy Log4j Reference | Older Log4j concepts retained for historical reference. |
| 56 | Legacy TestNG Reference | Older TestNG lectures retained for historical comparison and migration awareness. |

---

## Selenium Java Tutorial Guide with Code Samples and Expected Results

### 1. Selenium WebDriver Basics

Selenium WebDriver drives a real browser and performs the same actions a user performs: opening pages, clicking links, typing text, selecting dropdown values, and validating results.

```java
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class OpenBrowserDemo {
    public static void main(String[] args) {
        WebDriver driver = new ChromeDriver();
        driver.get("https://example.com");
        System.out.println(driver.getTitle());
        driver.quit();
    }
}
```

**Expected Result:** Chrome opens, navigates to Example Domain, prints the page title, and closes cleanly.

---

### 2. Java Fundamentals for Selenium

Java fundamentals support every Selenium framework class: strings for URLs and locators, arrays/lists for element collections, booleans for assertions, and classes for page objects.

```java
String browser = "chrome";
int timeoutSeconds = 10;
boolean runHeadless = false;
String[] supportedBrowsers = {"chrome", "firefox", "edge"};

System.out.println(browser);
System.out.println(timeoutSeconds);
System.out.println(runHeadless);
System.out.println(supportedBrowsers.length);
```

**Expected Result:** Java prints browser settings and confirms there are three supported browsers.

---

### 3. Locator Information and Best Practices

Locators identify elements on the page. Strong locators make tests reliable. Weak locators create flaky tests.

| Locator | Best Use | Example |
|---|---|---|
| `id` | Unique input/button IDs | `By.id("email")` |
| `name` | Form fields | `By.name("password")` |
| CSS selector | Fast, flexible element matching | `By.cssSelector("button[type='submit']")` |
| XPath | Complex relationships | `By.xpath("//label[text()='Email']/following::input[1]")` |
| linkText | Exact link text | `By.linkText("Forgot Password")` |
| partialLinkText | Partial link text | `By.partialLinkText("Forgot")` |
| className | Single class only | `By.className("primary")` |
| tagName | Collections such as links | `By.tagName("a")` |

```java
WebElement email = driver.findElement(By.id("email"));
WebElement password = driver.findElement(By.name("password"));
WebElement login = driver.findElement(By.cssSelector("button[type='submit']"));
WebElement forgot = driver.findElement(By.linkText("Forgot Password"));
```

**Expected Result:** Selenium locates each element and makes it available for actions or validation.

---

### 4. CSS and XPath Advanced Locators

CSS is usually shorter and fast. XPath is useful for text matching, parent/child traversal, and sibling relationships.

```java
By cssByClass = By.cssSelector("button.primary.submit");
By cssChild = By.cssSelector("form#loginForm input[name='email']");
By xpathByText = By.xpath("//button[text()='Login']");
By xpathContains = By.xpath("//button[contains(text(),'Log')]");
By xpathSibling = By.xpath("//td[text()='Brian']/following-sibling::td/button");
```

**Expected Result:** The framework can locate elements through CSS and XPath strategies depending on DOM structure.

---

### 5. Working with Web Elements

WebElement methods are used for interaction and validation.

```java
WebElement email = driver.findElement(By.id("email"));
email.clear();
email.sendKeys("demo@example.com");

WebElement checkbox = driver.findElement(By.id("terms"));
if (!checkbox.isSelected()) {
    checkbox.click();
}

System.out.println(email.getAttribute("value"));
System.out.println(checkbox.isSelected());
```

**Expected Result:** The email field is filled, the checkbox is selected, and values are printed for validation.

---

### 6. Dropdowns, Radio Buttons, and Lists

Selenium's `Select` class handles standard HTML dropdowns.

```java
Select country = new Select(driver.findElement(By.id("country")));
country.selectByVisibleText("United States");

List<WebElement> options = country.getOptions();
System.out.println(options.size());
```

**Expected Result:** United States is selected and the number of dropdown options is printed.

---

### 7. Waits and Synchronization

Explicit waits are preferred for dynamic pages because they wait for a specific condition.

```java
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
WebElement button = wait.until(ExpectedConditions.elementToBeClickable(By.id("login-submit")));
button.click();
```

**Expected Result:** Selenium waits until the button is clickable before clicking, reducing timing failures.

---

### 8. Login Tests

Login coverage should include valid login, invalid login, required field validation, logout, session behavior, and role-based redirects.

```java
@Test
public void validLoginTest() {
    driver.get("https://example.com/login");
    driver.findElement(By.id("email")).sendKeys("demo@example.com");
    driver.findElement(By.id("password")).sendKeys("DemoPassword123");
    driver.findElement(By.id("login-submit")).click();

    WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
    WebElement dashboard = wait.until(ExpectedConditions.visibilityOfElementLocated(By.id("dashboard")));
    Assert.assertTrue(dashboard.isDisplayed());
}

@Test
public void invalidLoginShowsErrorTest() {
    driver.get("https://example.com/login");
    driver.findElement(By.id("email")).sendKeys("invalid@example.com");
    driver.findElement(By.id("password")).sendKeys("WrongPassword");
    driver.findElement(By.id("login-submit")).click();

    String error = driver.findElement(By.cssSelector(".error-message")).getText();
    Assert.assertEquals(error, "Invalid username or password");
}
```

**Expected Result:** Valid login reaches the dashboard. Invalid login displays a useful error message.

---

### 9. API Tests with REST Assured

A complete automation portfolio should include UI tests and API tests. API tests validate backend behavior directly and can also prepare data for UI tests.

```java
import io.restassured.RestAssured;
import org.testng.annotations.Test;

public class ApiTests {
    @Test
    public void getProductsApiTest() {
        RestAssured
            .given()
                .baseUri("https://api.example.com")
            .when()
                .get("/products")
            .then()
                .statusCode(200);
    }
}
```

**Expected Result:** The API endpoint returns HTTP 200. The test fails if the endpoint is unavailable or returns the wrong status.

---

### 10. JavaScript Execution

JavaScriptExecutor can scroll or click when normal WebDriver actions are blocked by layout or overlays.

```java
JavascriptExecutor js = (JavascriptExecutor) driver;
WebElement element = driver.findElement(By.id("submit"));
js.executeScript("arguments[0].scrollIntoView(true);", element);
js.executeScript("arguments[0].click();", element);
```

**Expected Result:** Selenium scrolls to the element and performs a JavaScript click.

---

### 11. Windows, IFrames, and Alerts

```java
String parent = driver.getWindowHandle();
for (String handle : driver.getWindowHandles()) {
    if (!handle.equals(parent)) {
        driver.switchTo().window(handle);
        break;
    }
}

driver.switchTo().frame("payment-frame");
driver.findElement(By.id("cardNumber")).sendKeys("4111111111111111");
driver.switchTo().defaultContent();

Alert alert = driver.switchTo().alert();
alert.accept();
```

**Expected Result:** Selenium changes browser focus to a new window, works inside an iframe, returns to the main page, and handles an alert.

---

### 12. Actions Class and Keyboard Events

```java
Actions actions = new Actions(driver);
WebElement menu = driver.findElement(By.id("menu"));
WebElement submenu = driver.findElement(By.id("submenu"));
actions.moveToElement(menu).click(submenu).perform();

actions.keyDown(Keys.CONTROL).sendKeys("a").keyUp(Keys.CONTROL).perform();
```

**Expected Result:** Selenium performs mouse hover, submenu click, and keyboard shortcut actions.

---

### 13. Selenium Exceptions

Common exceptions usually point to timing, locator, frame, visibility, or DOM-refresh problems.

```java
try {
    WebElement save = new WebDriverWait(driver, Duration.ofSeconds(10))
            .until(ExpectedConditions.elementToBeClickable(By.id("save")));
    save.click();
} catch (TimeoutException e) {
    System.out.println("Save button was not clickable within 10 seconds.");
}
```

**Expected Result:** The test gives a clear diagnostic message instead of an unclear failure.

---

### 14. TestNG, DataProviders, and Parallel Execution

```java
@DataProvider(name = "loginData")
public Object[][] loginData() {
    return new Object[][] {
        {"valid@example.com", "Password123", true},
        {"invalid@example.com", "WrongPassword", false}
    };
}

@Test(dataProvider = "loginData")
public void loginDataTest(String email, String password, boolean expectedSuccess) {
    System.out.println(email + " should pass: " + expectedSuccess);
}
```

```xml
<suite name="Parallel Suite" parallel="tests" thread-count="2">
    <test name="Chrome Tests">
        <parameter name="browser" value="chrome"/>
        <classes><class name="tests.LoginTest"/></classes>
    </test>
</suite>
```

**Expected Result:** TestNG runs the test once per data row and can run tests in parallel through XML configuration.

---

### 15. Screenshots, Logging, and Reports

```java
public void captureScreenshot(String testName) throws IOException {
    File src = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
    File dest = new File("screenshots/" + testName + ".png");
    FileUtils.copyFile(src, dest);
}
```

```java
private static final Logger log = LogManager.getLogger(LoginTest.class);
log.info("Starting login test");
log.info("Entering credentials");
```

**Expected Result:** The framework records screenshots on failure and logs execution steps for troubleshooting.

---

### 16. Selenium Grid and Cloud Execution

RemoteWebDriver allows execution on a grid or cloud browser provider.

```java
ChromeOptions options = new ChromeOptions();
WebDriver driver = new RemoteWebDriver(new URL("http://localhost:4444/wd/hub"), options);
driver.get("https://example.com");
System.out.println(driver.getTitle());
driver.quit();
```

**Expected Result:** The test runs on a remote browser node instead of the local machine.

---

### 17. Database Testing

```java
Connection connection = DriverManager.getConnection(dbUrl, dbUser, dbPassword);
Statement statement = connection.createStatement();
ResultSet resultSet = statement.executeQuery("SELECT email FROM users WHERE id = 1");

if (resultSet.next()) {
    Assert.assertEquals(resultSet.getString("email"), "demo@example.com");
}
```

**Expected Result:** The database value matches the expected UI/API test data.

---

### 18. Cucumber BDD

```gherkin
Feature: Login
  Scenario: Valid user logs in
    Given user is on the login page
    When user enters valid credentials
    Then dashboard should be displayed
```

```java
@Given("user is on the login page")
public void userIsOnLoginPage() {
    driver.get(baseUrl + "/login");
}
```

**Expected Result:** A readable Gherkin scenario executes Selenium Java step definitions.

---

## Building a Selenium Java Framework from Scratch

### Recommended Framework Structure

```text
selenium-java-framework/
├── pom.xml
├── testng.xml
├── src/test/java/
│   ├── base/BaseTest.java
│   ├── factory/DriverFactory.java
│   ├── pages/BasePage.java
│   ├── pages/LoginPage.java
│   ├── tests/LoginTest.java
│   ├── tests/ApiTests.java
│   ├── listeners/TestListener.java
│   └── utils/
│       ├── ConfigReader.java
│       ├── WaitUtil.java
│       ├── ScreenshotUtil.java
│       ├── ExcelUtil.java
│       └── ApiUtil.java
├── src/test/resources/
│   ├── config.properties
│   ├── log4j2.xml
│   └── testdata.xlsx
└── reports/
```

### Required Files

| File | Required? | Purpose |
|---|---:|---|
| `pom.xml` | Yes | Maven dependencies and plugins. |
| `testng.xml` | Recommended | Test suite, browser parameters, groups, and parallel execution. |
| `BaseTest.java` | Yes | Driver setup and teardown. |
| `DriverFactory.java` | Yes | Browser creation logic. |
| `BasePage.java` | Recommended | Shared page methods and waits. |
| Page classes | Yes for POM | Encapsulate locators and page actions. |
| Test classes | Yes | Contain test scenarios and assertions. |
| `ConfigReader.java` | Recommended | Reads URLs and framework settings. |
| `WaitUtil.java` | Recommended | Centralized explicit wait methods. |
| `ScreenshotUtil.java` | Recommended | Captures screenshots on failure. |
| `TestListener.java` | Recommended | Hooks into pass/fail/skip events. |
| `log4j2.xml` | Recommended | Logging configuration. |
| Reporting config | Recommended | Extent or TestNG report setup. |

### DriverFactory Example

```java
public class DriverFactory {
    public WebDriver initDriver(String browser) {
        switch (browser.toLowerCase()) {
            case "firefox": return new FirefoxDriver();
            case "edge": return new EdgeDriver();
            default: return new ChromeDriver();
        }
    }
}
```

### BaseTest Example

```java
public class BaseTest {
    protected WebDriver driver;

    @BeforeMethod
    @Parameters("browser")
    public void setUp(@Optional("chrome") String browser) {
        driver = new DriverFactory().initDriver(browser);
        driver.manage().window().maximize();
        driver.get("https://example.com");
    }

    @AfterMethod
    public void tearDown() {
        if (driver != null) {
            driver.quit();
        }
    }
}
```

### Framework Build Steps

1. Create Maven project.
2. Add Selenium, TestNG, Log4j2, Extent Reports, REST Assured, and Apache POI dependencies.
3. Create `BaseTest` for setup/teardown.
4. Create `DriverFactory` for browser selection.
5. Create page classes using POM.
6. Create utilities for waits, screenshots, JavaScript, config, Excel, API, and database.
7. Create TestNG XML suites.
8. Add TestNG listeners for screenshots on failure.
9. Add logging and reporting.
10. Add Maven profiles for smoke/regression execution.
11. Add CI/CD through Jenkins or GitHub Actions.

---

## When to Build Framework from Scratch vs Use Pre-Built Frameworks

| Scenario | Use Simple / Pre-Built Setup | Build Custom Framework From Scratch |
|---|---|---|
| Learning Selenium basics | Yes | No |
| Small smoke suite | Yes | No |
| 10-30 tests | Yes, light POM only | Usually no |
| 100+ regression tests | No | Yes |
| Multiple browsers/environments | Maybe | Yes |
| Data-driven testing from Excel/API/DB | Maybe | Yes |
| CI/CD and custom reports | Maybe | Yes |
| Multiple teams maintaining tests | No | Yes |
| BDD required by stakeholders | Use Cucumber starter | Build BDD framework layer |
| Grid/cloud execution | Use provider template | Build grid/cloud integration layer when scale requires it |

### Popular Selenium Java Framework Patterns

| Framework Pattern | Best For | Tools |
|---|---|---|
| Selenium + TestNG + Maven | Standard UI automation | Selenium, TestNG, Maven |
| Selenium + POM + TestNG | Maintainable regression suites | Page Object Model, TestNG |
| Selenium + Page Factory | Page object element initialization | `@FindBy`, `PageFactory` |
| Selenium + Cucumber BDD | Business-readable scenarios | Cucumber, Gherkin |
| Selenium + REST Assured | UI plus API testing | Selenium, REST Assured |
| Selenium + Apache POI | Excel-driven testing | POI, DataProvider |
| Selenium + Extent Reports | Portfolio/reporting | Extent Reports, screenshots |
| Selenium Grid Framework | Cross-browser/OS scale | Grid, RemoteWebDriver |
| Selenium + Jenkins | CI/CD execution | Jenkins, Maven, GitHub |
| Hybrid Keyword/Data-Driven Framework | Keyword-driven execution | Excel/CSV, POI, reflection |

**Recommendation:** The most practical professional setup is **Selenium 4 + Java + Maven + TestNG + Page Object Model + explicit waits + Log4j2 + Extent Reports + REST Assured + CI/CD**. Build custom framework layers only when the test suite has enough size, repetition, reporting needs, test data complexity, or CI/CD requirements to justify it.

---

## Top 30 Selenium Java Technical Interview Questions with Code Examples

| # | Question | Short Answer / Code Example |
|---:|---|---|
| 1 | What is Selenium WebDriver? | Browser automation API. `WebDriver driver = new ChromeDriver();` |
| 2 | `findElement` vs `findElements`? | `findElement` throws if missing; `findElements` returns empty list. |
| 3 | Best locator strategy? | Prefer `id`, `name`, CSS, then relative XPath. |
| 4 | What is explicit wait? | `wait.until(ExpectedConditions.visibilityOfElementLocated(By.id("msg")));` |
| 5 | Implicit vs explicit wait? | Implicit is global; explicit waits for a specific condition. |
| 6 | How do you handle stale elements? | Re-locate element or use `ExpectedConditions.refreshed(...)`. |
| 7 | How do you switch to iframe? | `driver.switchTo().frame("frameName");` |
| 8 | How do you handle alerts? | `driver.switchTo().alert().accept();` |
| 9 | How do you handle windows? | Loop through `driver.getWindowHandles()`. |
| 10 | What is POM? | Page classes store locators/actions separate from tests. |
| 11 | What is Page Factory? | `PageFactory.initElements(driver, this);` initializes `@FindBy` fields. |
| 12 | How do you run parallel tests? | TestNG XML: `parallel="tests" thread-count="2"`. |
| 13 | How do you take screenshot? | `((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);` |
| 14 | How do you execute JavaScript? | `((JavascriptExecutor)driver).executeScript("arguments[0].click();", element);` |
| 15 | How do you select dropdown values? | `new Select(element).selectByVisibleText("United States");` |
| 16 | How do you check checkbox state? | `element.isSelected();` |
| 17 | How do you mouse hover? | `new Actions(driver).moveToElement(menu).perform();` |
| 18 | How do you drag and drop? | `new Actions(driver).dragAndDrop(source, target).perform();` |
| 19 | How do you upload a file? | `fileInput.sendKeys("C:\\files\\test.pdf");` |
| 20 | What is Selenium Grid? | Remote execution across browsers/nodes. |
| 21 | What is TestNG DataProvider? | Runs test with multiple data sets. |
| 22 | What are TestNG listeners? | Hooks for pass/fail/skip and reporting events. |
| 23 | How do you read config? | Use `Properties` and `FileInputStream`. |
| 24 | How do you add API tests? | Use REST Assured in the same Maven framework. |
| 25 | How do you validate database data? | Use JDBC `Connection`, `Statement`, `ResultSet`. |
| 26 | Dynamic XPath example? | `//td[text()='Brian']/following-sibling::td/button` |
| 27 | ElementNotInteractable cause? | Hidden, disabled, overlapped, or not ready. |
| 28 | NoSuchElement cause? | Wrong locator, timing, iframe, or wrong page. |
| 29 | Stable framework design? | POM, waits, utilities, logging, reports, CI, isolated data. |
| 30 | What should be automated? | High-value repeatable flows: login, checkout, search, forms, APIs, regression. |

---

## Best Practices

- Use stable locators and avoid brittle absolute XPath.
- Prefer explicit waits over hard sleeps.
- Keep page locators inside page classes.
- Keep tests focused on business scenarios.
- Use TestNG groups for smoke/regression suites.
- Use DataProviders for repeated data scenarios.
- Capture screenshots on failure.
- Add logging and readable reports.
- Keep configuration outside code.
- Use API setup where UI setup is slow.
- Use Grid/cloud execution only when cross-browser scale is needed.
- Start simple, then add framework layers as the suite grows.

---

## How to Run

```bash
git clone https://github.com/BrianGator/Selenium-WebDriver-Automation-w-Java-Ninja-Showcase.git
cd Selenium-WebDriver-Automation-w-Java-Ninja-Showcase
mvn clean test
```

Run a TestNG suite:

```bash
mvn clean test -DsuiteXmlFile=testng.xml
```

Run with a browser parameter:

```bash
mvn clean test -Dbrowser=chrome
```

---

## Author

**Written by Brian McCarthy**

This repository demonstrates Selenium WebDriver automation with Java, TestNG, Maven, REST Assured, Page Object Model, Page Factory, logging, reporting, data-driven testing, Selenium Grid, Jenkins, GitHub, Cucumber BDD, database testing, and framework design best practices.
