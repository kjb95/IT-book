# 6.1) @Controller, @RequestMapping

-   servlet-context.xml에는 < context:component-scan > 태그를 이용해서 지정된 패키지 내의 빈 설정이 되어있는 클래스들을 생성하고 관리

# 6.2) Controller의 파라미터 수집

## @InitBinter

-   Controller 에서 파라미터를 바인딩할 때 @InitBinter가 붙은 메소드가 자동으로 호출 됨

# 6.4) Model이라는 데이터 전달자

-   Model 객체는 컨트롤러에서 생성된 데이터를 담아서 View에 전달하는 역할

## @ModelAttribute

-   해당 어노테이션을 전달받은 파라미터는 타입에 관계없이 Model에 담아서 전달 됨

## RedirectAttributes

-   일회성으로 사용되는 데이터를 전달하기 위해 사용

# 6.5) Controller의 리턴 타입

## Controller의 메서드가 사용하는 리턴 타입

-   String : jsp를 이용하는 경우에는 jsp 파일의 경로와 파일이름을 나타냄
-   void : 호출하는 URL과 동일한 이름의 jsp를 의미
-   VO, DTO (객체 타입) : 주로 JSON 타입의 데이터를 만들어서 반환하는 용도
-   ResponseEntity : response 할 때 Http 헤더 정보와 내용을 가공하는 용도로 사용
-   Model, ModelAndView : Model로 데이터를 반환하거나 화면까지 같이 지정하는 경우에 사용
-   HttpHeaders : 응답에 내용 없이 Http 헤더 메시지만 전달하는 용도로 사용

## 파일 업로드 처리 (149p)

# 6.6) Controller의 Exception 처리

## @ControllerAdvice

-   AOP를 이용하여 공통적인 예외사항에 대해서 별도로 분리
-   해당 객체가 스프링의 컨트롤러에서 발생하는 예외를 처리하는 존재임을 명시

## @ExceptionHandler

-   해당 메서드가 지정한 예외 타입을 처리

## 404 에러 페이지 (158p)