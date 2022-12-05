## 16 public 클래스에서는 public 필드가 아닌 접근자 메서드를 사용하라

-   public 클래스에서는 가변 필드를 public으로 선언하면 안됩니다.
-   package-private 클래스나 private 중첩 클래스에서는 종종 필드를 노출하는 편이 나을때도 있습니다.
