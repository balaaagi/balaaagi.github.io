---
title: "Testing Spring Boot apps"
date: 2021-03-26T16:02:55+05:30
draft: false
---

Spring boot becoming a common defacto for writing micro-services in the Java ecosystem. We have a lot of frameworks and options to write unit and integration tests are available. Below are the few resources, that I have looked upon in the past to improve my unit testing skills

* [Test Containers](https://www.sivalabs.in/2020/02/spring-boot-integration-testing-using-testcontainers-starter) - By Siva
* [Testing Spring Boot](https://www.baeldung.com/spring-boot-testing)- By Baeldung

We are not going to discuss in detail writing unit-testing. But setting up the necessary things that enable us to independently write end-to-end tests for our spring boot applications. 


## Assumption
Our application is going to be a simple backend service connected with a database. In our case, let's assume it is Postgres. Based on your application architecture the same template can be changed. Below the types of tests we have 
* Controller Level Tests
* Service Level Tests
* Core Business Logic

Most of the time we might miss validating our repository/data layer via tests under the assumption all will be fine. But if we do it, it is always good to ensure we don't end up with weird data issues in production. As I mentioned above `TestContainers` are a good way to write tests including embedded databases. Cored database schema migrations are integrated into the application bootup. We can use tools like `flyway` or `liquibase` to do this. 


## Settings
For our application, we should have the below properties `src/test/java/resource/application.properties` for effective testing

{{< gist balaaagi a1e02965015fab903a66b94e9d826193 >}}



We have passed our values to be env variables. You can refer [here](https://balaaagi.in/post/envsinspringboot/)

### Base Image

Create a base image for your projects and push it to some registry. Either docker hub or anything which can be accessed. Please keep this base image minimal without any confidential details of your project. Let's assume we have a base image named `orgname/base-springboot`

{{< gist balaaagi bd57215588177be2cec52960552d5c25 >}}


We would need a `docker-compose.yml` file to have this setup working end to end. Below is a docker-compose that can be used for reference

{{< gist balaaagi bcc4b75527d566b42128fdbf479cd790 >}}

## How to Run the tests?

Below is the simple command that can be used to run the tests

`docker-compose up --abort-on-container-exit --exit-code-from application_under_test`

What the above command does is spins the DB, application and runs the tests. If a test failed it gets exit. The same command can be used in CI/CD pipelines also. To fasten the process the base image should be built with all common dependencies. 
















 