# Mock Eureka! Clinical Central Authentication Service
[Georgia Clinical and Translational Science Alliance (Georgia CTSA)](http://www.georgiactsa.org), [Emory University](http://www.emory.edu), Atlanta, GA

## What does it do?
It provides a mock CAS server for system tests of Eureka! Clinical components. It responds to the following [CAS protocol version 2](https://apereo.github.io/cas/5.0.x/protocol/CAS-Protocol.html) URLs:
* `/login` (it auto authenticates the user as the `superuser`) 
* `/logout`
* `/serviceValidate`
* `/proxy`
* `/proxyValidate`

The responses are hard-coded.

## Version 2.1 development series
Latest release: [![Latest release](https://maven-badges.herokuapp.com/maven-central/org.eurekaclinical/cas-mock/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.eurekaclinical/cas-mock)

This version will include the following changes:
* Support proxy callbacks. This was inadvertently omitted from previous releases.

## Version 2.0
No feature changes. This release only updates dependencies.

## Version 1.0
Initial release. Supports all features of CAS that Eureka! Clinical uses.

## Build requirements
* [Oracle Java JDK 8](http://www.oracle.com/technetwork/java/javase/overview/index.html)
* [Maven 3.2.5 or greater](https://maven.apache.org)

## Runtime requirements
* [Oracle Java JRE 8](http://www.oracle.com/technetwork/java/javase/overview/index.html)
* [Tomcat 7](https://tomcat.apache.org)

## Building it
The project uses the maven build tool. Typically, you build it by invoking `mvn clean install` at the command line. For simple file changes, not additions or deletions, you can usually use `mvn install`. See https://github.com/eurekaclinical/dev-wiki/wiki/Building-Eureka!-Clinical-projects for more details.

## Installation
This project is intended for other Eureka! Clinical web applications to depend on it for running in embedded Tomcat. All that is needed is for the tomcat maven plugin to add it as a dependency, and for Eureka! Clinical web applications to use `https://localhost:8443/cas-mock` as the CAS server URL.

For standalone deployment, do the following:
1) Stop Tomcat.
2) Remove any old copies of the unpacked war from Tomcat's webapps directory.
3) Copy the warfile into the Tomcat webapps directory, renaming it to remove the version. For example, rename `cas-mock-1.0.war` to `cas-mock.war`.
4) Start Tomcat.

## Maven dependency
```
<dependency>
    <groupId>org.eurekaclinical</groupId>
    <artifactId>cas-mock</artifactId>
    <version>version</version>
</dependency>
```

## Developer documentation
* [Javadoc for latest development release](http://javadoc.io/doc/org.eurekaclinical/cas-mock) [![Javadocs](http://javadoc.io/badge/org.eurekaclinical/cas-mock.svg)](http://javadoc.io/doc/org.eurekaclinical/cas-mock)

## Getting help
Feel free to contact us at help@eurekaclinical.org.
