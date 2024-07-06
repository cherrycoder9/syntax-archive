# JSP 핵심 개념 및 스프링부트와의 관계

## JSP 개요

JavaServer Pages(JSP)는 동적 웹 페이지 생성을 위한 서버 사이드 기술입니다. HTML 내에 자바 코드를 삽입할 수 있어, 서버 측 로직과 프레젠테이션을 쉽게 결합할 수 있습니다.

## 주요 스크립트 요소

- **스크립틀릿**: `<% %>` - 자바 코드 삽입
- **표현식**: `<%= %>` - 값 출력
- **선언부**: `<%! %>` - 메서드나 변수 선언

이 요소들은 JSP의 핵심이지만, 과도한 사용은 코드의 가독성을 해칠 수 있습니다.

## EL과 JSTL

- **Expression Language (EL)**: `${}` 문법으로 자바 객체의 속성에 쉽게 접근
- **JSP Standard Tag Library (JSTL)**: 반복문, 조건문 등을 태그 형태로 제공

EL과 JSTL의 도입으로 JSP 페이지의 가독성과 유지보수성이 크게 향상되었습니다.

## JSP와 서블릿의 관계

JSP 파일은 첫 요청 시 서블릿으로 변환되어 컴파일됩니다. 이는 초기 로딩 시간을 증가시키지만, 이후 요청에서는 빠른 응답 시간을 제공합니다.

## MVC 패턴에서의 JSP

모델 2 아키텍처(MVC 패턴의 일종)에서 JSP는 주로 뷰 역할을 담당합니다:

1. 컨트롤러(서블릿)가 비즈니스 로직 처리
2. 결과를 모델에 저장
3. JSP에서 모델 데이터를 사용하여 최종 HTML 생성

이 구조는 관심사의 분리를 통해 대규모 애플리케이션 개발에 적합합니다.

## 스프링부트에서의 JSP 사용

스프링부트에서 JSP를 사용하려면 추가 설정이 필요합니다:

1. `application.properties`에 뷰 리졸버 설정 추가
2. 컨트롤러에서 뷰 이름 반환
3. WAR 패키징 사용 (JSP는 기본 JAR 패키징과 호환되지 않음)

## JSP vs 현대적 템플릿 엔진

개인적으로, 새 프로젝트에는 JSP 대신 Thymeleaf를 추천합니다:

- 내추럴 템플릿 방식으로 디자이너-개발자 협업 용이
- 스프링과의 통합이 우수
- JAR 패키징 호환으로 마이크로서비스 아키텍처에 적합

그러나 JSP 이해는 여전히 중요합니다:

- 레거시 시스템 유지보수에 필요
- 다른 템플릿 엔진 학습에 도움
- 웹 개발의 기본 원리 이해에 유용

결론적으로, 기술 선택은 프로젝트 요구사항과 팀 경험을 고려해야 합니다. JSP는 여전히 가치 있는 기술이지만, 현대적인 대안들도 충분히 고려해볼 만합니다.