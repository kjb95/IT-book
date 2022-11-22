## 09 try-finally보다는 try-with-resources를 사용하라

### try-with-resources

try-with-resources는 AutoCloseable을 구현한 객체만 try()구문이 종료될떄, 자동으로 자원을 해제해주는 기능입니다.  
try()구문을 벗어나면, 객체의 close()를 자동으로 호출하기때문에, close()를 명시할 필요가 없습니다.  
간결한 코드와, 유지보수가 용이한 코드를 생성하게 도와주기도 합니다.