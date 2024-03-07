[![Java-Build Action Status](https://github.com/Hotmoka/io-hotmoka-testing/actions/workflows/java_build.yml/badge.svg)](https://github.com/Hotmoka/io-hotmoka-testing/actions)
[![Maven Central](https://img.shields.io/maven-central/v/io.hotmoka.testing/io-hotmoka-testing.svg?label=Maven%20Central)](https://central.sonatype.com/search?smo=true&q=g:io.hotmoka.testing)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)

# Utilities for JUnit testing classes

This project provides utilities supporting testing with JUnit.

## Test logging

The class `AbstractLoggedTests` allows one to create test classes that log
their tests into a log file named like the class. For each test, a header is logged, with the
name of the test, followed by the logging for the test.

For that, it's enough to subclass `AbstractLoggedTests`:

```java
public class MyTestClass extends AbstractLoggedTests {

  @Test
  @DisplayName("my smart test")
  public void test1() {
    ...
  }

  @Test
  @DisplayName("my smarter test")
  public void test2() {
    ...
  }
}
```

The execution of this JUnit test will create a `MyTestClass.log` file containing two headers, one
for each test, followed by the logs generated during the execution of the test.

<p align="center"><img width="100" src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by.png" alt="This documentation is licensed under a Creative Commons Attribution 4.0 Internat
ional License"></p><p align="center">This document is licensed under a Creative Commons Attribution 4.0 International License.</p>

<p align="center">Copyright 2024 by Fausto Spoto (fausto.spoto@hotmoka.io)</p>