## Spring WebFlux and Reactive WebClient Demo Project

In this demo project you may examples of reactive endpoints built on top of Spring WebFlux, and using `WebClient` for calling other resources.
1. Explaining different communication models in reactive application with Spring WebFlux. Differences between standard `application/json` content type and `application/stream+json`. 
2. A detailed analyse of threading and concurrency model used by Spring WebFlux and Reactor Netty. It also threats about `WebClient` and Spring Boot Actuator pooling.

### Guide

Required:
1. JDK 11+
2. Maven

How to run ?
`mvn clean install`

There are two JUnit tests: `PerformanceSpringWebFluxTest` and `SampleSpringWebFluxTest`.

To provide some standalone tests just run the main class `SampleSpringWebFluxApp`.
For generating some traffic to the application run application `SendingApp`. It runs `MockWebServer` on localhost:8082 in order to mock downstream service called by `WebClient` and than calls endpoints exposed by the application usung `TestRestTemplate`.