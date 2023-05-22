# Spring Security Zero to Master along with JWT,OAUTH2

[![Image](https://udemy-image-web-upload.s3.amazonaws.com:443/redactor/raw/article_lecture/2022-08-02_02-29-54-2dd92a5c40a42ff2f67d0441d21e1bff.png "Spring Security Zero to Master along with JWT,OAUTH2")](https://www.udemy.com/course/spring-security-zero-to-master/?referralCode=87DD08821FF0A3685D1C)

'Spring Security Zero to Master' course will help in understanding the Spring Security Architecture, important packages, interfaces, classes inside it which handles authentication and authorization requests in the web applications. It also covers most common security related topics like CORs, CSRF, JWT, OAUTH2, password management, method level security, user, roles & authorities management inside web applications.

## Topics covered in the course

* Spring Security framework details and it features
* How to adapt security for a Java web application using Spring Security
* Password Management in Spring Security with PasswordEncoders
* Deep dive about encoding, encryption and hashing
* What is CSRF, CORS and how to address them
* What is Authentication and Authorization. How they are different from each other.
* Securing endpoint URLs inside web applications using Ant, MVC & Regex Matchers
* Filters in Spring Security and how to write own custom filters
* Deep dive about JWT (JSON Web Tokens) and the role of them inside Authentication & Authorization
* Deep dive about OAUTH2 and various grant type flows inside OAUTH2.
* Deep dive about OpenID Connect & how it is related to OAUTH2
* Applying authorization rules using roles, authorities inside a web application using Spring Security
* Method level security in web/non-web applications
* Social Login integrations into web applications
* Set up of Authorization Server using KeyCloak 

## Pre-requisite for the course
- Good understanding on Java and Spring concepts
- Basic understanding on SpringBoot & REST services is a bonus but not mandatory
- Interest to learn and explore about Spring Security

# Important Links

- Spring website to generate projects - https://start.spring.io/
- Spring Website - https://spring.io/
- Spring Projects website - https://spring.io/projects
- Spring Boot properties - https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html
- AWS website - https://aws.amazon.com/
- SQLECTRON website - https://sqlectron.github.io
- Free MySQL DB website - https://www.freemysqlhosting.net
- OAuth2 Website - https://oauth.net/2/
- OAuth2 playground - https://www.oauth.com/playground/
- KeyCloak website - https://www.keycloak.org
- KeyCloak Download page - https://www.keycloak.org/downloads
- KeyCloak setup - https://www.keycloak.org/getting-started/getting-started-zip
- KeyCloak guides - https://www.keycloak.org/guides
- KeyCloak Well known APIs - http://localhost:8180/realms/eazybankdev/.well-known/openid-configuration
- Angular Keycloak library - https://www.npmjs.com/package/keycloak-angular
- Keycloak official documentation - https://www.keycloak.org/documentation
- Keycloak Admin REST APIs - https://www.keycloak.org/docs-api/19.0.2/rest-api/index.html

# Sections: 

- ch1 -> 9,10,11,12 internals of spring security
- ch2 -> 17 explains about enabling authentication to individual requests
     * defaultSecurityFilterChain
- ch3 -> 23 explains about using password encoder and in-memory storing of user details
- ch4 & 5 Password management and encoders, Authentication providers
- ch6 57, enable cors -> cross orgin resource sharing
- ch6 59 csrf/xsrf -> cross site request forgery
- ch7  Authority and Roles.
- ch8 74, pdf has inbuilt security filters.
- ch8 adding filters uisng addFilter*(), GenericFilterBean, OncePerRequestFilter
- ch9 adding filters for token validators and generators
- ch10 method level security @Preauthorize, @PostAuthorize, @PreFilter, @PostFilter
- ch11 Oauth terminologies
   - Grant Flows  
     * Authorization code (initial code which is then used for pkce)
     * PKCE (client & server)
     * CLient Credentials(server & server)
     * Device code(apple devices etc)
     * Refresh Token 
     * Implicit grant flow(both code and pkce together, not secure deprecated)
     * 102 06:00, what details to be passed for pcke flow
   - OAuth 
     * resource owner(end user)
     * client(app, browser, postapp)
     * Authorization server(knows the resource owner(keycloak))
     * Resource server(other micro services to access data)
     * Scopes(permissions to access the data from resources(roles)) 
   
