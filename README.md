# Okta Micronaut Sample

This example shows you how to use the [Micronaut's OAuth 2.0 support](https://micronaut-projects.github.io/micronaut-security/latest/guide/#oauth) to login a user. The login is achieved through the [Authorization Code Flow](https://developer.okta.com/docs/guides/implement-grant-type/authcode/main/) where the user is redirected to the Okta-Hosted login page. After the user authenticates, they are redirected back to the application and a local cookie session is created.

It also shows how to return the user's information from an API using an OAuth 2.0 access token.

## Prerequisites

Before running this sample, you will need the following:

* [Java 17+](https://sdkman.io/jdks)
* [The Okta CLI Tool](https://github.com/okta/okta-cli/#installation)
* An Okta Developer Account, create one using `okta register`, or configure an existing one with `okta login`

## Get the Code

Grab and configure this project using `okta start micronaut`.

You can also clone this repo and run `okta start` in it.

```bash
git clone https://github.com/okta-samples/okta-micronaut-sample.git
cd okta-micronaut-sample
okta start
```

## Run the Example

```bash
source .okta.env
```

### Maven

Run the application with Maven
```
./mvnw mn:run
```

The application uses [Micronaut Ahead-of-time optimizations (AOT) optimizations via the Micronaut Maven Plugin](https://micronaut-projects.github.io/micronaut-maven-plugin/latest/examples/aot.html). You can enable [Micronaut Security AOT optimizations](https://micronaut-projects.github.io/micronaut-security/latest/guide/#aot) in `aot-jar.properties`.

### Gradle

Run the application via the [Micronaut Application Gradle Plugin](https://micronaut-projects.github.io/micronaut-gradle-plugin/latest/).  

```
./gradlew run
```

or run an optimized JAR with Gradle

```
./gradle optimizedRun
```

Log in at `http://localhost:8080`.

## Learn More

For more details on how to build an application with Okta and Micronaut you can read [Build Native Java Apps with Micronaut, Quarkus, and Spring Boot](https://developer.okta.com/blog/2021/06/18/native-java-framework-comparison).

[OIDC Web Application Setup Instructions]: https://developer.okta.com/docs/guides/implement-grant-type/authcode/main/#set-up-your-app
