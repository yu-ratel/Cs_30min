# OSI 7 계층

네트워크에서 통신이 일어나는 과정을 7단계로 나눈 것

- 응용 계층(Application Layer)

  - 최종 목적지, 사용자와 연결되어 네트워크 접근을 도우는 계층
  - 인터페이스 제공
  - 입력받은 정보 하위계층에 전달
  - HTTP, SMTP...

- 표현 계층(Presentation Layer)

  - 데이터의 표현방식결정
  - 데이터 인코딩, 디코딩
  - JPEG, ASCII, GIF

- 세션 계층(Session Layer)

  - 컴퓨터간 연결인 세션의 생성과 유지를 관리하는 계층
  - API, Sockket

- 전송 계층(Transport Layer)

  - 데이터의 신뢰성있는 전송을 위한 계층
  - TCP, UDP

- 네트워크 계층(Network Layer)

  - 데이터 전송경로, 순서등 관리
  - 패킷단위 분할 전송, 수신시 결합
  - IP주소를 사용한 데이터 전송
  - 라우터

- 데이터 링크계층(DataLink Layer)

  - 물리계층을 통해 송수신되는 정보를 관리하여 통신흐름관리
  - 패킷을 프레임으로 구성하고 검사, 수정
  - MAC주소를 사용한 데이터 전송
  - 브리지, 스위치, 이더넷 등

- 물리계층 (Physical Layer)
  - 물리적인 장비로서 데이터를 물리적인 신호로 변환하여 전달하는 계층
  - 물리적인 신호를 사용 (0, 1 === on off)
  - 통신케이블, 리퍼터,허브 등

# TCP/IP 4계층

대부분 통신에 실제로 사용하는 네트워크

- 응용 계층 (Application Layer) OSI 5, 6, 7

  - TCP/UDP 기반의 응용 프로그램을 구현할 때 사용
  - HTTP, SSH 프로토콜

- 전송 계층 (Transport Layer) OSI 4

  - 통신 노드간 연결을 제어하고, 신뢰성있는 데이터 전송 담당
  - TCP, UDP 프로토콜

- 인터넷 계층 (Internet Layer) OSI 3

  - 통신 노드간의 IP패킷을 전송하는 기능, 라우팅 기능
  - IP 프로토콜

- 네트워크 엑세스 (Networt Access Layer) OSI 1, 2
  - 물리적인 주소로 MAC 사용
  - LAN, 패킷망 등 사용
