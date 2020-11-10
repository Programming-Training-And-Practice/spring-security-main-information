# HTTP Basic Authentication.





## Contents at a Glance.
* [About](#about)
* [Documentation.](#documentation)
* [Help](#help)





## About.





## Documentation.


## Overview HTTP Basic Authentication:
* HTTP Basic Authentication is part of the HTTP Specification
  * Originally from RFC 2617, 1999, updated in RFC 7617 in 2015
* Basic Authentication provides a standard way for HTTP clients to submit user name and password
* URL Encoding - https://username:password@www.example.com
* HTTP Header - Key: Authorization, Value: Basic <Base64 encoded string>
  * String - username:password


## Criticisms of Basic Authentication:
* URL Encoding and Header Encoding are not secure
  * Trivial task to revert Base64 encoded string back to text value
* To protect user credentials, use of HTTPS is recommended
* HTTP Basic Authentication also criticized for sending user credentials in every request
  * Increases risk of compromise
  * Other methods send an authentication token in each request


## Spring Boot Spring Security Auto-Configuration:
* When Spring Boot detects Spring Security on the classpath, it will auto-configure Spring Security for HTTP Basic Authentication
  * Default User - user
    * Set Property spring.security.user.name to override
  * Default Password - Random UUID, check console output
    * Set Property spring.security.user.password to override
* All paths secured - except actuator info and health



## Help.
