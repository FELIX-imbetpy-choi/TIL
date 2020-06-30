![](https://images.velog.io/images/doomchit_3/post/ad1ba345-9439-45c3-b0db-ca957f5f604a/webtriangle.png)

<br/>
<br/>

# 🚦 URL (Uniform Resource Locator) 이란?
 
 ![](https://images.velog.io/images/doomchit_3/post/03b0ae3e-dc60-4a22-a34f-b65e8f9e14cd/uri.png)
 
- **URI(Uniform Resource Identifier, URI)** 란 인터넷에 있는 자원의 위치를 나타내는 유일한 주소이며, 인터넷에서 요구되는 기본조건으로 인터넷 프로토콜에 항상 붙어있다.

- **URI 의 하위개념**으로 `URL`, URN 이 있다.

- 주소 식별 체계인 URI 가 브라우저에서는 주소입력창을 통해 `URL(Uniform Resource Locator)`이란 이름으로 사용된다.

- `URL` 이란 **Uniform Resource Locator** 의 약자이다.
- `URL` 은 **web address** 또는 **문화어로 파일식별자, 유일자원지시기** 라고 불린다.

- **자원(Resource)** 이란 웹페이지, 이미지, 음악파일, 동영상파일 등 웹상에 존재하는 다양한 종류의 리소스를 통칭해 말한다.

- `URL` 은 흔히 웹사이트 주소로 알지만, 주소 뿐 아니라 컴퓨터 네트워크상의 자원을 모두 나타낼 수 있다.

- 주소에 접속하려면 해당 **URL에 맞는 프로토콜**을 알아야 하고, 그와 동일한 프로토콜로 접속해야 한다.

- **FTP 프로토콜**인 경우에는 FTP 클라이언트를 이용해야 하고

- **HTTP**인 경우에는 웹 브라우저를 이용해야 한다. 

- **텔넷**의 경우에는 텔넷 프로그램을 이용해서 접속해야 한다.
- **웹 브라우저**는 URL을 통해 URI(자원식별자) 정보를 추출하여, 웹 상에서 HTTP통신규약을 통해 자원을 찾습니다.

<br/>
<br/>

# 🃏 URL 문법 ( Uniform Resource Locator )


> URL은 스킴에 따라 문법이 모두 다르지만, 아래의 구조를 기반으로 선택적으로 사용한다. 

![](https://images.velog.io/images/doomchit_3/post/4fd06089-a0fb-471e-83f6-6c091fef4505/url.PNG)

![](https://images.velog.io/images/doomchit_3/post/0a01e6a0-cd0f-44f0-8d64-388bd1242140/url2.PNG)


### ① 스킴 ( scheme )
- URL 은 가장 앞( scheme ) 에 자원에 접근할 방법을 정의해 둔 프로토콜 이름을 적는다. (gopher, telnet, ftp, http, usenet 등)
- **웹에서 주로 HTTP 프로토콜**을 사용한다.
- 그 밖에** ftp, mailto(이메일), rtsp(스트리밍)** 과 같은 프로토콜을 사용할 수도 있다.
- 프로토콜 이름 다음에는 프로토콜 이름을 구분하는 구분자인 `:`을 적는다.
- 만약 IP 혹은 Domain name 정보가 필요한 프로토콜이라면 `:` 다음에 `//`를 적는다.
- 프로토콜명 구분자인 `:` 혹은 `//` 다음에는 프로토콜 마다 특화된 정보를 넣는다.
	- 예1) http://www.somehost.com/a.gif - IP 혹은 Domain name 정보가 필요한 형태 ( www.somehost.com에 있는 a.gif를 가리키고 있음 )
	- 예2) ftp://id:pass@192.168.1.234/a.gif - IP 혹은 Domain name 정보가 필요한 형태 ( 192.168.1.234에 있는 a.gif를 가리키고 있음 )
	- 예3) mailto:somebody@mail.somehost.com - IP정보가 필요없는 프로토콜 ( mailto 프로토콜은 단지 메일을 받는 사람의 주소를 나타냄 )

<br/>

### ② 사용자 이름과 비밀번호
- 어떤 서버들은 자신이 가지고 있는 데이터에 접근하기 위해서 사용자의 이름과 비밀번호를 요구한다.
	- ex) ftp://victolee:12345@호스트/asd.xls
- 만약 웹 서버에서 사용자이름과 비밀번호를 요구하는 URL 스킴을 사용함에도 클라이언트가 이를 명시하지 않고 URL에 접근한다면, 기본값으로 "사용자 이름 : anonumous , 비밀번호는 브라우저에서 제공하는 기본 값"을 따르게 된다.

<br/>

### ③ 호스트와 포트
- 하나의  **Host( 컴퓨터 )** 에는 여러 개의 **Process( 프로그램 )** 가 각각의 **Socket( 소켓 )** 을 사용하여 데이터 통신을 하고 있기 때문에, 각각의 소켓을 구분할 필요가 있다.
- 이 때 **소켓을 구분하는 역할을 하는 것이 Port( 포트 )** 이다.
- 서버에는 포트에 따라 소켓이 연결되어 있고, 포트 번호에 따라 다른 프로토콜이 사용될 수 있습니다.
- HTTP 프로토콜에서 포트 번호를 명시하지 않으면, 80번 포트를 기본 값으로 사용한다.


<br/>

### ④ 경로
- 호스트에서 제공하는 자원의 경로를 의미한다.
ex) https://movie.naver.com/movie/running/current.nhn

<br/>

### ⑤ 질의
- Query String 이라고도 한다.
- 클라이언트가 자원을 GET 방식으로 요청할 때, 필요한 데이터를 함께 넘겨 줄 목적으로 사용한다.

<br/>

### ⑥ 프래그먼트
- HTML에는 각각의 요소에 id 속성을 부여할 수 있는데, URL에 프래그먼트를 전달하면 페이지가 해당 id가 있는 곳으로 스크롤이 이동하게 된다.

이 글의 URL에 프래그먼트를 추가하면, 가장 마지막으로 이동할 것입니다.
ex) http://victorydntmd.tistory.com/287#bottom

<br/>
<br/>

# 참고📚
[URL,URI 구조 - victorydntmd](https://victorydntmd.tistory.com/287)
[URI, URL 차이 정리](https://velog.io/@pa324/%EA%B0%9C%EB%B0%9C%EC%83%81%EC%8B%9D-URI-URL-%EC%B0%A8%EC%9D%B4-%EC%A0%95%EB%A6%AC)