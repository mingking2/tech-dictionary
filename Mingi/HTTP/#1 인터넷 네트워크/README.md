# #1 인터넷 네트워크

##  인터넷 통신
- 컴퓨터 간의 통신을 할 때 중간에 인터넷이 있다.
- 복잡한 인터넷 망을 어떤 규칙으로 어떻게 넘어가는가?
<br><br>
<br><br>
## IP(Internet Protocol)
- **인터넷 프로토콜 역할**
    - 지정한 IP 주소(IP Address)에 데이터 전달
    - 패킷(Packet)이라는 통신 단위로 데이터 전달
<br><br>

- **IP 패킷 정보**
    ![Alt text](./image/IP%20패킷%20정보.png)

    - 클라이언트 패킷 전달
    ![Alt text](./image/클라이언트%20패킷%20전달.png) 

    - 서버 패킷 전달
    ![Alt text](./image/서버%20패킷%20전달.png)

- **IP 프로토콜의 한계**
    - 비연결성
        - 패킷을 받을 대상이 없거나 서비스 불능 상태여도 패킷 전송
    <br><br>
    - 비신뢰성
        - 중간에 패킷이 사라지면?
        - 패킷이 순서대로 안오면?
    <br><br>
    - 프로그램 구분
        - 같은 IP를 사용하는 서버에서 통신하는 애플리케이션이 둘 이상이면?
<br><br>
<br><br>
## TCP, UDP

**인터넷 프로토콜 스택의 4계층**

![Alt text](./image/인터넷%20프로토콜%20스택의%204계층.png)
<br><br>

- **프로토콜 계층**

    ![Alt text](./image/프로토콜%20계층.png)
    <br><br>

- **TCP/IP 패킷 정보**

    ![Alt text](./image/TCP.IP%20패킷%20정보.png)
    <br><br>

- **TCP 특징**
    - 전송 제어 프로토콜(Transmission Control Protocol)
<br><br>
    - 연결지향 - TCP 3 way handshake (가상 연결)
        ![Alt text](./image/연결지향.png)
    - 데이터 전달 보증
        ![Alt text](./image/데이터%20전달%20보증.png)
    - 순서 보장
        ![Alt text](./image/순서%20보장.png)
<br><br>
    - 신뢰할 수 있는 프로토콜
    - 현재는 대부분 TCP 사용
<br><br>
<br><br>

- **UDP 특징** <- 요즘 뜬다
    - 사용자 데이터그램 프로토콜(User Datagram Protocol)
    <br><br>
    - 하얀 도화지에 비유(기능이 거의 없음)
    - 연결 지향 X - TCP 3 way handshake X
    - 데이터 전달 보증 X
    - 순서 보장 X
    - 데이터 전달 및 순서가 보장되지 않지만, 단순하고 빠름
    - 정리
        - IP와 거의 같다. +PORT +체크섬 정도만 추가
        - 애플리케이션에서 추가 작업 필요
<br><br>
<br><br>
## PORT
- **한번에 둘 이상 연결해야 하면?**
    ![Alt text](./image/한번에%20둘%20이상%20연결해야한다.png)
<br><br>
- **패킷 정보**
    ![Alt text](./image/패킷%20정보.png)
<br><br>
- **PORT - 같은 IP 내에서 프로세스 구분**
    ![Alt text](./image/같은%20IP%20내에서%20프로세스%20구분.png)

<br><br>
- **PORT**
    - 0 ~ 65535 할당 가능
    - 0 ~ 1023: 잘 알려진 포트, 사용하지 않는 것이 좋음
        - FTP - 20,21
        - TELNET - 23
        - HTTP - 80
        - HTTPS - 443
<br><br>
<br><br>
## DNS
- **IP는 기억하기 어렵다.**
- **IP는 변경될 수 있다.**
<br><br>
- **DNS**
    - 도메인 네임 시스템(Domain Name System)
        - 전화번호부
        - 도메인 명을 IP 주소로 변환
<br><br>

    ![Alt text](./image/DNS%20사용.png)