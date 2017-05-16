# Mock Eureka! Clinical Central Authentication Service
Mock CAS server for system tests of Eureka! Clinical components

## Version history
### Version 1.0
Initial release. Supports all features that Eureka! Clinical uses.

## What does it do?
It provides RESTful APIs for users to request an account, manage their profile and change their password. It also provides APIs for an administrator to create accounts.

## Building it
The project uses the maven build tool. Typically, you build it by invoking `mvn clean install` at the command line. For simple file changes, not additions or deletions, you can usually use `mvn install`. See https://github.com/eurekaclinical/dev-wiki/wiki/Building-Eureka!-Clinical-projects for more details.

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
