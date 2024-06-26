# 자바 유용한 메서드 모음

01. [**`String`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/01.%20String.md): 문자열을 표현하고 조작할 때 사용. 불변 객체로, 문자열 연산 시 새로운 객체를 생성함.

02. [**`StringBuilder`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/02.%20StringBuilder.md): 가변 문자열을 다룰 때 사용. 문자열 결합이 빈번할 때 유용. 불변성을 가지지 않음.

03. [**`StringBuffer`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/03.%20StringBuffer.md): `StringBuilder`와 비슷하지만, 스레드 안전성을 제공. 동기화된 메서드를 사용하여 스레드 간에 안전하게 사용할 수 있음.

04. [**`Integer`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/04.%20Integer.md): 정수형 값(`int`)을 객체로 다룰 때 사용. 박싱과 언박싱을 통해 기본형과 객체형 간 변환이 가능.

05. [**`Double`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/05.%20Double.md): 실수형 값(`double`)을 객체로 다룰 때 사용. 박싱과 언박싱을 통해 기본형과 객체형 간 변환이 가능.

06. [**`Boolean`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/06.%20Boolean.md): 논리값(`boolean`)을 객체로 다룰 때 사용. 박싱과 언박싱을 통해 기본형과 객체형 간 변환이 가능.

07. [**`ArrayList`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/07.%20ArrayList.md): 동적 배열을 구현한 리스트. 크기가 자동으로 조절되며, 인덱스를 통해 요소에 접근 가능.

08. [**`HashMap`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/08.%20HashMap.md): 키-값 쌍을 저장하는 해시 테이블. 빠른 검색, 삽입, 삭제를 제공.

09. [**`HashSet`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/09.%20HashSet.md): 중복을 허용하지 않는 집합. 요소의 유일성을 보장하며, 빠른 검색과 삽입을 제공.

10. [**`LinkedList`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/10.%20LinkedList.md): 링크드 리스트 자료구조. 요소의 삽입과 삭제가 빠르며, 양방향 연결리스트로 구현됨.

11. [**`Collections`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/11.%20Collections.md): 컬렉션 조작에 유용한 메서드 모음. 정렬, 검색, 채우기, 복사 등 다양한 작업을 지원.

12. [**`Arrays`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/12.%20Arrays.md): 배열 조작에 유용한 메서드 모음. 배열의 정렬, 검색, 복사 등을 지원.

13. [**`Date`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/13.%20Date.md): 날짜와 시간을 다룰 때 사용. 오래된 API로, `Calendar`나 `LocalDate`를 더 자주 사용함.

14. [**`Calendar`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/14.%20Calendar.md): 날짜와 시간 조작을 더 편리하게 도와줌. 여러 날짜 필드를 다룰 수 있음.

15. [**`LocalDate`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/15.%20LocalDate.md): Java 8부터 추가된 클래스로, 날짜를 다룸. 불변 객체로, 시간 정보 없이 날짜만 표현.

16. [**`LocalTime`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/16.%20LocalTime.md): Java 8부터 추가된 클래스로, 시간을 다룸. 불변 객체로, 날짜 정보 없이 시간만 표현.

17. [**`LocalDateTime`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/17.%20LocalDateTime.md): Java 8부터 추가된 클래스로, 날짜와 시간을 다룸. 불변 객체로, 날짜와 시간을 모두 표현.

18. [**`Math`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/18.%20Math.md): 수학 연산에 유용한 메서드 모음. 다양한 수학 함수와 상수를 제공.

19. [**`Random`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/19.%20Random.md): 난수 생성을 위한 클래스. 다양한 타입의 난수를 생성할 수 있음.

20. [**`Scanner`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/20.%20Scanner.md): 콘솔 입력을 처리할 때 사용. 파일, 문자열 등 다양한 입력 소스로부터 데이터를 읽어올 수 있음.

21. [**`File`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/21.%20File.md): 파일과 디렉터리 경로를 표현하고 조작. 파일의 생성, 삭제, 정보 읽기 등을 지원.

22. [**`BufferedReader`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/22.%20BufferedReader.md): 문자 입력 스트림에서 텍스트를 읽기 위해 사용. 버퍼링을 통해 효율적인 읽기 작업을 지원.

23. [**`BufferedWriter`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/23.%20BufferedWriter.md): 문자 출력 스트림에 텍스트를 쓰기 위해 사용. 버퍼링을 통해 효율적인 쓰기 작업을 지원.

24. [**`InputStream`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/24.%20InputStream.md): 바이트 입력 스트림의 최상위 클래스. 다양한 입력 소스로부터 바이트를 읽어옴.

25. [**`OutputStream`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/25.%20OutputStream.md): 바이트 출력 스트림의 최상위 클래스. 다양한 출력 대상으로 바이트를 씀.

26. [**`Object`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/26.%20Object.md): 모든 클래스의 최상위 클래스. 모든 객체가 상속받는 기본 클래스.

27. [**`System`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/27.%20System.md): 시스템 관련 기능을 제공. 표준 입력, 출력, 오류 스트림과 시스템 속성, 환경 변수 등을 다룸.

28. [**`Exception`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/28.%20Exception.md): 예외 처리를 위한 기본 클래스. 다양한 예외 상황을 표현하고 처리할 수 있음.

29. [**`Statement`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/29.%20Statement.md): SQL 쿼리를 실행할 때 사용하는 인터페이스. PreparedStatement와 달리 쿼리 파라미터를 직접 설정할 수 없지만, 단순한 쿼리 실행에는 유용함.

30. [**`CallableStatement`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/30.%20CallableStatement.md): 저장 프로시저를 호출할 때 사용하는 인터페이스. 복잡한 로직을 데이터베이스에 캡슐화하여 호출할 수 있음.

31. [**`DatabaseMetaData`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/31.%20DatabaseMetaData.md): 데이터베이스의 메타데이터를 제공하는 인터페이스. 데이터베이스에 대한 정보(예: 테이블 목록, 컬럼 정보)를 얻을 수 있음.

32. [**`ResultSetMetaData`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/32.%20ResultSetMetaData.md): ResultSet의 메타데이터를 제공하는 인터페이스임. 결과 집합의 컬럼 정보(예: 컬럼 이름, 타입)를 얻을 수 있음.

33. [**`DataSource`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/33.%20DataSource.md): 데이터베이스 연결 풀링을 관리하는 인터페이스. JNDI를 통해 데이터베이스 연결을 설정하고 관리

34. [**`PreparedStatement`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/34.%20PreparedStatement.md): Java JDBC API에서 SQL 쿼리를 안전하고 효율적으로 실행하기 위한 중요한 도구. 미리 컴파일된 SQL 문을 사용하여 성능을 향상시키고, 파라미터화를 통해 SQL 인젝션 공격을 방지

35. [**`ResultSet`**](https://github.com/cherrycoder9/syntax-archive/blob/main/Java/Method/35.%20ResultSet.md): Java JDBC API에서 데이터베이스 쿼리 결과를 표현하고 처리하는 핵심 컴포넌트. 커서 기반의 결과 집합 탐색, 다양한 데이터 타입 지원, 스크롤 가능성, 그리고 동시성 옵션을 제공
