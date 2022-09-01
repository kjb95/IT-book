# 5.1) 중간 연산

## filter()

-   사용된 함수형 인터페이스 형식 : Predicate< T >
-   반환 형식 : Stream< T >
-   Predicate가 true인 모든 요소를 포함하는 스트림을 반환

## distinct()

-   반환 형식 : Stream< T >
-   중복되는 요소들을 모두 제거해주고 새로운 스트림을 반환

## takeWhile()

-   사용된 함수형 인터페이스 형식 : Predicate< T >
-   반환 형식 : Stream< T >
-   filter()와 다른점은 Predicate가 처음으로 false일 경우 연산을 바로 멈춤

## dropWhile()

-   사용된 함수형 인터페이스 형식 : Predicate< T >
-   반환 형식 : Stream< T >
-   takeWhile과 정반대의 작업으로, Predicate가 처음으로 false인 시점까지의 요소를 모두 버리고 남은 요소를 반환

## skip()

-   사용된 함수형 인터페이스 형식 : long
-   반환 형식 : Stream< T >
-   인자로 들어온 n에 대해, n개의 요소를 제외한 스트림 반환

## limit()

-   사용된 함수형 인터페이스 형식 : long
-   반환 형식 : Stream< T >
-   인자로 들어온 n에 대해, n 이하의 크기를 갖는 스트림 반환

## map()

-   사용된 함수형 인터페이스 형식 : Function< T, R >
-   반환 형식 : Stream< R >
-   함수를 인자로 받아 각 요소에 적용되고, 적용된 결과가 새로운 요소로 매핑 됨

## flatMap()

-   사용된 함수형 인터페이스 형식 : Function< T, Stream< R > >
-   반환 형식 : Stream< R >
-   스트림의 각 값을 다른 스트림으로 만든 다음 모든 스트림을 하나의 스트림으로 연결

## sorted

-   사용된 함수형 인터페이스 형식 : Comparator< T >
-   반환 형식 : Stream< T >
-   요소들을 Comparable을 기준으로 정렬

# 5.2) 최종 연산

## anyMatch()

-   사용된 함수형 인터페이스 형식 : Predicate< T >
-   반환 형식 : boolean
-   적어도 한 요소가 주어진 Predicate와 일치하는지 확인

## allMatch()

-   사용된 함수형 인터페이스 형식 : Predicate< T >
-   반환 형식 : boolean
-   모든 요소가 Predicate와 일치하는지 확인

## nonMatch()

-   사용된 함수형 인터페이스 형식 : Predicate< T >
-   반환 형식 : boolean
-   allMatch()와 반대로 모든 요소가 일치하지 않는지 확인

## findAny()

-   반환 형식 : Optional< T >
-   현재 스트림에서 임의의 요소 반환

## findFirst()

-   반환 형식 : Optional< T >
-   생성된 스트림에서 순서가 정해져 있을 때, 첫 번째 요소를 반환

## forEach()

-   사용된 함수형 인터페이스 형식 : Consumer< T >
-   반환 형식 : void
-   요소 전체를 반복하며 처리

## collect()

-   사용된 함수형 인터페이스 형식 : Collector< T, A, R >
-   반환 형식 : R
-   Collector를 기준으로 스트림의 요소를 수집

## reduce()

-   사용된 함수형 인터페이스 형식 : BinaryOperator< T >
-   반환 형식 : Optional< T >
-   reduce([초기값], Operator)
-   Operator를 통해 모든 요소를 하나씩 소비하면서 최종 결과를 반환

## count

-   반환 형식 : long
-   스트림의 요소 개수 반환

# 5.3) 스트림 생성

-   Stream.of() : 스트림 생성
-   Stream.empty() : 비어있는 스트림 생성
-   Stream.generate() : Supplier를 인자로 받아서 무한 스트림 생성
-   Stream.iterate() : 초기값과 Supplier를 인자로 받아서 무한 스트림 생성
