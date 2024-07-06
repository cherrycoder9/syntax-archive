# JDBC와 스프링 부트: 핵심 개념 및 활용

## JDBC 기본 개념

### 1. 핵심 구성 요소

- **DriverManager**: 데이터베이스 드라이버 관리 및 연결 생성
- **Connection**: 데이터베이스와의 연결 표현
- **Statement/PreparedStatement**: SQL 쿼리 실행 객체
- **ResultSet**: 쿼리 실행 결과 저장 객체

### 2. 기본 사용 흐름

1. 드라이버 로드
2. 데이터베이스 연결 생성
3. SQL 쿼리 실행
4. 결과 처리
5. 자원 해제

## 스프링 부트의 JDBC 지원

### 1. 자동 설정

- `application.properties` 또는 `application.yml`을 통한 DataSource 자동 구성

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/mydb
spring.datasource.username=user
spring.datasource.password=password
```

### 2. JdbcTemplate

- JDBC 작업을 간소화하는 유틸리티 클래스

```java
@Autowired
private JdbcTemplate jdbcTemplate;

public List<User> findAllUsers() {
    return jdbcTemplate.query("SELECT * FROM users", 
        (rs, rowNum) -> new User(rs.getLong("id"), rs.getString("name")));
}
```

### 3. 연결 풀링

- HikariCP 등의 고성능 연결 풀 자동 설정

### 4. 트랜잭션 관리

- 선언적 트랜잭션 관리 지원

```java
@Transactional
public void transferMoney(long fromId, long toId, BigDecimal amount) {
    // 트랜잭션 로직
}
```

## JDBC와 ORM

### 1. JPA 통합

- 객체 지향적 데이터베이스 접근

```java
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;
    // getters and setters
}
```

### 2. 스프링 데이터 JPA

- 리포지토리 인터페이스만으로 데이터 액세스 계층 구현

```java
public interface UserRepository extends JpaRepository<User, Long> {
    List<User> findByName(String name);
}
```

## 보안 및 테스트

### 1. 스프링 시큐리티 통합

- 데이터베이스 기반 인증 및 권한 부여

### 2. 테스트 지원

- 슬라이스 테스트를 통한 데이터 액세스 계층 테스트

```java
@DataJpaTest
class UserRepositoryTest {
    @Autowired
    private UserRepository userRepository;

    @Test
    void testFindByName() {
        // 테스트 로직
    }
}
```

## 고급 기능

### 1. 데이터베이스 마이그레이션

- Flyway, Liquibase 등의 도구와 쉽게 통합

### 2. 모니터링 및 관리

- 스프링 부트 액추에이터를 통한 데이터베이스 연결 상태 및 성능 모니터링

## 결론

스프링 부트는 JDBC의 복잡성을 추상화하여 개발 생산성을 높이지만, JDBC의 기본 개념 이해는 여전히 중요합니다. 특히 성능 최적화나 복잡한 쿼리 처리 시 JDBC의 저수준 지식이 필요할 수 있습니다. 또한, JPA나 다른 ORM 사용 시에도 JDBC 이해는 문제 해결과 성능 튜닝에 도움이 됩니다.

개발자는 JDBC의 기본을 숙지하고 스프링 부트의 추상화 계층을 효과적으로 활용하여 견고하고 효율적인 데이터 액세스 계층을 구현해야 합니다.
