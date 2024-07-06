# 스프링부트 핵심 문법 및 어노테이션 요약

## 프로젝트 설정

1. **프로젝트 생성**: Spring Initializr (<https://start.spring.io/>) 사용
2. **설정 파일**: `application.properties` 또는 `application.yml`

## 주요 어노테이션

### 클래스 레벨 어노테이션

- `@SpringBootApplication`: 스프링부트 애플리케이션의 시작점
- `@RestController`: RESTful 웹 서비스 컨트롤러
- `@Service`: 서비스 계층 클래스
- `@Repository`: 데이터 액세스 객체(DAO) 클래스
- `@Configuration`: 설정 클래스
- `@Entity`: JPA 엔티티 클래스

### 메서드 및 필드 레벨 어노테이션

- `@Autowired`: 의존성 주입
- `@Value("${property}")`: 외부 설정 값 주입
- `@RequestMapping`: HTTP 요청 매핑
- `@GetMapping`, `@PostMapping`, `@PutMapping`, `@DeleteMapping`: HTTP 메서드별 매핑
- `@PathVariable`: URL 경로 변수 추출
- `@RequestParam`: 쿼리 파라미터 추출
- `@RequestBody`: HTTP 요청 본문 데이터 추출
- `@Transactional`: 트랜잭션 관리

## 컴포넌트 예시

### 컨트롤러

```java
@RestController
@RequestMapping("/api")
public class MyController {
    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, World!";
    }

    @PostMapping("/create")
    public ResponseEntity<String> createResource(@RequestBody MyResource resource) {
        // 리소스 생성 로직
        return ResponseEntity.ok("Resource created");
    }
}
```

### 서비스

```java
@Service
public class MyService {
    public String performOperation() {
        // 비즈니스 로직
        return "Operation performed";
    }
}
```

### 리포지토리

```java
@Repository
public interface MyRepository extends JpaRepository<MyEntity, Long> {
    // 커스텀 쿼리 메서드 정의 가능
}
```

### 엔티티

```java
@Entity
@Table(name = "my_table")
public class MyEntity {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;
    // Getter, Setter, Constructor
}
```

## 예외 처리

```java
@ControllerAdvice
public class GlobalExceptionHandler {
    @ExceptionHandler(ResourceNotFoundException.class)
    public ResponseEntity<String> handleResourceNotFound(ResourceNotFoundException ex) {
        return ResponseEntity.status(HttpStatus.NOT_FOUND).body(ex.getMessage());
    }
}
```

## 테스트

```java
@SpringBootTest
public class MyServiceTest {
    @Autowired
    private MyService myService;

    @Test
    public void testPerformOperation() {
        String result = myService.performOperation();
        assertEquals("Operation performed", result);
    }
}
```

## 애플리케이션 시작

```java
@SpringBootApplication
public class MySpringBootApplication {
    public static void main(String[] args) {
        SpringApplication.run(MySpringBootApplication.class, args);
    }
}
```

## 기타 유용한 설정

1. **로깅 설정**:

   ```properties
   logging.level.org.springframework=INFO
   logging.file.name=app.log
   ```

2. **프로파일**:

   ```properties
   # application-dev.properties
   spring.datasource.url=jdbc:mysql://localhost:3306/devdb
   ```
