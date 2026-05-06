# Spring Security란
- Spring 기반 애플리케이션의 인증과 인가를 담당하는 보안 프레임워크이다.

## 동작 방식
- Spring Security는 Filter Chain 기반으로 동작한다. HTTP 요청이 Controller에 도달하기 전에 여러 필터를 순서대로 통과하는 구조다.

## 주요 특징
- Filter Chain - 모든 요청이 보안 필터를 통과

- 인증/인가 분리 - 로그인과 권한을 구분

- 다양한 인증 방식 - JWT, OAuth2 등과 연동 가능

# JWT란
- JWT는 유저 정보를 JSON으로 담아 서명한 토큰이다. 서버가 세션을 저장하지 않아도 되는 Stateless 인증 방식이다.

## 인증 흐름
- 로그인 -> DB조회 & 비밀번호 검증 -> Access Token + Refresh Token 발급

- API 요청 -> 헤더에 Access Token 첨부 -> 서명 검증 + 만료 확인 -> SecurityContext 저장 -> Controller 실행

- 토큰 만료 -> Refresh Token으로 재발급 요청 -> DB 대조 -> 새 Access Token 발급

- 로그아웃 -> 서버에서 Refresh Token 삭제

## 주요 특징
- Stateless - 서버가 세션 저장 안 해도 됨

- Header.Payload.Signature 구조 - 토큰 자체에 사용자 정보 포함

- 위변조 방지 - 서명으로 검증