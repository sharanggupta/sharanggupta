<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="assets/banner-light.svg">
  <img alt="Java, Spring, TDD. Java and Spring, built test-first." src="assets/banner-light.svg">
</picture>

Software engineer at THG in Bournemouth, England. MSc Computer Science (Distinction), University of Southampton.

I work mostly in Java and Spring, test-first. Lately I've been sending fixes upstream to open-source libraries I use, and writing up what I learn with small apps that each demonstrate exactly one thing.

[Website](https://www.sharanggupta.dev) · [Writing](https://sharanggupta.medium.com) · [LinkedIn](https://www.linkedin.com/in/sharanggupta/)

---

## Merged upstream

Fixes and features that landed in projects I use. The eight below are the ones I would show first;
[all of them, with what each problem was and how it was fixed](https://www.sharanggupta.dev/open-source), are on my website.

| Project | Change |
|---|---|
| [Spring Framework](https://github.com/spring-projects/spring-framework/pull/37543) | `ProtobufDecoder` releases the buffer of a partly read message when the subscriber cancels, so pooled buffers no longer leak. |
| [Micronaut Core](https://github.com/micronaut-projects/micronaut-core/pull/13801) | An `Accept-Charset` header no longer decides how a `String` request body is decoded. |
| [Eclipse Jetty](https://github.com/jetty/jetty.project/pull/15976) | A web application in a directory such as `foo.com` deploys as one app, together with its properties file (#14127). |
| [Apache Commons Lang](https://github.com/apache/commons-lang/pull/1812) | `TypeUtils.containsTypeVariables` and `unrollVariables` honour the owner type of a `ParameterizedType`, so `Outer<T>.Inner` resolves (LANG-1836). |
| [Apache Log4j 2](https://github.com/apache/logging-log4j2/pull/4400) | Timestamps before 1970 format correctly; found by differential fuzzing against `java.time`, with no prior report. |
| [SpotBugs](https://github.com/spotbugs/spotbugs/pull/4377) | An ignored `Arrays.copyOf` result is reported; the root cause, `Class.desiredAssertionStatus()` taken for a side effect, hid every pure method of a class that uses `assert`. |
| [Spring Integration](https://github.com/spring-projects/spring-integration/pull/11535) | The FTP and FTPS session factories connect through a SOCKS or HTTP proxy, a request open since 2012. |
| [OpenFeign](https://github.com/OpenFeign/feign/pull/3605) | A `Request` built with a `null` body behaves like one with an empty body instead of throwing on first access. |

Also landed in [Apache Tomcat](https://github.com/apache/tomcat/pull/1094), [Apache Dubbo](https://github.com/apache/dubbo/pull/16527),
[Mockito](https://github.com/mockito/mockito/pull/3890), [Apache Camel](https://github.com/apache/camel/pull/28129),
[Apache Maven](https://github.com/apache/maven/pull/13498), [ArchUnit](https://github.com/TNG/ArchUnit/pull/1747),
[Spring AMQP](https://github.com/spring-projects/spring-amqp/pull/3728), [Spring Cloud Config](https://github.com/spring-cloud/spring-cloud-config/pull/3346),
[Spring Cloud Stream](https://github.com/spring-cloud/spring-cloud-stream/pull/3296), [Apache Felix](https://github.com/apache/felix-dev/pull/575),
[Apache WSS4J](https://github.com/apache/ws-wss4j/pull/761), [Eclipse Yasson](https://github.com/eclipse-ee4j/yasson/pull/789),
[Eclipse Angus Mail](https://github.com/eclipse-ee4j/angus-mail/pull/215) and [Eclipse Mojarra](https://github.com/eclipse-ee4j/mojarra/pull/6066):
36 pull requests in 22 projects so far, nearly all with a test that fails without the change.

More are in review: [open pull requests](https://github.com/pulls?q=is%3Apr+author%3Asharanggupta+is%3Aopen+-user%3Asharanggupta).

## Selected projects

- **[orderly](https://github.com/sharanggupta/orderly)** (work in progress): a Java 21 walk from controller-service-repository to hexagonal architecture, one failing test at a time. Module boundaries are enforced by the build.
- **[flight-search](https://github.com/sharanggupta/flight-search)**: a Spring Boot REST API built test-first with a hexagon that never depends on the outside at compile time.
- **[eazybank](https://github.com/sharanggupta/eazybank)**: Spring Boot microservices with an API gateway, deployed on Kubernetes, with metrics, logs and distributed tracing (Prometheus, Grafana, Loki, Tempo).
- **[oauth2product](https://github.com/sharanggupta/oauth2product)**: OAuth2 resource server and client with Spring Boot, built test-first. The article series below follows this code.

## Writing

A four-part series on OAuth2 with Spring Boot, each part with a working app:

1. [Demystifying OAuth2](https://sharanggupta.medium.com/demystifying-oauth2-a-step-by-step-guide-to-building-a-resource-server-with-spring-boot-tdd-6da6912411a5)
2. [Building an OAuth2 Resource Server](https://sharanggupta.medium.com/building-an-oauth2-resource-server-in-spring-boot-tdd-621a34999410)
3. [Building an OAuth2 Client](https://sharanggupta.medium.com/part-3-building-an-oauth2-client-in-spring-boot-tdd-91b0ba8ee5ae)
4. [Running the System End-to-End](https://sharanggupta.medium.com/part-4-running-the-system-end-to-end-spring-multi-module-docker-86a41a128e46)

---

Day-to-day work at THG lives in private repositories; my work account is [@sharang-gupta-thg](https://github.com/sharang-gupta-thg).
