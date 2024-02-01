# 🎯 HTTP Method

클라이언트와 서버 사이에 이루어지는 요청과 응답 데이터를 전송하는 방식으로 9가지의 종류가 있다.

# 📝 주요 메소드

## 📋 GET

리소스 조회

## 📋 POST

데이터 추가, 등록

## 📋 PUT

리소스 대체(덮어쓰기), 없다면 생성

## 📋 PATCH

리소스 부분 변경

## 📋 DELETE

리소스 삭제

# 기타 메소드

### 📋 HEAD

GET과 동일한 역할을 하지만 상태줄과 헤더만 반환받음(body x)

### 📋 OPTIONS

요청한 리소스에 대한 통신 가능 여부 설명 (주로 CROS사용)

### 📋 CONNECT

네트워크 터널 설정

### 📋 TRACE

진단 목적으로 사용 메시지 루프백 테스트

# 📝 HTTP 메소드 속성

| method  | Safe | 멱등성 | 캐시 |
| ------- | ---- | ------ | ---- |
| GET     | O    | O      | O    |
| POST    | X    | X      | O    |
| PUT     | X    | O      | X    |
| PATCH   | X    | X      | O    |
| DELETE  | X    | O      | X    |
| HEAD    | O    | X      | O    |
| OPTIONS | O    | X      | X    |
| CONNECT | X    | X      | X    |
| TRACE   | O    | X      | X    |
