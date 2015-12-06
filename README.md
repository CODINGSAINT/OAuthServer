# OAuthServer

OAuthServer is sample OAuth Server via Spring OAuth 2.0 Module. It uses

  - Spring Boot
  - Maven
  - Spring OAuth 2.0

This is just an attempt for a small instance of Spring OAuth . It uses In Memory Client .

> This is just for tutorial . We don't take any responsibility for security .

This text you see here is *actually* written in Markdown! To get a feel for Markdown's syntax, type some text into the left window and watch the results in the right.

### Version
1.0.0

### Tech


* [Spring Boot] - Spring Boot
* [Spring OAuth 2.0] -OAuth Implementation via Spring


### Installation

``` sh
git clone https://github.com/CODINGSAINT/OAuthServer.git
cd OAuthServer
mvn package
cd target
java -java OAuthServer-0.0.1-SNAPSHOT.jar
```
Open browser and go to URL
http://localhost:8080/oauth/authorize?response_type=code&client_id=myclient&redirect_uri=http://somexyzwebsite.com

##### User : user
##### Password : passworda
This will lead to browser to generate a code e.g. http://somexyzwebsite.com/?code=ssXdsD.
Here code is ssXdsD
#### Curl
```
$ curl myclient:myclientsecret@localhost:8080/oauth/token  \
-d grant_type=authorization_code -d client_id=acme     \
-d redirect_uri=http://example.com -d code=jYWioI
```

This will result in a json like 
```


    {
        "access_token": "c5ce3f0d-37b9-471f-bb36-5d68c374eddc",
        "token_type": "bearer",
        "refresh_token": "39db6645-a247-44a5-8d64-8ac52c5aa29e",
        "expires_in": 43199,
        "scope": "openid"
    }

```



  [Spring Boot]: <http://projects.spring.io/spring-boot/>
   [Spring OAuth 2.0]: <http://projects.spring.io/spring-security-oauth>