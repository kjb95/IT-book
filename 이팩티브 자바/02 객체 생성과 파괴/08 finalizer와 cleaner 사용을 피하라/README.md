## 08 finalizer와 cleaner 사용을 피하라

### 자바의 객체 소멸자

자바에서는 두가지의 객체 소멸자 finalizer, cleaner를 제공합니다.  
finalizer, cleaner는 수행 시점뿐 아니라, 수행 여부도 보장하지 않습니다.
따라서 두 객체 소멸자의 사용은 피하는것이 좋습니다.