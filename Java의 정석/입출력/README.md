# 스트림

-   스트림 : 데이터를 운반하는데 사용되는 연결통로
-   보조 스트림 : 데이터를 입출력할 수 있는 기능은 없지만, 스트림의 기능을 향상시키거나 새로운 기능을 추가
-   바이트 기반 스트림 : byte[]로 데이터를 전송하는 입출력 스트림 (XXXInputStream, XXXOutputStream)
-   문자 기반 스트림 : char[]로 데이터를 전송하는 입출력 스트림 (XXXReader, XXXWriter)

# 스트림 종류

-   FileInputStream / FileOutputStream : 파일에 입출력 하기 위한 스트림
-   FilterInputStream / FilterOutputStream : InputStream / OutputStream의 자손이면서 모든 보조 스트림의 조상
-   BufferedInputStream / BufferedOutputStream : 스트림의 입출력 효율을 높이기 위해 버퍼를 사용하는 보조 스트림
-   SequenceInputStream : 여러 개의 입력스트림을 연속적으로 연결해서 하나의 스트림으로 데이터를 읽는 것 같이 처리할 수 있도록 도와 줌
-   PrintStream : print, println, printf와 같은 메소드들을 오버 로딩 하여 제공

# 직렬화

-   직렬화 : 객체에 저장된 데이터를 스트림에 쓰기 위해 연속적인 데이터로 변환하는 것
-   역직렬화 : 스트림 으로부터 데이터를 읽어서 객체를 만드는 것
-   ObjectOutputStream : 직렬화시 사용
-   ObjectInputStream : 역직렬화시 사용
-   Serializable 인터페이스를 구현하면 직렬화가 가능한 클래스를 만들 수 있음
