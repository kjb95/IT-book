# 5.1) 스프링 MVC 프로젝트의 내부 구조

## WebApplicationContext

-   ApplicationContext : 애플리케이션에 대한 context를 가짐
-   WebApplicationContext : ApplicationContext를 확장한 인터페이스로, 웹 애플리케이션에 필요한 몇 가지 기능들이 추가 됨

## 프로젝트 경로 수정

-   https://seeminglyjs.tistory.com/304

# 5.2) 예제 프로젝트의 로딩 구조

## web.xml

-   Tomcat 구동과 관련된 설정
-   프로젝트 구동의 시작
-   root-context.xml의 경로가 설정되어 있음

## root-context.xml

-   root-context.xml에 정의된 빈들은 스프링의 Context안에 생성되고, 객체들 간의 의존성이 처리 됨
-   root-context.xml이 처리된 후에는 DispatcherServlet 이라는 서블릿과 관련된 설정들이 동작

## servlet-context.xml

-   DispatcherServlet에서 XmlWebApplicationContext를 이용해서 servlet-context.xml을 로딩하고 해석

# 5.3) 스프링 MVC의 기본 사상

-   Servlet/JSP 에서는 HttpServletRequest / HttpServletResponse 객체를 이용해 브라우저에서 전송한 정보를 처리
-   스프링 MVC를 이용하게 되면 Servlet/JSP의 API를 사용하지 않고도, 원하는 기능을 구현할 수 있게 됨

# 5.4) 모델2와 스프링 MVC

## 모델2

-   스프링 MVC는 모델2 라는 방식으로 처리되는 구조
-   모델2 : 로직과 화면을 분리

## 스프링 MVC 기본 구조

1. 사용자의 Request는 Front-Controller인 DispatcherServlet을 통해서 처리
2. HandlerMapping은 Request의 처리를 담당하는 컨트롤러를 찾기 위해서 존재
3. 적절한 컨트롤러가 찾아졌다면 HandlerAdapter를 통해서 해당 컨트롤러를 동작시킴
4. Controller는 실제 Request를 처리하는 로직이 작성되어 있음
   Controller에서 View에 전달해야 하는 데이터는 주로 Model이라는 객체에 담아서 전달
5. ViewResolver는 Controller가 반환한 결과를 어떤 View를 통해서 처리할지 해석
6. View는 실제로 응답 보내야 하는 데이터를 Jsp 등을 이용해서 생성
7. 만들어진 응답은 Dispatcherservlet을 통해서 전송
