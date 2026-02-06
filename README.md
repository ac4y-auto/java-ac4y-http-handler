# java-ac4y-http-handler

HTTP service handler using Apache HttpClient for REST API calls.

## Maven Dependency

```xml
<dependency>
    <groupId>ac4y</groupId>
    <artifactId>ac4y-http-handler</artifactId>
    <version>1.0.0</version>
</dependency>
```

## Overview

Provides `Ac4yHttpServiceHandler` for making HTTP GET requests to REST services. Constructs URLs from host + serviceName + request components and returns JSON responses.

## Dependencies

- `org.apache.httpcomponents:httpclient:4.3.4`

## Usage

```java
Ac4yHttpServiceHandler handler = new Ac4yHttpServiceHandler();
String response = handler.getResponse(
    "http://localhost:8080/",
    "api/users",
    "?id=123"
);
```

## Build

```bash
mvn clean install
mvn test
```

## Origin

Extracted from `IJAc4yServiceModule/HttpHandler` module.

---
**Version:** 1.0.0
