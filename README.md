# Spring Boot Tutorial

아래 가이드를 참고해서 진행했다.

https://spring.io/guides/gs/spring-boot#scratch

**1. 링크를 클릭해서 코드를 생성하고 다운 받는다.**

https://start.spring.io/#!type=maven-project&language=java&packaging=jar&jvmVersion=17&groupId=com.example&artifactId=spring-boot&name=spring-boot&description=Demo%20project%20for%20Spring%20Boot&packageName=com.example.spring-boot&dependencies=web

**2. HelloController.java를 추가한다.**

```java
package com.example.spring_boot;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

    @GetMapping("/")
    public String index() {
        return "Greetings from Spring Boot!";
    }

}
```

아래 경로에 추가한다.

src/main/java/com/example/spring_boot/HelloController.java

**3. Maven을 사용한다면 다음 명령어를 입력해서 서버를 실행한다.**

```sh
./mvnw spring-boot:run
```

[http://localhost:8080](http://localhost:8080)에서 접근할 수 있다.
