![](https://images.velog.io/images/doomchit_3/post/92731a47-c7f0-435f-97be-6c32597aa039/bitcoin-domains.jpg)

# 🏡 도메인네임(Domain Name) 이란?

![](https://images.velog.io/images/doomchit_3/post/4a97780b-488a-46af-9c9c-cb717d28d82d/do1.jpg)

- `Domain Name` 은 웹사이트의 주소, 즉 웹사이트를 찾기위한 고유한 **문자형 주소체계** 를 말한다.

- https://www.naver.com , **http** 는 _통신방식(규칙)_을 말하며 **www** 는 _호스트(host)_ 이며 **naver.com** 이 실제 도메인주소이다.

- 통신망 환경에서 컴퓨터나 통신장비간 통신에 최적화된 주소체계는 **IP Adress** 이다. 하지만 이는 숫자로 이루어져 사람이 기억하기 힘들다. 이런 단점을 보완해 등장한 것이 문자형주소체계인 `Domain name` 이다.

- 문자주소체계인 도메인주소는 **상호맵핑되는 구조** 를 가진다. (IP Adress ↔ Domain name )

- 도메인만 알면 자동으로 통신과정 중 IP 로 변환되어 컴퓨터간 통신할 수 있게 자동처리 해주는 서비스를 **DNS(Domain Name Service)** 라고한다.

<br/>
<br/>

# 📬도메인 체계

![](https://images.velog.io/images/doomchit_3/post/0cdd0ebd-f8d1-48b1-912c-4e675df60b64/do2.gif)

- 도메인은 `.` 또는 `루트(root)`라 불리는 도메인 이하에 위의 그림과 같이 역트리(Inverted tree)구조로 구성되어 있다.
- 루트 도메인 바로 아래의 단계를 1단계 도메인 또는 최상위 도메인(TLD, Top Level Domain)이라고 부르며, 그 다음 단계를 2단계 도메인(SLD, Second Level Domain)이라고 부른다.

<br/>
<br/>

# 🎈 도메인 종류
- 도메인에는 **국가도메인(ccTLD, country code Top Level Domain)** 과 **일반도메인(gTLD, generic Top Level Domain)** 이 있다.
- `국가도메인` 은 인터넷 상에서 국가를 나타내는 도메인으로 ‘.kr(대한민국) .jp(일본), .cn(중국), .us(미국) 등 영문으로 구성된 영문 국가도메인이 있습니다. 또한 ‘.한국(대한민국)’, ‘중국(중국), .러시아(러시아), .이집트(이집트)처럼 자국어 국가도메인이 있다.
- `일반도메인` 은 ‘.com(회사)’, ‘.net(네트워크 관련기관)’, ‘org(비영리기관)’, ‘.biz(사업)’ 등 등록인의 특성에 따라 사용할 수 있는 도메인이다.

### ① 국가 최상위 도메인 (ccTLD)

> 인터넷 상에서 국가를 나타내는 영문 및 자국어 도메인 (ccTLD, country code Top Level Domain)

- 2자리 영문 국가코드 또는 자국어 국가코드로 이뤄짐.
- 관리기관 : https://www.iana.org/domains/root/db

<br/>

### ②일반 최상위 도메인 (gTLD)

> 조직, 목적, 분류 등 명칭을 영문약자로 표현한 최상위 도메인 (gTLD, genertic Top Level Domain) 

- 영문은 3자리 이상, 영문 외 다국어는 2자리 이상으로 이뤄짐
- 관리기관 : https://xn--3e0bx5euxnjje69i70af08bea817g.xn--3e0b707e/jsp/popup/domainGTLD.jsp

<br/>
<br/>

# 참고📚
[위키백과](https://ko.wikipedia.org/wiki/%EB%8F%84%EB%A9%94%EC%9D%B8_%EB%84%A4%EC%9E%84)
[mixedcode](http://mixedcode.com/Article/Index?aidx=1050)
[한국인터넷정보센터](https://xn--3e0bx5euxnjje69i70af08bea817g.xn--3e0b707e/jsp/resources/domainInfo/domainInfo.jsp)