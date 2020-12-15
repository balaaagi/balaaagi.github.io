---
title: "Environment Variables In Spring Boot Application"
date: 2020-12-15T19:33:17+05:30
draft: false
categories : [ "java", "springboot", ]
---

Spring Boot lets you externalize [configurations](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-external-config) for our application. Let's take a simple application that connects to the database and perform some operations on it. The standard configuration for this kind of app would be the database related details. Below is one sample `properties` file

{{< gist balaaagi b752d0afe3969f5903a046ac2dcaab08 >}}

Like this, we might have more properties specific to our application also which we want to have as dynamic configurations that can be passed when application startup. In order to have these have different across different environments like dev, staging, production. Spring boot provides us with [option ](https://docs.spring.io/spring-boot/docs/current/reference/html/spring-boot-features.html#boot-features-external-config-files-profile-specific) to have environment-specific files with different values for different environments.

Below are a few common practices developers follow which has their own pros and cons

*  Commit secrets in these files as part of the codebase
*  Commit only local configuration in the codebase and as part of deployment pipeline copy environment-specific files from the different repository and build the package

If we are having separate profile files then we might need to have separate start-up scripts for each to ensure the right profile details are passed. If we are copying files at the time of the build for any change in secrets or configurations we might need to build the package again to take effect.

According to [12factor](https://12factor.net/config) apps it's good practice to store configurations in environments.

## How can we achieve this?

* We can avoid multiple property files and have only one file as below

{{< gist balaaagi 0039a444bbc34944ec38d1c9cec00680 >}}

The above helps in multiple ways

* No need to rebuild the package again if there is any change in configuration.
* One common property file versioned as part of the code base.
* Build pipelines would be generic. Same builds can be used across all environments

### When running as containers

If we are running our application as containers we need to pass the environment variables while starting the application. This can be taken care of by a deployment pipeline. If there is a change in value just a restart of the container is enough

### When running as fat jars

If we are running our application as normal jars then the best practice would be to set the environment variables as part of the host machine and start the application. 


### What about local development/tests

For tests, I would recommend having a dedicated properties file. For local development, we can do it in two ways.
* Have one `.env` file in local and `source` them before starting the application
* We can give default values to properties if not present in environment as `spring.datasource.username=${DB_USERNAME:username}`
 

The key thing to note here is the deployment process. I will cover a detailed blog on how the deployment pipeline can be done for such a setup of spring boot application.



