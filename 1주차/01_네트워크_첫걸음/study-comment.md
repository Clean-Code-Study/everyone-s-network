# 1장 네트워크 첫걸음

## 01. 네트워크의 구조

### 1. 컴퓨터 네트워크란?

- 컴퓨터 두 대 이상 연결되어 있으면 컴퓨터 네트워크가 되고, 컴퓨터 간에 필요한 데이터(정보)를 서로 주고받을 수 있다.
    - 컴퓨터 간의 데이터(파일) 전송, 웹 사이트 열람, 메일 송수신 등
- 인터넷: 전 세계의 큰 네트워크부터 작은 네트워크까지를 연결하는 거대한 네트워크

### 2. 패킷이란?

- 네트워크나 인터넷에서 데이터를 주고받으려면 규칙이 있어야 한다. 그 규칙에는 패킷(packet)을 사용한다.
- 패킷: 컴퓨터 간에 데이터를 주고받을 때 네트워크를 통해 전송되는 데이터의 작은 조각
- 큰 데이터가 있더라도 작게 나누어서 보내는 게 규칙이다.
- 왜 큰 데이터를 그대로 보내지 않는지?
    - 데이터가 네트워크의 대역폭을 너무 많이 차지(점유)해서 다른 패킷의 흐름을 막을 위험이 있다.
    - 대역폭: 일반적으로는 네트워크에서 이용 가능한 최대 전송 속도로 정보를 전송할 수 있는 단위 시간당 전송량을 말한다.
- 작게 나눈 그대로라면 목적지에 도착하더라도 볼 수 없을 것이다. 따라서 원래대로 되돌리는 작업이 필요하다.
- 일단 목적지로 보낸 패킷이 전송한 순서대로 도착하지 않을 수도 있다. 또, 패킷이 전송될 때 네트워크가 지연되어서 늦게 도착하거나 패킷이 누락되기도 한다.
- 그렇게 되면 원래대로 되돌릴 수 없기 때문에 송신 측에서 수신 측으로 패킷을 보낼 때는 각 패킷에 순서대로 번호를 붙여서 보내고, 번호에 맞춰 정렬한다.

## 02. 정보의 양을 나타내는 단위

### 1. 비트와 바이트란?

- 디지털 데이터: 모든 컴퓨터는 0과 1만 다루는데, 그 0과 1의 집합을 말한다.
- 비트(bit): 0과 1의 정보를 나타내는 최소 단위
- 바이트(byte): 0 또는 1인 숫자 여덟 개를 모아 표시한 것
- 컴퓨터는 기본적으로 바이트 단위로 데이터를 읽고 쓰는 작업을 하기 때문에, 디지털 데이터를 만들 때는 8비트를 1바이트로 다루는 것이 좋다.
- 숫자와 문자의 대응표를 문자 코드라고 한다.

## 03. 랜과 왠

### 1. 랜과 왠 차이

- 랜(LAN): Local Area Network(근거리 통신망)
    - 건물 안이나 특정 지역을 범위로 하는 네트워크
- 왠(WAN): Wide Area Network(광역 통신망)
    - 지리적으로 넓은 범위에 구축된 네트워크
    - 인터넷 서비스 제공자(ISP)가 제공하는 서비스를 사용하여 구축된 네트워크
- 인터넷 서비스 제공자(ISP): 인터넷 상용 서비스 사업을 하는 KT, U+ 등..

|  | 랜 | 왠 |
| --- | --- | --- |
| 범위 | 좁다(건물이나 특정 지역) | 넓다(랜과 랜을 연결) |
| 속도 | 빠르다 | 느리다 |
| 오류 | 적다  | 많다 |

## 04. 가정에서 하는 랜 구성

### 1. 가정에서의 네트워크 구성

- 인터넷을 사용하기 위해 결정해야 할 것
    - 인터넷 서비스 제공자(ISP)
    - 인터넷 회선 (광랜을 주로 사용)
- 인터넷 공유지: boradband router
    - 가정이나 소규모 기업에서 인터넷에 접속할 때 사용
- 연결 방식은 크게 유선과 무선 연결로 나뉜다.
    - 랜 케이블 필요: 유선
    - 랜 케이블 불필요: 무선

## 05. 회사에서 하는 랜 구성

### 1. 소규모 회사에서의 네트워크 구성

- DMZ: 외부에 서버를 공개하기 위한 네트워크
    - 웹 사이트를 외부 사용자에게 공개하려면 웹 서버를 외부에 공개
    - 외부 사용자와 메일을 주고받으려면 메일 서버를 공개
    - 외부에서 도메인 이름을 사용하여 회사의 서버에 접속하려면 DNS 서버를 공개 등
    - 일반적인 가정의 네트워크에서는 서버를 외부에 공개할 필요가 없기 때문에 공개하지 않는다.
- 회사에서 서버를 운영하기 위해?
    - 온프레미스(on-premise)
        - 서버를 사내에 설치
        - 데이터 센터에 둠
    - 클라우드에 둠
- 데이터 센터: 대량의 데이터를 보관하기 위해 데이터 센터 서버나 네트워크 기기를 설치한 전용 시설
- 클라우드: 인터넷을 통해 소프트웨어나 하드웨어 등의 컴퓨팅 서비스를 제공하는 것으로 인터넷에 접속하기만 하면 언제 어디서든 이용할 수 있다.
- 사내에서 서버를 운영하는 경우에는 회사 내에 서버 장비실을 두고 그곳에 랙(선반)을 설치한다.
- 랙 안에는 랙에 설치하기 적합한 형태와 크기를 가진 서버, 라우터, 스위치를 설치할 수 있다.
- 각 서버는 스위치와 연결하여 서로 통신할 수 있다.