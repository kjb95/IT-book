# 1.1) 개발 환경설정

## JDK

-   Java Development Kit
-   Java로 소프트웨어를 개발할 수 있도록 여러 기능들을 제공하는 패키지
-   openjdk 11 버전 설치

## Eclipse

-   Preferences > Java > Compiler 에서 JDK 11 버전으로 변경
-   Preferences > Java > Installed JREs 에서 Add ... > standard VM > JRE Home : /Library/Java/JavaVirtualMachines/temurin-11.jdk/Contents/Home
-   eclipse.ini 파일의 -vm 내용 변경 : /Library/Java/JavaVirtualMachines/temurin-11.jdk/Contents/Home/bin
-   Help > Eclipse Marketplace 에서 Spring Tools 3 Add-On ... 설치
-   Help > Install New Software > https://download.eclipse.org/releases/2021-09 검색 결과 전부 설치

## Tomcat

-   웹 어플리케이션 서버(WAS) 로서, 자바 서블릿을 실행키고 JSP코드가 포함되어 있는 웹 페이지를 만듬
-   Tomcat 9.0 설치
-   Preferences > Runtime Enviroment 에서 Add ... > Apache Tomcat v9.0

# 1.2) 스프링 프로젝트 생성

## 프로젝트 생성

-   Perspective > Spring
-   File > New > Spring Legacy Project

## 스프링 버전 번경

### pom.xml 수정

-   3.1.1.RELEASE -> 5.0.7.RELEASE
-   1.6 -> 11

### 메이븐 업데이트

-   Project > Update Maven Project

# 1.5) Java Configuraation을 하는 경우

## XML 파일 삭제

-   File > New > Spring Legacy Project
-   web.xml, servlet-context.xml, root-context.xml 삭제
-   servlet-context.xml, root-context.xml이 포함된 spring 폴더 삭제
-   pomx.xml 수정 (42p)
-   Project > Update Maven Project

## @Configuration (43p)

## web.xml을 대신하는 클래스 작성 (44p)
