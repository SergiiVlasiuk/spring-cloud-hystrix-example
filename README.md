[![Build Status](https://travis-ci.org/ExampleDriven/spring-cloud-hystrix-example.svg?branch=master)](https://travis-ci.org/ExampleDriven/spring-cloud-hystrix-example)
# spring-cloud-hystrix-example
Spring Cloud Hystrix example

This is the source code for the blog post

https://exampledriven.wordpress.com/2016/07/05/spring-cloud-hystrix-example/

This example covers the following :


Feature | Test URL
--- | ---
 Hystrix circuit breaker, fallback using @HystrixCommand | [http://localhost:8080/customer-fallback/2](http://localhost:8080/customer-fallback/2)
 Hystrix request collapser using @HystrixCollapser | URL1: [http://localhost:8080/customer-collapser/1](http://localhost:8080/customer-collapser/1)
  URL2: [http://localhost:8080/customer-collapser/2](http://localhost:8080/customer-collapser/2)
 Hystrix stream | [http://localhost:8080/hystrix.stream](http://localhost:8080/hystrix.stream)
 Hystrix dashboard | [http://localhost:8081/hystrix/monitor?stream=http://localhost:8082/turbine.stream http://localhost:8081/hystrix/monitor?stream=http%3A%2F%2Flocalhost%3A8080%2Fhystrix.stream](http://localhost:8081/hystrix/monitor?stream=http://localhost:8082/turbine.stream http://localhost:8081/hystrix/monitor?stream=http%3A%2F%2Flocalhost%3A8080%2Fhystrix.stream)
 Turbine stream | [http://localhost:8082/turbine.stream](http://localhost:8082/turbine.stream)

Cache |
  URL1: [http://localhost:8080/customer-cache/2?name=Peter](http://localhost:8080/customer-cache/2?name=Peter)
  URL2:  [http://localhost:8080/customer-cache/2?name=Peter2](http://localhost:8080/customer-cache/2?name=Peter2)

===================================
---

## Make it working with spring boot2

    http://localhost:8080/actuator/hystrix.stream

## is not resolved - Turbine???

## to be considered:

 - service-registry
 - org.springframework.cloud.netflix.turbine.stream.TurbineApplication

# Docs:

 - [circuit_breaker_hystrix_clients](https://cloud.spring.io/spring-cloud-netflix/single/spring-cloud-netflix.html#_circuit_breaker_hystrix_clients)
 - [Finchley.SR1 turbine_stream](https://cloud.spring.io/spring-cloud-static/Finchley.SR1/single/spring-cloud.html#_turbine_stream)
 - [Greenwich.RELEASE ystrix_timeouts_and_ribbon_clients](https://cloud.spring.io/spring-cloud-static/Greenwich.RELEASE/single/spring-cloud.html#_hystrix_timeouts_and_ribbon_clients)
 - [spring-cloud-stream](https://docs.spring.io/spring-cloud-stream/docs/current/reference/htmlsingle/)
