# Getting Started

When you create a project using the Spring Boot CLI, `spring-boot-starter-test` is automatically included as a dependency and brings a number of helpful libraries along with it:

    $ spring init testing -d=web
    $ cd testing
    $ mvn dependency:tree
    
    [INFO] Scanning for projects...
    ...
    [INFO] \- org.springframework.boot:spring-boot-starter-test:jar:1.2.7.RELEASE:test
    [INFO]    +- junit:junit:jar:4.12:test
    [INFO]    +- org.mockito:mockito-core:jar:1.10.19:test
    [INFO]    |  \- org.objenesis:objenesis:jar:2.1:test
    [INFO]    +- org.hamcrest:hamcrest-core:jar:1.3:test
    [INFO]    +- org.hamcrest:hamcrest-library:jar:1.3:test
    [INFO]    \- org.springframework:spring-test:jar:4.1.8.RELEASE:test

Let's go through these one by one:    
    
- [JUnit](http://junit.org) - JUnit is a simple framework to write repeatable tests. It is an instance of the xUnit architecture for unit testing frameworks.
- [Mockito](http://mockito.org) - Mocking Framework
- [Hamcrest](http://hamcrest.org) - Matchers that can be combined to create flexible expressions of intent
- [Spring Test](http://docs.spring.io/spring/docs/current/spring-framework-reference/htmlsingle/index.html#testing) - Testing support for Spring

### Additional Testing Libraries

We'll also be using the following libraries:

- [Cucumber](https://cucumber.io)
- [Simplelenium](https://github.com/dgageot/simplelenium)

You can open up `pom.xml` and add the following `dependencies` to add them to your project:

    <dependency>
        <groupId>net.code-story</groupId>
        <artifactId>simplelenium</artifactId>
        <version>2.1</version>
        <scope>test</scope>
    </dependency>
    <dependency>
        <groupId>info.cukes</groupId>
        <artifactId>cucumber-java8</artifactId>
        <version>1.2.3</version>
        <scope>test</scope>
    </dependency>
    <dependency>
        <groupId>info.cukes</groupId>
        <artifactId>cucumber-junit</artifactId>
        <version>1.2.3</version>
        <scope>test</scope>
    </dependency>
    <dependency>
        <groupId>info.cukes</groupId>
        <artifactId>cucumber-spring</artifactId>
        <version>1.2.3</version>
        <scope>test</scope>
    </dependency>

- TODO: What requires `org.springframework.spring-tx`?

## Definitions

Before we dive into testing, it's important to understand the landscape of testing and the terms that used.

### Unit Tests

### Integration Tests

### Feature Tests

### Assertions

### Matchers

### Mocking

### Stubbing


