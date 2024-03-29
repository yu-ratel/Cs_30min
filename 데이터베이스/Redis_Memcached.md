# 📝 Redis (Remote Dictionary Server)

일종의 NoSQL로서 key - value 구조의 데이터 관리 시스템

- 특징
  - 오픈소스 기반의 인-메모리DB 구조 저장소로서 메모리에 데이터를 저장한다.
    > 별도의 쿼리문 없이, 일반 ssd에 데이터를 쓰는 구조가 아니기에 빠른 속도로 처리할 수 있다. (ssd는 제일 낮은 효능 그위가 dram)
  - 다양한 데이터 구조 지원 (문자열, 해시, 리스트 등)
  - 메모리 기반이지만 영속성을 보장하기 위해 스냅샷, AOF(명령이 실행 될 때 마다 파일에 기록되는 형식)을 디스크에 저장시켜 비휘발성인 보존이 가능하다.
  - 싱글 스레드
  - 트랜잭션

# 📝 Memcached

분산 메모리 캐싱 시스템으로 인-메모리 데이터 저장소를 사용하며 redis보다 명료하고 단순함을 위하여 개발되었다.

### Redis vs Memcached

둘다 사용하기 쉽고 고성능을 제공하지만, redis는 더 다양한 데이터 구조와 기능을 제공하고<br>
memcached는 단순하고 높은 성능에 초점을 맞추어 나온 만큼 상황에 따라 사용하는 것이 좋다.

- 공통점
  - 데이터를 메모리에 저장하기에 디스크 기반의 DB보다 빠르다. (인-메모리 캐싱)
  - 간단한 key - value 구조
  - 다양한 언어 지원
  - 분산 아키텍처 (확장성)

> 오늘 날 redis는 실행을 제외한 부분적으로 멀티 스레드를 지원한다 그렇기에 atomic한 싱글 스레드는 유지하면서 속도는 빨라졌다.

# 참고사이트

- https://junuuu.tistory.com/746
  > redis 도 멀티 스레드?
