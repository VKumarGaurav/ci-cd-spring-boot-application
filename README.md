# hello-cicd

Simple Spring Boot 3 (Java 17) app with two GET APIs.

## Run
    mvn spring-boot:run

## APIs
    GET http://localhost:8080/api/hello        -> Hello World
    GET http://localhost:8080/api/hello-cicd   -> Hello CI/CD
    GET http://localhost:8080/actuator/health  -> {"status":"UP"}

## Test
    mvn clean test

## Docker
    docker build -t hello-cicd .
    docker run -p 8080:8080 hello-cicd

## CI
GitHub Actions workflow at `.github/workflows/ci.yml` builds, tests and builds the Docker image on every push/PR to `main`.
