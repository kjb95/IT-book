# ES6 함수의 추가 기능

## 26.1) 함수의 구분
- ES6 이전의 모든 함수는 callable 이면서 constructor
- ES6에서는 함수를 일반함수, 메서드, 화살표함수 세가지 종류로 구분함

## 26.2) 메서드
- 메서드 축약 표현으로 정의된 함수만을 의미
- 인스턴스를 생성할 수 없는 non-constructor
- 자신을 바인딩한 객체를 가리키는 내부 슬롯 [[HomeObject]]를 가짐
- 메서드가 아닌 함수는 내부 슬롯 [[HomeObject]]을 갖지 않기 때문에 super 키워드를 사용할 수 없음

## 26.3) 화살표 함수
- 기존의 함수 정의 방식보다 간략하게 함수를 정의
- 인스턴스를 생성할 수 없는 non-constructor
- 중복된 매개변수 이름을 선언할 수 없음
- 함수 자체의 this, arguments, super, new.target 바인딩을 갖지 않음
### this
- 화살표 함수는 함수 자체의 this 바인딩을 갖지 않음
- lexical this : 화살표 함수 내부에서 this를 참조하면 상위 스코프의 this를 그대로 참조
- Function.prototype.call, Function.prototype.apply, Function.prototype.bind 메서드를 사용해도 화살표 함수 내부의 this를 교체할 수 없고, 항상 상위 스코프의 this 바인딩을 참조
- 클래스 필드에 할당한 화살표 함수 내부에서 참조한 this는 constructor 내부의 this 바인딩과 같음
- 클래스 필드에 할당한 화살표 함수는 프로토타입 메서드가 아니라 인스턴스 메서드가 됨
### super, arguments
- 화살표 함수는 함수 자체의 super, arguments 바인딩을 갖지 않음
- 화살표 함수 내부에서 super를 참조하면 상위 스코프의 super, arguments를 참조

## 26.4) Rest 파라미터
### arguments 객체
- 함수 호출 시 전달된 인수들의 정보를 담고 있는 순회 가능한 유사 배열 객체
- 화살표 함수는 arguments 객체를 가지지 않음
### Rest 파라미터
- 함수 호출 시 전달된 인수들의 정보를 담고 있는 배열