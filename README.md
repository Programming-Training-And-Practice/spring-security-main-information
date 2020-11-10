# Spring Security.





## Contents at a Glance.
* [About](#about)
* [Documentation.](#documentation)
* [HTTP Basic Authentication.](http-basic-authentication.md)
* [Spring Security Description.](#spring-security-description)
* [Application Security Key Terms.](#application-security-key-terms)
* [Authentication Providers.](#authentication-providers)
* [Password Storage.](#password-storage)
* [Spring Security Modules.](#spring-security-modules)
* [Spring Security for Common Vulnerabilities.](#spring-security-for-common-vulnerabilities)
* [Spring Security XXS Prevention.](#spring-security-xxs-prevention)
* [Help](#help)





## About.





## Documentation.





## Spring Security Description:
* Spring Security focuses on Application Security
* Spring Security does not address other levels of security
* Application Security focuses on who can do what within the context of an application
* Spring Security provides:
  * Protection from common security exploits
  * Integration with external security products, such as LDAP
  * Provides utilities for password encoding





## Application Security Key Terms:
* Identity - A unique actor, typically an individual aka user
* Credentials - Usually a user id and password
* Authentication - Is how the application verifies the identity of the requestor
* Spring Security has a variety of methods for Authentication
* Typically the user provides credentials, which are validated
* Authorization - Can a user perform an action?
* Using the user’s identity, Spring Security determines if they are authorized to perform action





## Authentication Providers:
* Authentication Providers - Verify users identities
* Authentication Providers supported by Spring Security:
  * In Memory 
  * JDBC/Database
  * Custom 
  * LDAP/Active Directory 
  * Keycloak
  * ACL (Access Control List)
  * OpenID
  * CAS





## Password Storage:
* Spring Security supports a variety of methods to store and verify passwords
  * NoOp Password Encoder - plain text, not recommended - for legacy systems
  * BCrypt - uses bcrypt password hashing
  * Argon2 - Uses Argon2 algorithm
  * Pbkdf2 - Uses PBKDF2 algorithm
  * SCrypt - Uses scrypt algorithm
  * Custom - Roll your own? Not recommended!





## Spring Security Modules:
* Core - Core modules of Spring Security
* Remoting - Only needed for support of RMI operations
* Web - Support of web applications
* Config - Provides support for XML and Java configuration
* LDAP - for integration with LDAP identity providers
* OAuth 2.0 Core - Core of OAuth 2.0 Authorization and OpenID
* OAuth 2.0 Client - Client support for OAuth 2.0 and OpenID clients
* OAuth 2.0 JOSE - Provides support for JOSE (Javascript Object Signing and Encryption)
* OAuth 2.0 Resource Server - Support for OAuth 2.0 Resource Servers
* ACL - Support for Access Control Lists
* CAS - Support for Central Authentication Service
* OpenID - Authenticate users with external OpenID server
* Test - Testing Support for Spring Security





## Spring Security for Common Vulnerabilities:
* Spring Security has built in support to address several common vulnerabilities
* Cross-site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Security HTTP Response Headers
* Variety of headers can be set to improve browser security
* Redirect to HTTPS





## Spring Security XXS Prevention:
* Header ‘X-XSS-Protection’ is set to ‘1; mode=block’
  * Tells browser to to block XSS code when detected
  * Modern Browsers are starting to deprecate this in favor of Content Security Policy (CSP)
* Content Security Policy - Spring Security does not implement a default value
  * Spring Security can easily be configured
  * Refer to OWASP for best practices
    * Link to OWASP recommendations in lesson resources





## Help.
