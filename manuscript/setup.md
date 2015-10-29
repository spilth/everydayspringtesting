# Setup

To build and test a modern Spring Boot application, you will need the following installed:

- [Java 8 SDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [Homebrew](http://brew.sh) - Package Manager for OS X
- [Apache Maven](https://maven.apache.org) - Java Build Tool
- [Spring Boot CLI](http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#cli) - Command-line Interface for creating Spring Boot applications

## Installing Homebrew

TK

## Installing Maven

First I'll make sure my Homebrew is up to date:

    $ brew update

Then I'll install Maven:

    $ brew install maven

## Installing the Spring Boot CLI

In order to install the Spring Bot CLI you'll need to add a "tap" for their tools to your Homebrew installation. 

    $ brew tap pivotal/tap

Then you can install the CLI:

    $ brew install springboot
