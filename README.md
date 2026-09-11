# nv-18n client sample project

This is a multi-module project which shows how to make use of the `nv-i18n` library on two different Java versions:

| Module | Java version | Artifact |
|--------|--------------|----------|
| `java25` | 25 | `nv-i18n-client-sample-java25` |
| `java8`  | 1.8 | `nv-i18n-client-sample-java8` |

Both modules contain the same main class, `uk.co.foundationsedge.Example` (declared in each module's `pom.xml` via the `maven-jar-plugin` and `exec-maven-plugin`).

## Running

Run a single module:

```
mvn -pl java25 clean compile exec:java
mvn -pl java8 clean compile exec:java
```

Run both modules:

```
mvn -pl java25,java8 clean compile exec:java
```

Note: building the `java25` module requires a JDK 25+ (e.g. `JAVA_HOME=/usr/lib/jvm/java-26-temurin`), while the `java8` module compiles to Java 1.8 bytecode and can be built with any modern JDK.
