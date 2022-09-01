# 12.1) LocalDate / LocalTime / LocalDateTime

-   LocalDate : 타임존 개념이 필요없는 날짜 정보를 나타냄
-   LocalTime : 타임존 개념이 필요없는 시간 정보를 나타냄
-   LocalDateTime : 타임존 개념이 필요 없는 날짜와 시간 정보를 모두 나타냄
-   now() : 현재 날짜 혹은 시간 정보를 가진 객체 생성
-   of(), parse() : 인자에 대한 날짜 혹은 시간 정보를 가진 객체 생성
-   plusXXX() / minusXXX() : 날짜 혹은 시간이 변경된 객체 반환
-   isAfter() / isBefore() : 날짜 혹은 시간이 이전인지 이후인지 확인

# 12.2) Instant

-   UTC 기준으로 1970년 1월 1일 0시 0분 0초를 숫자 0으로 정하고 그로부터 경과된 시간을 양수 또는 음수로 표현
-   ofEpochSecond() : 인자에 대한 Instant 객체 생성
-   now() : 현재 시간의 Instant 객체 생성

# 12.3) Duration / Period

-   Duration : 두 시간의 간격을 초나 나노 초 단위로 나타냄
-   Period : 두 날짜의 사이의 간격을 년/월/일 단위로 나타냄
