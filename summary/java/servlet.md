# 스프링부트를 위한 서블릿 핵심 개념

## 1. 서블릿과 서블릿 컨테이너

- 서블릿: HTTP 요청을 처리하는 자바 기반의 서버 측 프로그램
- 서블릿 컨테이너: 서블릿의 생명주기 관리, 요청 전달, 응답 반환
- 대표적인 서블릿 컨테이너: 톰캣(Tomcat), 제티(Jetty), 언더토우(Undertow)

## 2. 서블릿 라이프사이클

- 초기화 (init): 서블릿 인스턴스 생성 시 호출
- 서비스 (service): 클라이언트 요청마다 호출, doGet, doPost 등의 메서드로 처리
- 종료 (destroy): 서블릿 종료 시 호출, 자원 해제

## 3. 요청 및 응답 처리

- HttpServletRequest: 클라이언트 요청 정보 접근
- HttpServletResponse: 서버 응답 생성
- 요청 파라미터 처리, 응답 생성 방법

## 4. 서블릿 매핑

- URL 패턴에 따른 서블릿 매핑
- web.xml 파일 또는 @WebServlet 어노테이션 사용

## 5. 세션 관리

- HttpSession 인터페이스를 사용한 세션 생성, 속성 설정, 조회, 무효화
- 쿠키 생성, 설정, 읽기

## 6. 필터

- 요청과 응답을 가로채서 처리하는 프로그램
- 인증, 로깅, 인코딩 처리 등에 사용
- Filter 인터페이스 구현

## 7. 리스너

- 특정 이벤트(서블릿 컨텍스트 초기화, 세션 생성/소멸 등) 감지 및 처리
- ServletContextListener, HttpSessionListener 등 구현

## 8. 예외 처리

- 서블릿에서의 예외 처리 방법
- web.xml에 예외 처리 설정, @ExceptionHandler 어노테이션 사용

## 9. JSP와의 연동

- 서블릿과 JSP의 역할 분담
- 서블릿에서 JSP로 포워딩, JSP에서 서블릿으로 요청 전달

## 10. 비동기 처리

- 서블릿 3.0 이상에서 지원되는 비동기 처리 기능
- AsyncContext를 사용한 비동기 요청 처리

## 11. 멀티파트 요청 처리

- 파일 업로드 등의 멀티파트 요청 처리
- @MultipartConfig 어노테이션, Part 인터페이스 사용

## 스프링부트와의 연관성

- 스프링 MVC는 DispatcherServlet을 통해 모든 HTTP 요청 처리
- 스프링의 HandlerInterceptor는 서블릿 필터와 유사한 기능 제공
- 스프링부트는 서블릿 컨테이너를 내장하여 실행
