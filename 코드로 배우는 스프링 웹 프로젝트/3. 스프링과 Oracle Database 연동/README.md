# 3.1) 오라클 설치 (m1)

-   https://shanepark.tistory.com/400
-   docker run --name oracle -p 1521:1521 -e ORACLE_USER=admin ORACLE_PASSWORD=1234 -d gvenzl/oracle-xe

# 3.2) SQL Developer 설치 (73p)

# 3.3) 프로젝트의 JDBC 연결 (m1) (78p)

-   https://velog.io/@zinhoxxl/Apple-Silicon-M1-%EC%9C%BC%EB%A1%9C-oracleeclipse-%EC%97%B0%EB%8F%99%ED%95%98%EA%B8%B0-
-   https://parkpurong.tistory.com/128

# 3.4) 커넥션 풀 설정

## DB Connection

-   DB를 사용하기 위해 DB와 애플리케이션 간 통신을 할 수 있는 수단
-   Java에서는 주로 JDBC를 이용

## JDBC

-   Java Database Connectivity
-   DBMS 종류에 상관없이 하나의 JDBC API를 사용해서 데이터베이스 작업을 처리할 수 있게 해줌
-   DataSource : Connection Pool을 관리

## Connection Pool

-   WAS가 실행되면서 일정량의 Connection 객체를 미리 만들어서 pool에 저장했다가, 클라이언트의 요청이 오면 Connection 객체를 빌려주고 해당 객체의 임무가 완료되면 다시 Connection 객체를 반납 받아서 Pool에 저장하는 프로그래밍 기법
-   Java에서는 DataSource 라는 인터페이스를 통해서 Connection Pool을 사용

## 라이브러리 추가와 DataSource 설정

-   root-context.xml은 주로 이미 만들어진 클래스들을 이용해서 스프링의 빈으로 등록할때 사용
-   일반적인 상황에서는 어노테이션을 이용

### log4jdbc.log4j2 관련 에러 해결

-   https://kimvampa.tistory.com/63

### sqlSessionFactory 빈 생성시 오류

-   https://cceeun.tistory.com/83
