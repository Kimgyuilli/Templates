# 🌱 Spring Boot 기본 Setup 가이드

Spring Boot 프로젝트를 처음 시작할 때 필요한 필수 세팅을 단계별로 정리한 가이드입니다.  
Spring Initializr를 통한 프로젝트 생성부터 의존성 설정, DB 연동, 그리고 `application.yml` 구성까지 설명합니다.

---
## 1. 프로젝트 생성 (Spring Initializr)

[https://start.spring.io](https://start.spring.io) 에 접속하여 아래와 같이 설정 후 프로젝트를 생성합니다.

- **Project**: Gradle - Groovy
- **Language**: Java
- **Spring Boot**: 최신 안정화 버전 (예: 3.x.x)
- **Group**: com.example
- **Artifact**: demo
- **Packaging**: Jar
- **Java**: 17 이상 권장

---

## 📦 Dependency 설정 (Gradle)

아래는 가장 많이 사용하는 Spring Boot 의존성 조합입니다. 필요한 부분만 복사해서 사용하세요.

| 분류            | 의존성 (Gradle) |
|---------------|-----------------|
| 필수            | spring-boot-starter, spring-boot-starter-web |
| JPA           | spring-boot-starter-data-jpa |
| Validation    | spring-boot-starter-validation 또는 hibernate-validator |
| swagger 문서화   | springdoc-openapi-starter-webmvc-ui |
| View 템플릿      | spring-boot-starter-thymeleaf |
| DB 드라이버       | H2, MySQL, PostgreSQL 중 택 1 |
| Lombok        | lombok + annotationProcessor |
| DevTools (선택) | spring-boot-devtools |
| 테스트           | spring-boot-starter-test, junit-platform-launcher |


<details>
<summary>✅ 예시 1 – Web + JPA + PostgreSQL + Lombok</summary> 

```
dependencies {
implementation 'org.springframework.boot:spring-boot-starter-data-jpa'  
implementation 'org.springframework.boot:spring-boot-starter-web'  
implementation 'org.springdoc:springdoc-openapi-starter-webmvc-ui:2.8.6'  
implementation 'org.springframework.boot:spring-boot-starter-validation'

    compileOnly 'org.projectlombok:lombok'  
    annotationProcessor 'org.projectlombok:lombok'  
    runtimeOnly 'org.postgresql:postgresql'  

    testImplementation 'org.springframework.boot:spring-boot-starter-test'  
    testRuntimeOnly 'org.junit.platform:junit-platform-launcher'  
}
```
</details>

<details>
<summary>✅ 예시 2 – Web + JPA + Thymeleaf + PostgreSQL + DevTools</summary>

```
dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-data-jpa'  
    implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'  
    implementation 'org.springframework.boot:spring-boot-starter-web'

    implementation 'org.springdoc:springdoc-openapi-starter-webmvc-ui:2.8.6'  
    implementation 'org.hibernate.validator:hibernate-validator'  

    compileOnly 'org.projectlombok:lombok'  
    annotationProcessor 'org.projectlombok:lombok'  
    runtimeOnly 'org.postgresql:postgresql'  

    developmentOnly 'org.springframework.boot:spring-boot-devtools'  

    testImplementation 'org.springframework.boot:spring-boot-starter-test'  
}
```
</details>

---

## ⚙️ application.yml 설정

<details>
<summary>🟦 H2 설정</summary>

```yaml
spring:
  datasource:
    url: jdbc:h2:mem:testdb
    driver-class-name: org.h2.Driver
    username: sa
    password:

  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
    properties:
      hibernate:
        format_sql: true
    database-platform: org.hibernate.dialect.H2Dialect

# H2 Console (선택)
server:
  port: 8080

spring:
  h2:
    console:
      enabled: true
      path: /h2-console
```

</details>

<details>
<summary>🟨 MySQL 설정</summary>

```
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/your_db_name?useSSL=false&serverTimezone=Asia/Seoul&characterEncoding=UTF-8
    driver-class-name: com.mysql.cj.jdbc.Driver
    username: your_username
    password: your_password

  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
    properties:
      hibernate:
        format_sql: true
    database-platform: org.hibernate.dialect.MySQL8Dialect
```
</details>

<details>
<summary>🟩 PostgreSQL 설정</summary>

```
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/your_db_name
    driver-class-name: org.postgresql.Driver
    username: your_username
    password: your_password

  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
    properties:
      hibernate:
        format_sql: true
    database-platform: org.hibernate.dialect.PostgreSQLDialect
```

</details>


## ✅ ddl-auto 옵션 설명
```
옵션 | 설명
none | 변경하지 않음 (운영 환경 추천)
validate | DB와 Entity 일치 여부 확인
update | 변경된 Entity로 테이블 자동 수정 (개발 중 추천)
create | 매번 테이블 재생성
create-drop | 애플리케이션 종료 시 테이블 삭제
```
