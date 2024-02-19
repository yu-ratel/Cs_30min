# Cs_30min

👀 [Json](Json.md)

👀 [XML](XML.md)

👀 [API](API.md)

👀 [Cloud](Cloud.md)

👀 [CICD](ClCD.md)

👀 [Class_Object_Instance](Class_Object_Instance.md)

👀 [Static](Static.md)

👀 [Overloading_Overrding](Overloading_Overrding.md)

👀 [Abstraction](Abstraction.md)

이번주 스터디 내용

네트워크

- RESTful 이란 무엇이며, 이것에 대해 아는대로 설명해주세요.

운영체제

- 세마포어와 뮤텍스의 차이에 대해 설명해보세요.

데이터베이스

- Redis에 대해서 간단하게 설명해주세요.
- Redis와 Memcached의 차이에 대해서 설명해주세요.

컴퓨터구조

- 컴퓨터의 구성 요소는?

실행순서를 위한 동기화를 위해서 세마포어가 필요하다.

세마포어는 작업순서 => 호출순서가 중요한데 모니터는 개발자에게 맡기는게 아니라 모니터 자체로서 호출순서를 보장해준다.
프로시저 기법 (공유데이터1개) << 모니터

엔트릭큐 (블록된 프로세스)

프로시저 - 공유자원에 대해 호출할 수 있는 연산을 모아놓은 집합(개발자가 해야함) === class의 private fild 와 같지않을까?
**ava 인스턴스가 다 모니터이고 메서드가 다 프로시저다.**

js는 왜 싱글스레드이고 그러면 이벤트루프 비동기는 누가 담당하는걸까?
이벤트루프 => Node, web
멀티스레드로 해도되지않나? -> 난이도 문제, 간단한 비동기 프로그래밍 언어의 개요와 연관이있음 (쉽게)

메인보드 부팅 바이로스 롬
컴퓨터 실행

마이크로 오퍼레이션(stoer, loder) 물리적수준 명령어들의 조합이지만 트랜젝션의 ACID는 갖고있지 않음 => 데이터 무결성이 깨질 수 있음
요즘에는 하드웨어적인 연산을 보장해주어 Os의 동기화를 도와준다. [참조](https://ko.wikipedia.org/wiki/%EB%A7%88%EC%9D%B4%ED%81%AC%EB%A1%9C_%EC%98%A4%ED%8D%BC%EB%A0%88%EC%9D%B4%EC%85%98)
