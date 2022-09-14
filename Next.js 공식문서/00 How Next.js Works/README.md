## Development Environments

-   개발자가 애플리케이션을 잘 구축 하도록 최적화
-   ESLint, 빠른 새로 고침 등 개발자의 능률 향상을 위한 기능 제공

## Production Environments

-   유저가 애플리케이션을 잘 사용하도록 최적화
-   코드를 변환하여 성능과 접근성을 높임

## Compiling

-   개발자가 작성한 jsx, TypeScript, 최신 버전의 JavaScript 코드를 브라우저가 이해하기 쉬운 JavaScript로 변환하는 과정

## Minifying

-   코드의 기능을 변경하지 않고, 불필요한 코드 서식 및 주석을 제거하는 과정
-   파일 크기를 줄여 성능을 향상 시킴
-   Next.js 에서 JavaScript 및 CSS 파일은 배포 모드에서 축소화 됨

## Bundling

-   최적화를 위해 파일 또는 모듈들을 병합하는 과정

## Code Splitting

-   애플리케이션의 앤트리 포인트에 필요한 청크들로 분할하는 과정
-   Next.js는 빌드할 때, pages 하위 디렉토리에서 JavaScript 번들 과정을 통해 코드를 분할

## Build Time

-   배포 모드에서 애플리케이션 코드를 준비하는 시간
-   애플리케이션을 빌드하면, 코드를 최적화된 파일로 변환하여 서버에 배포

## Runtime

-   애플리케이션 빌드 및 배포 후에, 사용자의 요청에 대한 응답을 하며 실행되는 시간

## Rendering

-   작성된 코드를 HTML로 변환하여 웹 사이트가 그려지는 과정
-   Next.js 에서는 SSR, SSG, CSR 방식의 렌더링을 사용할 수 있음
-   Next.js 에서는 기본적으로 모든 페이지를 미리 렌더링 함

## SPA

-   Single Page Application
-   브라우저가 최초에 한번 페이지 전체를 로드하고, 이후 부터는 특정 부분만 데이터를 바인딩

## MPA

-   Multi Page Application
-   인터렉션이 발생할 때마다, 서버로 부터 새로운 html을 받아와서 페이지 전체를 새로 렌더링
-   화면을 구성하는 여러 페이지가 있기 때문에, SEO에 유리

## CSR

-   Client Side Rendering
-   SPA는 CSR 방식을 사용
-   사용자의 요청에 따라 필요한 부분만 렌더링
-   서버는 화면을 표시하는데 필요한 완전한 리소스를 응답하여 초기 로딩이 느림

## SSR

-   Server Side Rendering
-   MPA은 SSR 방식을 사용
-   서버로 부터 완전하게 만들어진 HTML 파일을 받아와 페이지 전체를 렌더링
-   서버로 부터 화면을 렌더링 하기 위해 필수적인 요소만 먼저 가져오기 때문에 초기 로딩이 빠름
-   매 요청마다 모든 리소스를 새로 준비해야 하므로 서버 부담이 큼

## SSG

-   Static Site Generation
-   배포 모드에서 빌드 시, 각 페이지를 생성하고, CDN에 저장
-   한번 요청한 페이지를 재요청시 이미 생성한 페이지를 반환

## Origin Server

-   응용 프로그램 코드의 원본 버전을 저장하고 실행 하는 컴퓨터

## CDN

-   Content Delivery Network
-   클라이언트와 오리진 서버 사이에 존재
-   정적 컨텐츠를 전세계의 여러 장소에 저장하여 새 요청시, 유저로 부터 가장 가까운 CDN에 캐싱된 결과를 응답

## Edge

-   엣지 서버는 전 세계에 여러 장소에 분산되어 있고, 캐싱과 코드 실행이 모두 가능
