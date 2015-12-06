# Feature Testing

## What is a Feature Test?

TK

## Feature Tests with Simplelenium

### Add Simplelenium as a Dependency

First we add [Simplelenium](https://github.com/dgageot/simplelenium) as a dependency in our `pom.xml`:

```xml
<dependency>
    <groupId>net.code-story</groupId>
    <artifactId>simplelenium</artifactId>
    <version>2.1</version>
    <scope>test</scope>
</dependency>
```

### Creat a Basic Feature Test

Then we add a feature test that looks for a message on the homepage of our web application:

```java
package features;

import com.example.DemoApplication;
import net.codestory.simplelenium.SeleniumTest;
import org.junit.Test;
import org.junit.runner.RunWith;
import org.springframework.boot.test.SpringApplicationConfiguration;
import org.springframework.boot.test.WebIntegrationTest;
import org.springframework.test.context.junit4.SpringJUnit4ClassRunner;

@RunWith(SpringJUnit4ClassRunner.class)
@SpringApplicationConfiguration(classes = DemoApplication.class)
@WebIntegrationTest
public class HomepageTest extends SeleniumTest {
    @Test
    public void itContainsMessage() {
        goTo(getDefaultBaseUrl());

        find("body").should().contain("Hello, world!");
    }

    @Override
    protected String getDefaultBaseUrl() {
        return "http://localhost:8080";
    }
}
```

When we run this test we see that it fails.

Simplelenium will automatically take a screenshot of any failing test and place it a `snapshots` folder in the root of the project. If we open up the `HomepageTest_homepage_containsMessage.png` we'll see a message about a `Whitelabel Error Page`.

You can confirm this by starting the application manually with `mvn spring-boot:run` and opening <http://localhost:8080> in your browser.

## Feature Tests with Fluentlenium

TK

## Cucumber

TK

## Page Object Pattern

TK