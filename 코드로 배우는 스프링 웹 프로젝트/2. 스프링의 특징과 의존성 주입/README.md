# 2.1) 스프링 프레임워크의 간략한 역사

## 스프링의 주요 특징

### POJO 기반의 구성

-   Plain Old Java Object
-   환경과 기술에 종속되지 않고 필요에 따라 재활용될 수 있는 방식으로 설계된 객체

### 의존성 주입(DI)과 스프링

-   의존성(Dependency) : 하나의 객체가 다른 객체 없이 제대로 된 역할을 할 수 없는 것
-   의존성 주입(Dependency Injection) : 어떤 객체가 필요한 객체를 외부에서 밀어 넣는 것
-   ApplicationContext는 존재가 필요한 객체를 생성하고, 관리하고, 주입
-   Bean : ApplicationContext가 관리하는 객체

### AOP의 지원

-   Aspect Oriented Programming
-   Cross Concern : 비즈니스 로직은 아니지만, 반드시 처리가 필요한 부분
-   AOP : Cross Concern을 분리해서 모듈로 분리한것

### 트랜잭션의 지원

-   트랜잭션관리를 어노테이션이나 XML로 설정 가능

# 2.3) 스프링이 동작하면서 생기는 일

1. ApplicationContext 객체 생성
2. root-context.xml에 스프링은 자신이 객체를 생성하고 관리해야 하는 설정이 명시
3. root-context.xml에 설정되어 있는 < context:component-scan > 태그의 내용을 통해서 패키지를 스캔
4. 해당 패키지에 있는 클래스들 중에서 @Component 어노테이션이 존재하는 클래스의 인스턴스를 생성
5. 생성된 인스턴스를 필요한 곳에 주입

## 테스트 코드를 통한 확인

-   스프링은 객체를 생성하고 관리하는 일종의 컨테이너 기능을 가짐

## 코드에 사용된 어노테이션들 (64p)