# 11.1) Optional

-   NPE(Null Pointer Exception) : null 값을 제대로 처리 하지 않을때 생기는 예외
-   NPE를 방지할 수 있도록 null이 올 수 있는 값을 감싸는 Wrapper 클래스

# 11.2) Optional 생성

-   Optional.empty() : 빈 Optional 생성
-   Optional.of() : null을 저장할 수 없는 Optional 생성
-   Optinal.ofNullable : null값을 저장할 수 있는 Optional 생성

# 11.3) Optional 최종 연산

-   ifPresent() : null이 아니면 인자로 들어온 Consuper 실행
-   isPresnet() : null이 아니면 true, null 이면 false 반환
-   get() : null이 아니면 객체를 꺼내고, null이면 예외 발생
-   orElse() : null이 아니면 객체를 꺼내고, null 이면 orElse의 인자로 들어온 값을 반환
-   orElseGet() : null이 아니면 객체를 꺼내고, null 이면 orElseGet의 인자로 들어온 Supplier의 반환값을 반환
-   orElseThrow() : null이 아니면 객체를 꺼내고, null 이면 orElseThrow의 인자로 들어온 예외를 발생시킴
-   ifPresentOrElse() : null이 아니면 ifPresentOrElse의 첫번째 인자로 들어온 Consumer 실행, null 이면 ifPresentOrElse의 두번째 인자로 들어온 Runnable 실행
