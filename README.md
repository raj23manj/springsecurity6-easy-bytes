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
     * PKCE(proof key for code exchange) (client & server)
       - for pkce client_id is optional, that is why we need to send code_challenhe & code_verifier
       - for non pkce flow, the client app(react, mob) should securely store the client secret and send it with client_id.(not recommended), coz if client_secret is leaked as it is to be stored on the js code, or use db call to securely fetch it. 
     * CLient Credentials(server & server)
     * Device code(apple devices etc)
     * Password Grant/Resource owner credentials Grant Type(not recommended if the auth server is third party, but if in house auth server this was used, but will be deperecated)
     * Refresh Token 
     * OpenID(OIDC) - used to get the idenetiy of the user. Same auth server(like keycloak) issues two tokens one for authorizations and other to access the identity details of the user apart from refresh tokens. We need to send the grnat type as `openid`. Implementing OpenId connect on top of OAuth 2.0 completes IAM(Identity access manager which gives idenetity(authentication) and authorizations). Onlu Oauth 2.0 lacks an authentication component.(109)
     * Implicit grant flow(both code and pkce together, not secure deprecated => all requests are made as get, cliend_id is exposed and returned token also passed as query param which can be accessed by hacker)
     * see Oauth playgroun url for demo, above in the links
     * 102 06:00, what details to be passed for pcke flow
     * 108, different methods to verify the token from auth server by client
       * make call to auth server via api and validate
       * the auth server and the client(microservice) has a access to common db, auth server when issuing the token adds a entry in this db, and when the client needs to verify the token, it uses the same db to check if token is present
       * use the public cert provided by the auth server(jsonweb token node)
   - OAuth 
     * resource owner(end user)
     * client(app, browser, postapp)
     * Authorization server(knows the resource owner(keycloak))
     * Resource server(other micro services to access data)
     * Scopes(permissions to access the data from resources(roles)) 
- ch13 
   * 114, keycloak/okta/forgerock/amazon cognito
   * 118 setup a keycloak resource server
   * 124 PKCE in detail


######################################################################################

# sergey: 
 
   - Resources
     Source Code
        Resource Server

        Repository: https://github.com/simplyi/ResourceServer

        Zip: https://github.com/simplyi/ResourceServer/archive/master.zip


        Albums Resource Server

        Before configuring it as Eureka Client

        Repository: https://github.com/simplyi/Albums-Resource-Server/tree/Albums-Resource-Server-Before-Eureka-Client

        Zip: https://github.com/simplyi/Albums-Resource-Server/archive/Albums-Resource-Server-Before-Eureka-Client.zip


        After Configuring Albums Resource Server as Eureka Client

        Repository: https://github.com/simplyi/Albums-Resource-Server/tree/Eureka-Client

        Zip: https://github.com/simplyi/Albums-Resource-Server/archive/Eureka-Client.zip


        Photos Resource Server

        Before configuring it as Eureka Client

        Repository: https://github.com/simplyi/Photos-Resource-Server/tree/Photos-Resource-Server-Before-Eureka-Client

        Zip: https://github.com/simplyi/Photos-Resource-Server/archive/Photos-Resource-Server-Before-Eureka-Client.zip


        After configuring it as Resource Server

        Repository: https://github.com/simplyi/Photos-Resource-Server/tree/Eureka-Client

        Zip: https://github.com/simplyi/Photos-Resource-Server/archive/Eureka-Client.zip


        API Gateway

        Repository: https://github.com/simplyi/ApiGateway

        Zip: https://github.com/simplyi/ApiGateway/archive/master.zip

        API Gateway Before CORS Configuration

        Repository: https://github.com/simplyi/ApiGateway/tree/Before-CORSE-Configuration

        Zip: https://github.com/simplyi/ApiGateway/archive/Before-CORSE-Configuration.zip


        API Gateway After CORS Configuration

        Repository: https://github.com/simplyi/ApiGateway/tree/CORS-Configuration

        Zip: https://github.com/simplyi/ApiGateway/archive/CORS-Configuration.zip


        Discovery Service

        Repository: https://github.com/simplyi/DiscoveryService

        Zip: https://github.com/simplyi/DiscoveryService/archive/master.zip


        Photo App Spring MVC Web Client Application

        Repository: https://github.com/simplyi/PhotoAppWebClient

        Zip: https://github.com/simplyi/PhotoAppWebClient/archive/master.zip


        PKCE Example

        Repository: https://github.com/simplyi/PKCE

        Zip: https://github.com/simplyi/PKCE/archive/main.zip


        Social Login/Logout

        Repository: https://github.com/simplyi/SocialLoginWebClient

        Zip: https://github.com/simplyi/SocialLoginWebClient/archive/master.zip


        The PKCE-Enhanced Authorization flow in JavaScript application

        JavaScript application

        Repository: https://github.com/simplyi/spa-example

        Zip: https://github.com/simplyi/spa-example/archive/main.zip

        API Gateway (before CORS configuration)

        Repository: https://github.com/simplyi/ApiGateway/tree/Before-CORSE-Configuration

        Zip: https://github.com/simplyi/ApiGateway/archive/Before-CORSE-Configuration.zip

        API Gateway (after CORS configuration)

        Repository: https://github.com/simplyi/ApiGateway/tree/CORS-Configuration

        Zip: https://github.com/simplyi/ApiGateway/archive/CORS-Configuration.zip


        Resource Server (before CORS configuration)

        Repository: https://github.com/simplyi/ResourceServer/tree/CORS-configuration

        Zip: https://github.com/simplyi/ResourceServer/archive/CORS-configuration.zip

        Resource Server ((after CORS configuration)

        Repository: https://github.com/simplyi/ResourceServer/tree/before-CORS-configuration

        Zip: https://github.com/simplyi/ResourceServer/archive/before-CORS-configuration.zip


        Keycloak User Storage Provider SPI

        (Remote User Authentication)

        Remote User Storage Provider Implementation

        Repository: https://github.com/simplyi/KeycloakRemoteUserStorageProvider.git

        Zip: https://github.com/simplyi/KeycloakRemoteUserStorageProvider/archive/main.zip


        Legacy Users Web Service

        Repository: https://github.com/simplyi/LegacyUsersWebService.git

        Zip: https://github.com/simplyi/LegacyUsersWebService/archive/main.zip


        The New Spring Authorization Server

        Repository: https://github.com/simplyi/NewSpringAuthorizationServer.git

        Zip: https://github.com/simplyi/NewSpringAuthorizationServer/archive/refs/heads/main.zip
        
Course: 

- Section 8 -> 63 time 4:10(all avaliable method level security)

   ![Screenshot 2023-05-26 at 7 04 51 AM](https://github.com/raj23manj/springsecurity6-easy-bytes/assets/2163592/297bd902-b1ca-4a13-9235-3c986751358b)

