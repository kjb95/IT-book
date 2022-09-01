# 6.1) collect()

-   Collector를 기준으로 스트림의 요소를 수집

# 6.2) Collectors 메소드

-   toList() : 모든 Stream 요소를 List 인스턴스로 수집
-   toSet() : 모든 Stream 요소를 Set 인스턴스로 수집
-   toCollection() : 모든 Stream 요소를 특정 Collectiond 으로 수집
-   toMap() : 모든 Stream 요소를 Map 인스턴스로 수집
-   collectingAndThen() : 스트립 요소들의 수집이 끝난 직후 반환된 결과에 대하여 다른 작업을 수행
-   joining() : Stream의 String 요소들을 합침
-   counting() : Stream 요소들의 개수 반환
-   summarizingDouble/Long/Int() : 숫자 데이터에 대한 통계 정보를 포함하는 특수 클래스를 반환
-   averagingDouble/Long/Int() : Stream 요소들의 평균을 반환
-   summingDouble/Long/Int() : Stream 요소들의 합계를 반환
-   maxBy()/minBy() : Stream 요소들의 최대값/최소값 반환
-   groupingBy() : Stream 요소들을 그룹화하고 그 결과를 Map 인스턴스로 반환
-   partitioningBy() : Boolean 값을 키, 컬렉션을 값으로 저장하는 Map 인스턴로 수집
