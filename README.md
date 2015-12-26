# Spring security app using annotation

This app demonstrates Spring Security 4 usage to secure a Spring MVC web application, securing URL access with authentication. We will use classic Hello World example to learn Spring Security 4 basics. This post uses Spring Annotation based configuration for Servlet 3.0 containers [thus no web.xml] and also shows corresponding XML based Security configuration for side-by-side comparison where applicable.

# How Spring Security works ?

Spring security have AuthenticationManager and it delegate to a collection of AuthenticationProvider instances.An AuthenticationProvider will call an object that implements the UserDetailsService interface. A UserDetailsService looks up the user data and returns a UserDetails object fully populated. If the UserDetailsService cannot find this user then a UsernameNotFoundException is thrown.UserDetailsService interface has just one method loadUserByUsername(String username) and  returns a UserDetails object, then the AuthenticationProvider will check that the password matches the password the user entered. If it does not match, then the AuthenticationProvider will throw an AuthenticationException.

Steps to build and deploy this app :

1) mvn clean install

2) deploy .war file in tomcat 8.

Here is the [Blog](https://sunilkumarpblog.blogspot.in/2015/12/spring-security-4-hello-world-example.html) of this project with precise explination.
