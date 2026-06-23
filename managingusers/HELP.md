# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/4.0.7/maven-plugin)
* [Create an OCI image](https://docs.spring.io/spring-boot/4.0.7/maven-plugin/build-image.html)
* [Spring Web](https://docs.spring.io/spring-boot/4.0.7/reference/web/servlet.html)
* [Spring Security](https://docs.spring.io/spring-boot/4.0.7/reference/web/spring-security.html)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/rest/)
* [Securing a Web Application](https://spring.io/guides/gs/securing-web/)
* [Spring Boot and OAuth2](https://spring.io/guides/tutorials/spring-boot-oauth2/)
* [Authenticating a User with LDAP](https://spring.io/guides/gs/authenticating-ldap/)

### Maven Parent overrides

Due to Maven's design, elements are inherited from the parent POM to the project POM.
While most of the inheritance is fine, it also inherits unwanted elements like `<license>` and `<developers>` from the parent.
To prevent this, the project POM contains empty overrides for these elements.
If you manually switch to a different parent and actually want the inheritance, you need to remove those overrides.

>>>>
1. Once you added the spring security dependency, and run the controller method (REST API), then it generates the password in the terminal where application is started, where user name is
   user, and password is the one that has got generated.
2. We also can set the username and password using spring configuration in application.properties as follows:
   spring.security.user.name=${SECURITY_USERNAME:sarosahu3}
   spring.security.user.password=${SECURITY_PASSWORD:98765}

   When you run the application, you need to enter the above user credentials. This is called static credentials setting.
   Note: In this case the password will not be generated as in the first step (1)
3. Currently there is no use of config/ProjectConfig.java, model/*User.java it won't work now.
   I just copied it from the book. We will definitely look into it in different project under spring-security parent project.
4. 