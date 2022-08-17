# Ajax

## 43.1) Ajax란?
- 자바스크립트를 사용하여 브라우저가 서버에게 비동기 방식으로 데이터를 요청하고, 서버가 응답한 데이터를 수신하여 웹페이지를 동적으로 갱신하는 프로그래밍 방식
- 변경할 부분을 갱신한 데 필요한 데이터만 서버로 전송
- 변경할 필요가 없는 부분은 다시 렌더링 하지 않음
- 클라이언트와 서버와의 통신이 비동기 방식으로 동작

## 43.2) JSON
- 클라이언트와 서버 간의 HTTP 통신을 위한 텍스트 데이터 포맷

## 43.3) XMLHttpRequest
- 자바스크립트를 사용하여 HTTP 요청을 전송하려면 XMLHttpRequest 객체를 사용
- XMLHttpRequest 객체는 HTTP 요청 전송과 HTTP 응답 수신을 위한 다양한 메서드와 프로퍼티를 제공
### HTTP 요청 전송 순서
1. XMLHttpRequest.prototype.open 메서드로 HTTP 요청을 초기화
- HTTP 요청 메서드는 클라이언트가 서버에게 요청의 종류와 목적을 알리는 방법
2. 필요에 따라 XMLHttpRequest.prototype.setRequestHeader 메서드로 특정 HTTP 요청의 헤더 값을 설정
3. 필요에 따라 XMLHttpRequest.prototype.send 메서드로 초기화된 HTTP 요청을 전송
- GET 요청일 경우 URL의 일부분인 쿼리 문자열로 전송 (바디에 데이터는 무시됨)
- POST 요청일 경우 데이터를 바디에 담아 전송
### HTTP 응답 처리
- 서버가 전송한 응답을 처리하려면 XMLHttpRequest 객체가 발생시키는 이벤트를 캐치해야 함