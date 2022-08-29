# 7.1) 3-Tier 방식

-   Presentation Tier : 화면에 보여주는 기술을 사용하는 영역
-   Business Tier : 순수한 비즈니스 로직을 담고 있는 영역
-   Persistence Tier : 데이터를 어떤 방식으로 보관하고, 사용하는가에 대한 설계가 들어가는 영역

# 7,2) 각 영역의 Naming Convention

## 패키지의 Naming Convention

-   config : 프로젝트와 관련된 설정 클래스
-   controller : 스프링 MVC의 Controller
-   service : 스프링 Service 인터페이스와 구현 클래스
-   domain : Vo, DTO 클래스
-   persistence : MyBatis Mapper 인터페이스
-   exception : 예외처리
-   aop : Spring AOP
-   security : Spring Security
-   util : 각종 유틸리티 클래스
