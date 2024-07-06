# 스프링 프레임워크 핵심 문법 및 개념 요약

## 1. 핵심 어노테이션

### 클래스 레벨

- `@Component`: 일반적인 스프링 관리 컴포넌트
- `@Service`: 비즈니스 로직을 담당하는 서비스 클래스
- `@Repository`: 데이터 액세스 객체(DAO) 클래스
- `@Controller`: 웹 MVC 컨트롤러
- `@RestController`: RESTful 웹 서비스 컨트롤러
- `@Configuration`: 설정 클래스
- `@SpringBootApplication`: 스프링 부트 애플리케이션의 시작점

### 메서드 및 필드 레벨

- `@Autowired`: 의존성 주입
- `@Value`: 외부 설정 값 주입
- `@Bean`: 빈 생성 메서드
- `@RequestMapping`: HTTP 요청 매핑
- `@GetMapping`, `@PostMapping`, `@PutMapping`, `@DeleteMapping`: HTTP 메서드별 매핑
- `@Transactional`: 트랜잭션 관리

## 2. IoC (Inversion of Control) 및 DI (Dependency Injection)

```java
@Service
public class MyService {
    private final MyRepository myRepository;

    @Autowired
    public MyService(MyRepository myRepository) {
        this.myRepository = myRepository;
    }
}
```

## 3. AOP (Aspect-Oriented Programming)

```java
@Aspect
@Component
public class LoggingAspect {
    @Before("execution(* com.example.service.*.*(..))")
    public void logBefore(JoinPoint joinPoint) {
        // 메서드 실행 전 로깅
    }
}
```

## 4. 스프링 MVC

```java
@Controller
public class MyController {
    @GetMapping("/hello")
    public String hello(Model model) {
        model.addAttribute("message", "Hello, World!");
        return "hello";
    }
}
```

## 5. 데이터 접근 (ORM 및 Spring Data)

```java
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;
}

@Repository
public interface UserRepository extends JpaRepository<User, Long> {
    List<User> findByName(String name);
}
```

## 6. 트랜잭션 관리

```java
@Service
public class UserService {
    @Transactional
    public void createUser(User user) {
        // 사용자 생성 로직
    }
}
```

## 7. 스프링 시큐리티

```java
@Configuration
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {
    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http.authorizeRequests()
            .antMatchers("/public/**").permitAll()
            .anyRequest().authenticated()
            .and()
            .formLogin();
    }
}
```

## 8. 테스트

```java
@SpringBootTest
class MyServiceTest {
    @Autowired
    private MyService myService;

    @Test
    void testMyService() {
        // 테스트 로직
    }
}
```

## 9. 설정 및 프로파일

```properties
# application.properties
spring.profiles.active=dev

# application-dev.properties
server.port=8080
```

## 10. 예외 처리

```java
@ControllerAdvice
public class GlobalExceptionHandler {
    @ExceptionHandler(ResourceNotFoundException.class)
    public ResponseEntity<String> handleResourceNotFound(ResourceNotFoundException ex) {
        return ResponseEntity.status(HttpStatus.NOT_FOUND).body(ex.getMessage());
    }
}
```
