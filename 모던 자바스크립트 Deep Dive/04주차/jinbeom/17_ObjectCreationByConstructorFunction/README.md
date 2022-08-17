# 생성자 함수에 의한 객체 생성

## 17.1) Object 생성자 함수
- Object 생성자 함수를 호출하면 빈 객체를 생성하여 반환
- 특별한 이유가 없다면 그다지 유용하지 않음

## 17.2) 생성자 함수
- new 연산자와 함께 호출하면 해당 함수는 생성자 함수로 동작
- 생성자 함수 내부에서 return 문을 반드시 생략해야 함
### 내부 메서드 [[Call]], [[Construct]]
- 함수 객체는 일반 객체가 가지고 있는 내부 슬롯과 내부 메서드를 모두 가짐
- 함수가 일반 함수로서 호출되면 함수 객체의 내부 메서드 [[Call]]이 호출됨
- 함수가 new 연산자와 함께 생성자 함수로서 호출되면 내부 메서드 [[Construct]]가 호출됨
### constructor와 non-constructor의 구분
- constructor : 함수 선언문, 함수 표현식, 클래스
- non-constructor : 메서드, 화살표 함수
- ECMAScript에서는 ES6 메서드 축약표현만 메소드로 인정
- no-constructor인 함수 객체는 내부 메서[[Construct]]를 갖지 않음
### new.target
- new 연산자와 함께 생성자 함수로서 호출되면 함수 내부의 new.target은 함수 자신을 가리킴
- new 연산자 없이 일반 함수로서 호출된 함수 내부의 new.target은 undefined
### 빌트인 생성자 함수
- 대부분의 빌트인 생성자 함수는 new 연산자 없이 호출해도 new 연산자와 함께 호출했을 떄와 동일하게 동작
- String, Number, Boolean 생성자 함수는 new 연산자 없이 호출하면 문자열, 숫자, 불리언 값을 반환