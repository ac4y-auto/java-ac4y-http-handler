# java-ac4y-http-handler - Architektúra Dokumentáció

## Áttekintés

HTTP service handler Apache HttpClient-tel REST API hívásokhoz.

**Verzió:** 1.0.0
**Java verzió:** 1.8
**Szervezet:** ac4y-auto

## Fő Komponensek

### Ac4yHttpServiceHandler

**Csomag:** `ac4y.service.http`

HTTP GET kérés kezelő.

**Metódus:**
- `getResponse(aHost, aServiceName, aRequest)` - HTTP GET kérés végrehajtása

**URL összeállítás:** `host + serviceName + request`

**Fejlécek:** `Accept: application/json`

**Használat:**
```java
Ac4yHttpServiceHandler handler = new Ac4yHttpServiceHandler();
String response = handler.getResponse(
    "http://localhost:8080/",
    "api/users",
    "?id=123"
);
```

## Függőségek

```xml
<dependency>
    <groupId>org.apache.httpcomponents</groupId>
    <artifactId>httpclient</artifactId>
    <version>4.3.4</version>
</dependency>
```

## AI Agent Használati Útmutató

### Token-hatékony Tudás

**Mit tartalmaz:**
- HTTP GET kérés kezelés
- JSON response fogadás
- URL összeállítás komponensekből

**Mit NEM tartalmaz:**
- POST/PUT/DELETE (ehhez lásd: `Ac4yRestServiceClient` az `ac4y-service-domain`-ban)
- Connection pooling
- Async kérések

## Eredetileg

`IJAc4yServiceModule/HttpHandler` modulból kiemelve.

---
**Utolsó frissítés:** 2026-02-06
