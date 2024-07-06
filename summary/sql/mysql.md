# MySQL 필수 명령문 요약

## 데이터베이스 관리

1. 데이터베이스 생성:

   ```sql
   CREATE DATABASE database_name;
   ```

2. 데이터베이스 선택:

   ```sql
   USE database_name;
   ```

## 테이블 관리

1. 테이블 생성:

   ```sql
   CREATE TABLE table_name (
       column1 datatype,
       column2 datatype,
       ...
   );
   ```

2. 테이블 삭제:

   ```sql
   DROP TABLE table_name;
   ```

## 데이터 조작 (DML)

1. 데이터 삽입:

   ```sql
   INSERT INTO table_name (column1, column2, ...)
   VALUES (value1, value2, ...);
   ```

2. 데이터 조회:

   ```sql
   SELECT column1, column2, ...
   FROM table_name
   WHERE condition;
   ```

3. 데이터 수정:

   ```sql
   UPDATE table_name
   SET column1 = value1, column2 = value2, ...
   WHERE condition;
   ```

4. 데이터 삭제:

   ```sql
   DELETE FROM table_name
   WHERE condition;
   ```

## 조건 및 정렬

1. 정렬:

   ```sql
   SELECT column1, column2, ...
   FROM table_name
   ORDER BY column1 [ASC|DESC], column2 [ASC|DESC];
   ```

## 집계 함수

- COUNT, SUM, AVG, MAX, MIN 사용 예:

  ```sql
  SELECT COUNT(column_name)
  FROM table_name
  WHERE condition;
  ```

## JOIN

1. INNER JOIN:

   ```sql
   SELECT columns
   FROM table1
   INNER JOIN table2
   ON table1.column = table2.column;
   ```

2. LEFT JOIN:

   ```sql
   SELECT columns
   FROM table1
   LEFT JOIN table2
   ON table1.column = table2.column;
   ```

3. RIGHT JOIN:

   ```sql
   SELECT columns
   FROM table1
   RIGHT JOIN table2
   ON table1.column = table2.column;
   ```

## 인덱스

1. 인덱스 생성:

   ```sql
   CREATE INDEX index_name
   ON table_name (column1, column2, ...);
   ```

2. 인덱스 삭제:

   ```sql
   DROP INDEX index_name
   ON table_name;
   ```

## 트랜잭션

1. 트랜잭션 시작:

   ```sql
   START TRANSACTION;
   ```

2. 커밋:

   ```sql
   COMMIT;
   ```

3. 롤백:

   ```sql
   ROLLBACK;
   ```
