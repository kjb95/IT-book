## Pages in Next.js

-   페이지의 파일 이름에 따라 경로와 연결
-   pages/index.js -> /
-   pages/a/b.js -> /a/b

## a Tag, Link Component

-   a Tag : 페이지를 이동 하면서, 페이지 전체를 재 렌더링
-   Link Component : 페이지를 이동 하면서, 필요한 부분만 재렌더링 되고, 나머지 부분은 유지 (Client-Side Navigation)

## Code splitting

-   Next.js는 코드 분할을 자동으로 수행하여 필요한 페이지만 제공
-   수백 페이지가 있는 경우에도 빠르게 로딩 됨
-   하나의 페이지에 에러가 발생해도 애플리케이션은 여전히 작동

## Prefetching

-   Link 컴포넌트가 브라우저의 뷰포트에 나타나게 되면, 해당 페이지의 코드들을 미리 가져 옴
-   링크를 클릭 하면 빠른 페이지 전환이 가능
