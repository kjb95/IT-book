## 19 상속을 고려해 설계하고 문서화하라. 그러지 않았다면 상속을 금지하라

### 메소드 재정의 하기

-   상속용 클래스는 재정의할 수 있는 메소드들을 내부적으로 어떻게 이용하는지 문서로 남겨야 합니다.
-   상속용 클래스는 배포 전에 반드시 하위 클래스를 만들어 검증해야 합니다.
-   상속용 클래스의 생성자는 직접적으로든 간접적으로든 재정의 가능 메소드를 호출해서는 안됩니다.

### 상속 금지하기

-   상속용으로 설계하지 않은 클래스는 상속을 금지해야 합니다.

1. final로 클래스를 선언하기
2. 모든 생성자를 private이나 package private으로 선언하고, public 정적 팩토리 만들기