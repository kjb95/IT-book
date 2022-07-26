# 이벤트

## 40.1) 이벤트 핸들러 등록
- 이벤트 헨들러 : 이벤트가 발생했을 때 호출되는 함수
- 이벤트 헨들러 등록 : 이벤트가 발생했을 때 브라우저에게 이벤트 핸들러의 호출을 위임하는 것
- 이벤트 타겟 : 이벤트를 발생시킬 객체
- 이벤트 타입 : 이벤트의 종류

## 40.2) 이벤트 핸들러 제거
- 무명 함수를 이벤트 핸들러로 등록한 경우 제거할 수 없음
- 이벤트 핸들러 프로퍼티 방식으로 등록한 이벤트 핸들러는 removeEventListener 메서드로 제거할 수 없고, null을 할당해 주면 됨

## 40.3) 이벤트 객체
- 이벤트가 발생하면 이벤트에 관련한 다양한 정보를 담고 있는 이벤트 객체가 동적으로 생성됨
- 생성된 이벤트 객체는 이벤트 핸들러의 첫 번째 인수로 전달됨
- 이벤트 핸들러 어트리뷰트 방식의 경우 이벤트 객체를 전달받으려면 이벤트 핸들러의 첫 번째 매개변수 이름이 반드시 event 이어야 함

## 40.4) 이벤트 전파
- 생성된 이벤트 객체는 이벤트를 발생시킨 이벤트 타깃을 중심으로 DOM 트리를 통해 전파됨
### 이벤트 객체 전파 3단계
1. 캡쳐링 단계 : 이벤트가 상위 요소에서 하위 요소 방향으로 전파
2. 타깃 단계 : 이벤트가 이벤트 타깃에 도달
3. 버블링 단계 : 이벤트가 하위 요소에서 상위 요소 방향으로 전파
- 이벤트 핸들러 어트리뷰트/프로퍼티 방식으로 등록한 이벤트 핸들러는 타깃단계와 버블링 단계의 이벤트만 캐치할 수 있음
- addEventListener 메서드 방식으로 등록한 이벤트 핸들러는 타깃 단계와 버블링 단계 뿐만 아니라 캡쳐링 단계의 이벤트도 캐치할 수 있음

## 40.5) 이벤트 위임
- 여러 개의 하위 DOM 요소에 각각 이벤트 핸들러를 등록하는 대신 하나의 상위 DOM 요소에 이벤트 핸들러를 등록하는 방법