# 비동기 프로그래밍

## 42.1) 동기 처리와 비동기 처리
- 동기 처리 : 현재 실행 중인 태스크가 종료될 때까지 다음에 실행할 태스크가 대기하는 방식
- 비동기 처리 : 현재 실행 중인 태스크가 종료되지 않은 상태라 해도 다음 태스크를 곧바로 실행하는 방식

## 42.2) 이벤트 루프와 태스트 큐
### 콜 스택
- 함수를 호출하면 함수 실행 컨텍스트가 순차적으로 콜 스택에 푸시되어 순차적으로 실행
- 자바스크립트 엔진은 단 하나의 콜 스택을 사용
### 힙
- 객체가 저장되는 메모리 공간
- 실행 컨텍스트는 힙에 저장된 객체를 참조
### 태스크 큐
- 비동기 함수의 콜백 함수 또는 이벤트 핸들러가 일시적으로 보관되는 영역
### 이벤트 루프
- 콜 스택에 현재 실행 중인 실행 컨텍스트가 있는지, 태스크 큐에 대기 중인 함수가 있는지 반복해서 확인
- 콜 스택이 비어 있고 태스트 큐에 대기 중인 함수가 있다면 이벤트 루프는 순차적으로 태스크 큐에 대기 중인 함수를 콜스택으로 이동