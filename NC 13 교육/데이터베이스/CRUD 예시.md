  

데이터베이스 연습으로 sakila 데이터베이스를 이용할 것이다.

  

```SQL
 		#데이터베이스에서 작업을 하기 전에는 반드시 특정 스키마를 선택해야 한다.
    #스키마를 선택할 때에는 SCHEMAS 탭에서
    #사용할 스키마 이름을 더블클릭하거나
    \#USE 스키마이름;을 입력해야한다.
    USE sakila;
    
	  #데이터베이스에서 데이터 불러오기
	  \#SELECT 컬럼이름 FROM 테이블이름
    SELECT actor_id FROM actor;
    
    #어떤 특정 컬럼만이 아니라 여러 컬럼을 보기
    \#SELECT 컬럼 이름, 컬럼이름 FROM 테이블이름
    SELECT actor_id, first_name FROM actor;
    
    #모든 컬럼 보기
    \#SELECT * FROM 테이블이름
    # * 은 All 의미
    SELECT * FROM actor;
    
    #조건에 따른 검색
    \#SELECT * FROM 테이블이름 WHERE 조건
    SELECT * FROM actor WHERE actor_id = 20;
    
    #데이터 입력
    \#INSERT INTO 테이블이름 VALUES(값)
    INSERT INTO actor Values(1080, 'Jeyung', 'CHO', NOW());
    SELECT * FROM actor WHERE actor_id = 1080;
    
    #특정 컬럼에만 값 입력
    \#INSERT INTO 테이블이름(컬럼이름1, 컬럼이름2, ...) VALUES(값1, 값2, ...);
    INSERT INTO actor(first_name, last_name) VALUES('철수', '김');
    SELECT * FROM actor WHERE first_name = '철수';
    
    #특정 데이터 값 수정
    \#UPDATE 테이블이름 SET 컬럼이름 = 새 값, 컬럼이름 = 새 값, ... WHERE 특정 조건;
    UPDATE actor 
    SET first_name = '재영',
    last_name = '조',
    last_update = NOW()
    WHERE actor_id = 1080;
    SELECT * FROM actor WHERE actor_id = 1080;
    
    #로우 삭제
    \#DELETE FROM 테이블이름 WHERE 삭제조건
    SELECT * FROM actor WHERE actor_id = 1081;
    DELETE FROM actor WHERE actor_id = 1081;
```