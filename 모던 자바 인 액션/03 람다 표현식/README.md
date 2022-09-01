# 3.1) 함수형 인터페이스

-   1 개의 추상 메소드를 갖는 인터페이스
-   디폴트 메서드가 있더라도 추상 메서드가 오직 하나면 함수형 인터페이스

# 3.2) 함수형 인터페이스 종류

## Predicate< T > : boolean test(T t)

-   and() : Predicate들의 결과들을 AND로 연결하고 그 결과를 반환
-   or() : Predicate들의 결과들을 OR 로 연결하고 그 결과를 반환
-   isEuqal() : 인자로 전달된 객체와 같은지 확인
-   negate() : Predicate가 반환하는 값과 반대가 되는 값을 반환하는 Predicate를 반환

## Consumer< T > : void accept(T t)

-   Primitive type에 대한 Consumer 클래스 제공
-   andThen() : Consumer들을 연결해주는 Chaining 메소드

## Supplier< T > : T get()

-   메서드 참조 방식으로 정의할 수 있음
-   Primitive type에 대한 Supplier 클래스 제공
-   Stream.generate()는 Supplier를 인자로 받아, 무한한 Stream을 생성 (limit 메소드로 개수를 제한 해주어야 함)

## Function : R apply(T t)

-   andThen() : Function들을 연결해주는 Chaining 메소드
-   compose() : Function의 apply들을 합성
-   identity() : 함수 인자를 그대로 반환

## Comparator : int compare(T o1, T o2)

-   Collections.sort()나 Arrays.sort() 사용시 Comparator를 인자로 넣어 정렬할 수 있음

## Runnable : void run()

## Callable : V call()

# 3.3) 메서드 참조

-   람다 표현식이 단 하나만의 메소드 만을 호출하는 경우에 람다 표현식에서 불필요한 매개변수를 제거하고 '::' 기호를 사용하여 표현
-   메소드의 인자와 반환 타입을 알고 있어야 함

## 메서드 참조 종류

-   Static 메서드 참조 : Static 메서드를 메서드 참조로 사용하는 경우
-   Instance 메서드 참조 : 객체의 메서드를 메서드 참조로 사용하는 경우
-   Constructor 메서드 참조 : 생성자를 메서드 참조로 사용하는 경우
