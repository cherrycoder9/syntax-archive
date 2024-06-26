# 자바 유용한 메서드 모음

1. **`String`**: 문자열을 표현하고 조작할 때 사용. 불변 객체로, 문자열 연산 시 새로운 객체를 생성함.
2. **`StringBuilder`**: 가변 문자열을 다룰 때 사용. 문자열 결합이 빈번할 때 유용. 불변성을 가지지 않음.
3. **`StringBuffer`**: `StringBuilder`와 비슷하지만, 스레드 안전성을 제공. 동기화된 메서드를 사용하여 스레드 간에 안전하게 사용할 수 있음.
4. **`Integer`**: 정수형 값(`int`)을 객체로 다룰 때 사용. 박싱과 언박싱을 통해 기본형과 객체형 간 변환이 가능.
5. **`Double`**: 실수형 값(`double`)을 객체로 다룰 때 사용. 박싱과 언박싱을 통해 기본형과 객체형 간 변환이 가능.
6. **`Boolean`**: 논리값(`boolean`)을 객체로 다룰 때 사용. 박싱과 언박싱을 통해 기본형과 객체형 간 변환이 가능.
7. **`ArrayList`**: 동적 배열을 구현한 리스트. 크기가 자동으로 조절되며, 인덱스를 통해 요소에 접근 가능.
8. **`HashMap`**: 키-값 쌍을 저장하는 해시 테이블. 빠른 검색, 삽입, 삭제를 제공.
9. **`HashSet`**: 중복을 허용하지 않는 집합. 요소의 유일성을 보장하며, 빠른 검색과 삽입을 제공.
10. **`LinkedList`**: 링크드 리스트 자료구조. 요소의 삽입과 삭제가 빠르며, 양방향 연결리스트로 구현됨.
11. **`Collections`**: 컬렉션 조작에 유용한 메서드 모음. 정렬, 검색, 채우기, 복사 등 다양한 작업을 지원.
12. **`Arrays`**: 배열 조작에 유용한 메서드 모음. 배열의 정렬, 검색, 복사 등을 지원.
13. **`Date`**: 날짜와 시간을 다룰 때 사용. 오래된 API로, `Calendar`나 `LocalDate`를 더 자주 사용함.
14. **`Calendar`**: 날짜와 시간 조작을 더 편리하게 도와줌. 여러 날짜 필드를 다룰 수 있음.
15. **`LocalDate`**: Java 8부터 추가된 클래스로, 날짜를 다룸. 불변 객체로, 시간 정보 없이 날짜만 표현.
16. **`LocalTime`**: Java 8부터 추가된 클래스로, 시간을 다룸. 불변 객체로, 날짜 정보 없이 시간만 표현.
17. **`LocalDateTime`**: Java 8부터 추가된 클래스로, 날짜와 시간을 다룸. 불변 객체로, 날짜와 시간을 모두 표현.
18. **`Math`**: 수학 연산에 유용한 메서드 모음. 다양한 수학 함수와 상수를 제공.
19. **`Random`**: 난수 생성을 위한 클래스. 다양한 타입의 난수를 생성할 수 있음.
20. **`Scanner`**: 콘솔 입력을 처리할 때 사용. 파일, 문자열 등 다양한 입력 소스로부터 데이터를 읽어올 수 있음.
21. **`File`**: 파일과 디렉터리 경로를 표현하고 조작. 파일의 생성, 삭제, 정보 읽기 등을 지원.
22. **`BufferedReader`**: 문자 입력 스트림에서 텍스트를 읽기 위해 사용. 버퍼링을 통해 효율적인 읽기 작업을 지원.
23. **`BufferedWriter`**: 문자 출력 스트림에 텍스트를 쓰기 위해 사용. 버퍼링을 통해 효율적인 쓰기 작업을 지원.
24. **`InputStream`**: 바이트 입력 스트림의 최상위 클래스. 다양한 입력 소스로부터 바이트를 읽어옴.
25. **`OutputStream`**: 바이트 출력 스트림의 최상위 클래스. 다양한 출력 대상으로 바이트를 씀.
26. **`Object`**: 모든 클래스의 최상위 클래스. 모든 객체가 상속받는 기본 클래스.
27. **`System`**: 시스템 관련 기능을 제공. 표준 입력, 출력, 오류 스트림과 시스템 속성, 환경 변수 등을 다룸.
28. **`Exception`**: 예외 처리를 위한 기본 클래스. 다양한 예외 상황을 표현하고 처리할 수 있음.