# 2023-08-02 WEB SERVER 구조

## 네트워크

서로 다른 컴퓨터들이 통신을 할 때 물리적 또는 무선으로 연결되어있어야 한다. 이러한 연결로 모든 현대 컴퓨터들이 연결을 지속할 수 있다. 컴퓨터의 수가 많아질 수록 물리적 연결 또한 많아져야 한다. 만약 이더넷 케이블로만 연결을 한다면 10대의 컴퓨터를 연결하면 총 45개의 케이블이 필요하게 된다. 이 문제를 해결하기 위해 탄생한 게 라우터 이다. 라우터는 컴퓨터에서 보낸 신호를 다른 올바른 컴퓨터로 보내는 역할을 하는 소형 컴퓨터이다. 라우터는 서로 다른 라우터 끼리 연결이 가능하며 이로 인해 더 많은 네트워크를 구성할 수 있다.

![Untitled](2023-08-02%20WEB%20SERVER%20%E1%84%80%E1%85%AE%E1%84%8C%E1%85%A9%2063879e68649a48bca89f8798c0eec144/Untitled.png)

인터넷을 더 멀리 멀리 보내려면 어떻게 해야 할까? 바로 모뎀을 사용해야 한다. 모뎀은 디지털 신호를 아날로그 신호로 또는 아날로그 신호를 디지털 신호로 변환해주는 기기이다. 디지털 신호는 멀리 보낼 수록 신호 전달이 잘 되지 않는다. 그렇기에 모뎀을 통해 아날로그 신호 또는 광 신호로 바꾸어 전달한다.

![Untitled](2023-08-02%20WEB%20SERVER%20%E1%84%80%E1%85%AE%E1%84%8C%E1%85%A9%2063879e68649a48bca89f8798c0eec144/Untitled%201.png)

모뎀은 인터넷 서비스 제공 업체(ISP, 우리나라 대표 ISP: KT, SK브로드밴드, LG U+)에 연결된다. ISP는 특수한 라우터들을 관리하고 다른 ISP 라우터에도 엑세스 할 수 있게 하는 회사이다. 이렇게 다른 ISP 네트워크로 연결되며 전체 네트워크 인프라를 구성한다. 이것을 인터넷이라고 한다.

![Untitled](2023-08-02%20WEB%20SERVER%20%E1%84%80%E1%85%AE%E1%84%8C%E1%85%A9%2063879e68649a48bca89f8798c0eec144/Untitled%202.png)

## 컴퓨터 찾기

컴퓨터에 메세지를 보내려면 메세지를 받을 특정 컴퓨터를 지정해야 한다. 이때 인터넷 주소가 필요한데 이를 IP 주소라고 한다. 주소는 점으로 구분 된 네 개의 숫자로 구성된 주소이다. ex) 192.168.0.1

하지만 IP주소는 사람이 기억하기 어렵다. 이를 해결하기 위해 도메인 네임을 이용한다. 도메인 네임을 이용하여 사람이 읽을 수 있는 IP 주소의 이름을 지정할 수 있다. 도메인 네임은 DNS(도메인 네임 시스템)에 의해 호스트의 네트워크 주소로 바뀌어 진다. 구글의 도메인 주소는 [google.com](http://google.com) 이고 IP 주소는 [142.250.190.78](http://142.250.190.78) 이다.

## 웹페이지, 웹사이트, 웹 서버 그리고 검색엔진의 차이

### 웹 페이지

웹 페이지는 브라우저를 통해 보여지는 단순한 문서이다. 이런 문서는 HTML 언어로 쓰여진다. 

### 웹사이트

웹사이트는 유일한 도메인 이름을 같이 사용하는 연결된 웹 페이지들의 모음이다. 

### 웹 서버

웹 서버는 한 개 이상의 웹사이트를 호스팅하는 컴퓨터이다. 유저의 request마다 호스팅하는 웹사이트에서 유저의 브라우저로 웹 페이지를 보내는 역할을 한다.

### 검색 엔진

검색 엔진은 웹 페이지를 다른 웹사이트에서 찾을 수 있게 도와주는 특별한 종류의 웹사이트이다.

## 웹 서버

### 서버의 종류

HTTP 서버 : 웹 서버라고 불린다. 클라이언트의 요청에 웹 페이지를 응답해주는 역할을 한다.

DB 서버 : 데이터베이스만을 다루는 서버이다.

파일 서버 (FTP, SAMBA, NFS) : 인터넷으로 파일을 송수신할 수 있는 서버이다.

메일 서버 (SMTP) : 메일을 전송하고 받을 수 있는 서버이다.

### 웹 서버

웹 서버는 하드웨어 측면에서는 웹 서버의 소프트웨어와 컴포넌트 파일들을 저장하는 컴퓨터이다. 웹 서버는 인터넷에 연결되어 웹에 연결된 다른 기기들이 웹 서버의 데이터를 주고받을 수 있도록 한다. 소프트웨어 측면에서는 웹 사용자들이 어떻게 호스트 파일들에 접근하는지 관리한다. 웹 서버는 정적 또는 동적인 웹 페이지를 전달할 수 있다. 정적 웹페이지는 서버에 저장된 파일을 브라우저에 전달하며 응답할 수 있고, 동적 웹페이지는 웹 서버의 추가적인 소프트웨어 WAS, DB를 활용하여 파일을 전송하기 전에 업데이트를 하고 전송을 한다.

![Untitled](2023-08-02%20WEB%20SERVER%20%E1%84%80%E1%85%AE%E1%84%8C%E1%85%A9%2063879e68649a48bca89f8798c0eec144/Untitled%203.png)

웹서버에는 NGINX, APACHE 등이 있다.

### 웹 서버의 동적 페이지 호출 방법

웹 서버에서 동적 페이지를 응답하는 방법은 여러가지 있지만 보통 3가지가 있다.

CGI 방식: CGI는 정보를 주고받는 규격을 의미한다. C, C++, PYTHON 등으로 만들어진 CGI 프로그램을 직접 호출하여 개별 프로세스를 생성하는 방식이다. CGI는 각각의 클라이언트 요청에 대하여 독립적인 별도의 프로세스가 생성된다는 것이 문제점이다. 요청이 많아질수록 시스템에 부하를 많이 주게 된다. 현재는 CGI 방식은 거의 사용되고 있지 않다.

웹 서버에 인터프리터 내장:  웹 서버에 인터프리터를 내장 시켜서 애플리케이션을 실행시키는 방법이다. 서버에서 실행시키기 때문에 리소스 관리에도 편하고 실행속도가 빠르다.  일반적으로 많이 사용되며 간단한 동적 웹페이지에 유리하다.

WAS 방식:  웹 서버가 직접 프로그램을 호출하기보다는 웹 애플리케이션 서버를 통해서 간접적으로 웹 애플리케이션 프로그램을 실행한다. 

### 웹 애플리케이션 서버

웹 서버로부터 오는 동적인 요청을 처리하고 그 결과를 웹 서버로 반환하는 역할을 하는 서버를 말한다. 주로 페이지 생성을 위한 프로그램 실행과 데이터베이스 연동 기능을 처리한다.

![Untitled](2023-08-02%20WEB%20SERVER%20%E1%84%80%E1%85%AE%E1%84%8C%E1%85%A9%2063879e68649a48bca89f8798c0eec144/Untitled%204.png)

웹 애플리케이션 서버에는 Apache Tomcat, JBoss, WebLogic 등이 있다.

웹 어플리케이션 서버로도 정적 페이지를 처리할 수 있어 웹 서버 없이 단독으로 사용할 수 있다. 하지만 웹 서버가 정적 페이지를 처리하는 것과 웹 어플리케이션 서버가 정적 페이지를 처리하는 것의 성능 부하차이가 다르다. 그렇기에 웹 서버와 웹 애플리케이션 서버를 같이 사용하는 것이 더 좋다. 또한 보안에서도 따로 사용하는 것이 더 좋다.

## 다음 시간에..

리엑트와 EXPRESS 연동 방법 ..

리엑트와 스프링 연동 방법 ..

## 참고 문헌

### 네트워크

[인터넷은 어떻게 동작하는가? - Web 개발 학습하기 | MDN](https://developer.mozilla.org/ko/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work)

[모뎀](https://ko.wikipedia.org/wiki/모뎀)

[모뎀과 라우터의 차이란?알기 쉽게 해설합니다!](https://dkel.tistory.com/1431)

[[전자기초]MODEM 이란 무엇인가?](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=ch0ry&logNo=100090969488)

### 컴퓨터 찾기

[도메인 네임 시스템](https://ko.wikipedia.org/wiki/도메인_네임_시스템)

[도메인 네임](https://ko.wikipedia.org/wiki/도메인_네임)

### 웹페이지, 웹사이트, 웹 서버, 그리고 검색엔진의 차이

[웹페이지, 웹사이트, 웹서버 그리고 검색엔진의 차이는 무엇일까요? - Web 개발 학습하기 | MDN](https://developer.mozilla.org/ko/docs/Learn/Common_questions/Web_mechanics/Pages_sites_servers_and_search_engines)

### 웹 서버

[네트워크 서버 종류 및 특징 비교 - TECH 블로그피디아](https://techblogpedia.com/네트워크-서버-종류-특징-비교/)

[웹 서버란 무엇일까? - Web 개발 학습하기 | MDN](https://developer.mozilla.org/ko/docs/Learn/Common_questions/Web_mechanics/What_is_a_web_server)

[[WEB] 🌐 웹 서비스 구조 (Web서버 / 웹컨테이너 / WAS) 정리](https://inpa.tistory.com/entry/WEB-🌐-웹-서비스-구조-정리)

[[서버]웹 서버와 웹 어플리케이션의 차이](https://studium-anywhere.tistory.com/19)

[웹 어플리케이션 서버](https://rrhh234cm.tistory.com/456)

[웹서버(Web Server) 와 웹 어플리케이션 서버 (WAS)](https://binux.tistory.com/32)

[WAS와 Server의 차이? 그리고 Web Container 란?](https://doozi316.github.io/web/2020/09/13/WEB26/)