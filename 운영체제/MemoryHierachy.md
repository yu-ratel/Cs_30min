# Memory hierachy (메모리 계층)

> 빠른순으로 레지스터, 캐시메모리, 램, HDD, SSD로 구성되어있다.

## Register

CPU 바로옆에 위치한 메모리로 가장 빠른 메모리 => CPU가 사용할 데이터를 저장

- 전용/범용 레지스터
- 사용자 가시/불가시 레지스터
- 데이터, 주소, 상태 레지스터

## CacheMemory

CPU와 mainMemory사이에 위치한 고속 기억장치
직업 읽거나 쓸 수 없고 MMU(하드웨어 메모리 관리시스템)이 내부적으로 제어함.
L1 부터 3까지 갈수록 용량이 커지며 속도가 느리다.

시간적 지역성과 공간적 지역성을 고려해 미리 캐싱

- 시간적 지역성
  - 한번 접근했던 데이터는 다시 접근할 가능성이 높다.
- 공간적 지역성
  - 가까운 주소에 연속적으로 접근된 데이터가 있다면 현재 데이터에도 접근할 가능성이 높다.
    > 가까운 주소의 블록 단위로 데이터를 가져옴
