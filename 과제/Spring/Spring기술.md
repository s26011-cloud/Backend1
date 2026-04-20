# Spring 기술

## 백엔드 코어
- Spring Boot

- Spring MVC

- Spring Security

- Lombok

## 데이터를 주고 받는 통로 어노테이션

### @GetMopping / @PostMapping
- 주소창에 URL을 칠 때나(GET), 글쓰기 버튼을 눌러 데이터를 보낼때(POST) 사용합니다.

### @RequestParam
- URL에 포함된 파라미터를 가져올 때 씁니다.

### @PathVariable
- URL 경로 자체에 포함된 값을 변수로 가져올 때 씁니다.

### @RequesBody
- 클라이언트가 보낸 JSON 데이터 등을 자바 객체로 변환해 받을 떄 사용합니다.

## 귀찮은 코드를 줄여주는 Lombok 어노테이션

### @Getter / @Setter
- 변수마다 일일이 만들던 메서드를 자동으로 생성한다.

### @NoArgsConstructor / @AllArgsConstructor
- 기본 생성자나 모든 필드를 포함한 생성자를 자동으로 만든다.