# 빌트인 객체

## 21.1) 자바스크립트 객체의 분류
### 표준 빌트인 객체
- ECMAScript 사양에 정의된 객체
- 표준 빌트인 객체는 전역 객체의 프로퍼티로서 제공
### 호스트 객체
- 자바스크립트 실행환경(브라우저 또는 Node)에서 추가로 제공하는 객체
### 사용자 정의 객체
- 사용자가 직접 정의한 객체

## 21.2) 표준 빌트인 객체
- ECMAScript 사양에 정의된 객체
- 표준 빌트인 객체는 전역 객체의 프로퍼티로서 제공
- Math, Reflect, JSON을 제외한 표준 빌트인 객체는 모두 인스턴스를 생성할 수 있는 생성자 함수 객체로써, 프로토타입 메서드와 정적 메서드를 제공
- 생성자 함수가 아닌 Math, Reflect, JSON 객체는 정적 메서드만 제공

## 22.3) 원시값과 래퍼 객체
- 원시값을 객체처럼 사용하면 자바스크립트 엔진은 암묵적으로 연관된 객체를 생성하여 생성된 객체로 프로퍼티에 접근하거나 메서드를 호출하고 다시 원시값으로 되돌림
- 래퍼 객체 : 문자열, 숫자, 불리언 값에 대해 객체처럼 접근하면 생성되는 임시 객체

## 22.4) 전역 객체
- 어떤 객체에도 속하지 않고, 어떤 객체보다도 먼저 생성되는 특수한 객체
- window 객체 : 브라우저 환경에서의 전역객체
- global 객체 : Node 환경에서의 전역 객체
- let이나 const로 선언한 전역 변수는 전역 객체의 프로퍼티가 아님
### 암묵적 전역
- 변수의 선언 없이 전역 객체에 프로퍼티를 동적 생성하여, 마치 전역 변수처럼 동작하는 것
- 변수가 아니므로 호이스팅이 발생하지 않음