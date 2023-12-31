# 신뢰성있는 송수신을 위한 개념

- TCP 연결성립 과정 -> 3 way handshake
- TCP 연결해제 과정 -> 4 way handshake

### Segment Structure

![](https://ifh.cc/g/WHbzsQ.jpg)

- Sequence number (32bit)

  - 패킷송신의 충돌을 방지가능 한 고유한 번호가 할당 된다.

- Flags
  - SYN: 동기화 시퀀스 넘버, 연결 요청 flag
  - ACK: 필드값이 유효함을 나타낸다, 응답 flag
  - FIN: 연결해제 flag

### TCP 연결성립 과정 -> 3 way handshake

1. client -> (syn) -> server

2. server -> (syn, ack) -> client

3. client -> (ack) -> server

#### 전체적인 상태

1. 모두 다 close 상태에서 server 가 연결 준비인 listen 상태로 변하고

2. client 에서 syn을 보내고 syn-sent 상태가 된다.

3. server 에서 요청을 받고 syn-receivde 상태가 되어 syn + ack 을 다시 보낸다.

4. client 에서 established 상태가 되고 ack 를 보내 server도 established 상태가 된다.

### TCP 연결해제 과정 -> 4 way handshake

1. client -> (fin) -> server

2. server -> (ack) -> client

3. server -> (fin) -> client

4. client -> (ack) -> server

#### 전체적인 상태

1. client 에서 server로 fin 을 보낸 후 fin-wait-1 상태가 된다.

2. server에서 ack 를 보내면서 close-wait 상태가 되고 client 는 fin-wait-2 상태가 된다.

3. server 는 last-ack 상태가 되며 fin 을 보낸다.

4. client 가 time-wait 상태가 되면서 ack 를 보내고 server는 closed 상태가 된다.

5. 일정 시간 후에 client 도 closed 상태가 된다.

> time-wait 후 일정시간 뒤에 closed 되는 이유는 지연패킷을 기다리기 위해서 이며 이로 인해 데이터의 무결성을 지킨다.
