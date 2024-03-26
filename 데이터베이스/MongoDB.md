# MongoDB

NoSQL, Document기반 오픈소스 비관계형 데이터베이스 관리 시스템(DMBS)

- 특징

  - 테이블기반이 아닌 Document기반이라서 빠르다.
  - Json과 유사한 형식인 BSON(Binary Json)형식
  - index지원
  - 분산형 아키텍처

- 장점

  - Schema-less 구조
    - RDBMS는 미리 정의된 스키마를 필요로하나, 몽고디비의 스키마 디자인은 유연한 변화 가능
  - Read/Write 성능이 뛰어남
  - Scale Out 구조
    - 수평적 확장이 뛰어남
  - 사용법이 쉬움

- 단점

  - 트랜잭션이 엄격하지 않음 (ACID기반이 아닌 BASE기반)
  - 데이터 공간소모 (key 중복입력)
  - 각각의 개체이기 때문에 많은 인덱스 사용시 충분한 메모리 확보 필요
  - 데이터 유실 가능성
