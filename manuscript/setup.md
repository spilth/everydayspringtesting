# Setup

## Installing Software

To build and test a modern Spring Boot application, you will need the following installed:

- [Homebrew](http://brew.sh) - Package Manager for OS X
- [JDK 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) - Java Development Kit 8
- [IntelliJ IDEA 15](https://www.jetbrains.com/idea/) - A recommended IDE for working on Java projects
- [Apache Maven](https://maven.apache.org) - A Java Build Tool
- [Spring Boot CLI](http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#cli) - Command-line Interface for creating Spring Boot applications

### Installing Homebrew

The latest instructions for installing Homebrew can be found on the [Homebrew web site](http://brew.sh). As of this writing, the way to install Homebrew is with the following command:

```sh
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

To make sure you have a complete and up to date install of Homebrew, run the following commands as well:

```sh
brew update
brew doctor
```

Running `brew doctor` make give you a list of issues to resolve.

### Installing Everything Else

All the tools we'll be using are installable using Homebrew:

```sh
$ brew cask install java
$ brew cask install intellij-idea
$ brew install git
$ brew install maven
$ brew install pivotal/tap/springboot
```

## Creating the Project

To create the project we'll be testing with we'll use the `spring init` command and pass the name of the project and the dependendies we want to use:

```sh
$ spring init everyday -d=web,freemarker,actuator,devtools,h2
```

The dependencies we'll be using are:

- `web`
- `h2`
- `freemarker`
- `actuator`
- `devtools`

Now you can change into the project directory and check out the structure of it:

```sh
$ cd everyday
$  ls -1A
.mvn
mvnw
mvnw.cmd
pom.xml
src
```

- `.mvn`, `mvwn` and `mvnw.cmd` are wrappers for Maven supplied by the CLI
- `pom.xml` - This is your Maven Project file which describes your project, its dependencies and its build configuration
- `src` - This is where your source code and resources live