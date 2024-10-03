# STARTER-jpa01

* TODO: Change the title of this README 
  in the text `# STARTER-jpa01` above
  to match the name of your repo, i. e., `jpa01-yourgithubid`, then delete
  this TODO item.

* TODO: Correct the links to repo below, 
  then delete this TODO.  Replace it with 
  a link to your repo, e.g. 
  https://github.com/ucsb-cs156-s24/jpa01-cgaucho

Repo: https://ucsb-cs156-s24/STARTER-jpa01

* TODO: Correct the "deployed at" link to app on Dokku
  then delete this TODO.  Replace it with 
  a link to your running app on Dokku, e.g.
  https://jpa01-cgaucho.dokku-14.cs.ucsb.edu


Deployed at: https://jpa01-replace-me.dokku-xx.cs.ucsb.edu


# About this repo

This is a minimal "Hello World" type webapp built with Spring Boot.

# What can you do with this code?

| Command | What it does   |
|----------|---------------------------------------|
| `mvn compile` | Should result in a clean compile |
| `mvn test` | Runs JUnit tests on the code base |
| `mvn test jacoco:report` | Runs JUnit tests, and if all tests pass, computes code coverage.  The code coverage report (Jacoco) can be found in `target/site/jacoco/index.html` |
| `mvn test pitest:mutationCoverage` | Runs JUnit tests, and if all tests pass, runs pit (pitest.org) mutation testing to measure effectivness of test suite |
| `mvn package` | Builds the jar file `target/gs-spring-boot-0.1.0.jar` |
| `mvn spring-boot:run` | Runs the code to startup a web server.  Access it via `http://localhost:8080` on the *same machine* where the server is running.  Use CTRL/C to stop it. |
| `java -cp target/hello-1.0.0.jar edu.ucsb.cs156.spring.hello.Application` | If done after `mvn package`, runs the code to startup a web server.  |
| `java -jar target/hello-1.0.0.jar | If done after `mvn package`, this is another way to start up the web server.|


# Sources

The code in this repo is in support of
jpa01 for Fall 2022 for CMPSC 156.

The code in this repo is based in part on the tutorial here:
<https://spring.io/guides/gs/spring-boot/>, and the code here in the
`complete` directory of this repo
<https://github.com/spring-guides/gs-spring-boot.git>.  

That code has been
modified for use in UCSB CMPSC 156 as described
below.

# Modifications from the original

* Java 21 support
  * Converting `pom.xml` to use Java 17
* JUnit 5
  * Converting test code to use JUnit 5 instead of JUnit 4  
* Dokku Support
  * Ensuring that the `PORT` environment variable is
    used to define the port on which Spring Boot starts the web server 
* Testing and CI
  * Adding JUnit tests
  * Adding jacoco as a plugin to measure test 
    case coverage
  * Adding pitest for mutation test coverage.
  * Adding support for GitHub Actions to run
    the test cases, compute jacoco report,
    upload code coverage reports to Codecov.io,
    and produce pitest artifacts.

