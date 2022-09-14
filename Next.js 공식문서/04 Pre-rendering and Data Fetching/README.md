## Check That Pre-rendering Is Happening

-   Next.js는 자바스크립트 없이도 앱의 UI를 볼 수 있도록, 앱을 정적 HTML로 프리 렌더링 함
-   프리 렌더링이 되는지 확인 하려면, 브라우저의 자바스크립트가 작동되지 않더라도 페이지가 렌더링 되어야 함

## Pre-rendering (Next.js)

-   Initial Load : 프리 렌더링 된 HTML을 보여 줌
-   Hydration : 앱이 인터렉티브 상태가 됨
-   Link 같은 인터렉티브한 컴포넌트가 있다면, 해당 요소는 JS가 로드된 후에 활성화 됨

## No Pre-rendering (React.js)

-   Initial Load : 앱이 렌더링 되지 않음
-   Hydration : 앱이 인터렉티브 상태가 됨

## Static Site Generation

-   빌드 타임때 생성되며, 한 번 프리 렌더링된 페이지는 매 요청 마다 재사용 됨
-   개발 모드에서는, 매 요청 마다 페이지를 새로 생성

## Server-Side Rendering

-   프리 렌더링 방식으로, 페이지를 매 요청 마다 새로 생성

## getStaticProps()

-   배포 모드에서 빌드 타임 때 호출 됨
-   개발 모드에서는, 매 요청 마다 호출 됨
-   클라이언트 단에서는 작동하지 않고, 오직 서버 단에서만 하므로 요청 시에 데이터를 가져와야 하는 상황 에서는 사용할 수 없음
-   page 에서만 export 될 수 있음

## Front-matter

-   파일 시작 시 작성하는 YAML 또는 JSON 코드
-   Front-matter가 끝나는 부분은 YAML의 경우 (---)로, JSON의 경우 (;;;)로 구분

## gray-matter

-   마크다운 파일을 파싱할 때 사용되는 라이브러리

## getServerSideProps()

-   매 요청 마다 호출 됨
-   요청 시에 데이터를 가져와야 하는 페이지를 프리 렌더링 할 때 사용
-   CDN과 같은 캐시를 사용할 수 없기 때문에 비교적 느림

## Client-Side Rendering

-   SEO가 필요하지 않고, 프리 렌더링이 필요없고, 데이터의 업데이트가 잦을 때 사용

## SWR

-   CSR 시에 사용되는 리액트 훅
