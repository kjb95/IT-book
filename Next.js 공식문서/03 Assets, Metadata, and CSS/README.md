## Assets

-   /public 폴더 안에 정적 파일을 저장해 두었다가 요청 시 제공

## Image Component and Image Optimization

-   페이지를 읽어들이는 시점에 중요하지 않은 컨텐츠의 로딩은 늦게 하는 Lazy Loading이 적용 됨
-   작은 뷰포트를 가진 장치에 큰 이미지를 출력하는 것을 방지하기 위해 이미지 사이즈를 최적화 해 줌
-   미리 이미지 크기 만큼 영역을 표시해서 이미지가 로드 된 후에도 레이아웃이 흔들리지 않도록 placeholder 제공

## Using the Image Component

-   Next.js는 빌드 시, 온디맨드로 이미지를 최적화 하기 때문에, 전송 해야하는 이미지가 아무리 많아도 빌드 시간은 증가하지 않음
-   이미지는 뷰포트로 스크롤될 때 로드 됨

## Metadata

-   next/head의 Head 컴포넌트를 통해 title 태그와 link 태그 수정이 가능

## Third-Party JavaScript

-   next/script의 Script 컴포넌트를 이용하면 스크립트를 불러오거나 실행할 때 최적화가 가능
-   strategy : 언제 써드파티 스크립트를 로드할지 결정
-   onLoad : 스크립트 로드가 완료된 직후 실행할 코드

## style-jsx

-   Next,js가 내장지원하는 CSS
-   CSS 범위는 해당 컴포넌트로 한정

## Sass

-   Systactically Awesome Style Sheets
-   CSS의 전처리기로, .scss/sass 두 확장자를 지원
-   Next.jssm는 Sass를 내장 지원

## CSS Modules

-   클래스 이름을 고유한 값으로 만들어서 컴포넌트 스타일 클래스 이름이 중첩되는 현상을 방지해 주는 기술
-   XXX.module.css 파일을 생성 한 뒤, CSS 코드 삽입

## pages/\_app.js

-   모든 페이지가 초기화될 때 가장 먼저 호출 되는 파일
-   각 페이지의 공통된 레이아웃 페이지, 글로벌 CSS 적용 가능

## Using classnames library to toggle classes

-   CSS 토글을 구현할 수 있는 라이브러리

## Customizing PostCSS Config (?)

## Using Sass

-   Next.js에서는 .scss, .sass 확장자의 Sass 파일이 import 가능
