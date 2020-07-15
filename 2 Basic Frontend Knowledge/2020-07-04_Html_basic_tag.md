# 🎈 HTML5 란
- **HTML (HyperText Markup Language)** 은 웹페이지에 자원을 나타내기 위한 언어이며, HTML 태그를 통해 정보를 구조화 한다.

- **`HTML5`** 는 2014년 10월 확정된 웹 표준으로 아래와 같은 기능들이 추가되었다.
	- **멀티미디어(Multimedia)** : 플래시 같은 플러그인 없이도 비디오 및 오디오 기능을 자체적으로 지원
	- **그래픽(Graphics & Effects)** : SVG, 캔버스를 사용한 2차원 그래픽 / CSS3, WebGL을 사용한 3차원 그래픽을 지원
	- **통신(Connectivity)** : HTML은 단방향 통신만이 가능하였으나, HTML5는 서버와의 소켓 통신을 지원하므로 서버와의 양방향 통신이 가능
	- **디바이스 접근(Device acess)** : 카메라, 동작센서 등의 하드웨어 기능을 직접적으로 제어할 수 있다.
	- **오프라인 및 저장소(Offline & Storage)** : 오프라인 상태에서도 애플리케이션을 동작시킬 수 있으며, 이는 HTML5가 플랫폼으로서 사용될 수 있음을 의미한다.
	- **시맨틱 태그(Semantics)** : HTML 요소의 의미를 명확히 설명하는 시맨틱 태그를 도입하여 브라우저, 검색엔진, 개발자 모두에게 콘텐츠의 의미를 명확히 설명할 수 있으며, 이를 통해 HTML 요소의 의미를 명확히 해석하고 그 데이터를 활용할 수 있는 시맨틱 웹을 실현할 수 있다.
	- **CSS3** : HTML5는 CSS3를 지원한다.

- HTML document는 .html 확장자를 갖는 순수한 텍스트 파일이다. 

- 따라서 메모장 등으로도 편집할 수 있으나 다양한 기능을 제공하는 editor 또는 IDE 를 사용하는 것이 일반적이다. 

- HTML5 문서는 반드시 `<!DOCTYPE html>` 으로 시작하여 문서 형식(document type)을 HTML5 로 지정한다.

- 실제적인 HTML document은 2행부터 시작되는데 `<html> 과 </html>` 사이에 기술한다.

- `<head>와 </head>` 사이에는 **document title, 외부 파일의 참조, 메타데이터의 설정** 등이 위치하며 이 정보들은 브라우저에 표시되지 않는다.

- 웹브라우저에 출력되는 모든 요소는 `<body> 와 </body>` 사이에 위치한다.

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Hello World</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>안녕하세요! HTML5</p>
  </body>
</html>
```

<br/>
<br/>

# 👓 HTML5 기본문법
### ① Element
`HTML요소(Element)` 는 **시작태그(start tag)** 와 **종료태그(end tag)** 또 태그 사이에 위치한 **content** 로 구성된다.

![](https://images.velog.io/images/doomchit_3/post/61a4515d-0642-4157-b766-1af56e4e7940/image.png)

- HTML document는 요소(Element)들의 집합으로 이루어진다.

- 태그는 대소문자를 구별하지 않으나 W3C: World Wide Web Consortium에서는 HTML4의 경우 소문자를 추천하고 있으므로 HTML5에서도 소문자를 사용하는 것이 일반적이다.

<br/>

### ② Nested Element
요소는 다른 요소를 포함하면서 정보를 나타내는데, 이 때 요소의 관계를 **부자관계** 라고 하며, `요소의 중첩(Nested Element)` 이라 한다.

```
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h1>Hello</h1>
    <p>world!</p>
  </body>
</html>
```
- 위의 코드를 보면 html 요소는 body 요소를 포함하고, body 요소는 h1 과 p 요소를 포함한다.

<br/>

### ③ Empty Element
`빈요소(Empty Element)` 란 컨텐츠를 가질 수 없는 요소를 말한다. 빈요소는 컨텐츠가 없고, 어트리뷰트 만을 가질 수 있다.

```
<meta charset="utf-8">
```
- 빈 요소 중 대표적인 요소는 다음과 같다. ( br / hr / img / input / link / meta )

<br/>

### ④ Attribute
`어트리뷰트(Attribute)` 란 요소의 성질을 정의하는 명세이다. 요소는 어트리뷰트를 가질 수 있고, 이는 추가정보(이미지경로, 이름) 를 표시한다.

![](https://images.velog.io/images/doomchit_3/post/cae37bf3-005f-4b95-84fa-b68ebde0471e/image.png)

```
<img src="html.jpg" width="104" height="142">
```

- 예제 소스에서 어트리뷰트는 img 파일의 경로, 파일명, 이미지 너비, 높이 정보를 브라우저에 알린다.

<br/>

### ⑤ Global Attribute
`글로벌 어트리뷰트(Global Attribute)` 는 모든 HTML 요소가 공통으로 사용할 수 있는 어트리뷰트다. 자주 사용되는 글로벌 어트리뷰트는 아래와 같다.


- **id** : 유일한 식별자(id)를 요소에 지정한다. 중복 지정이 불가하다.
- **class** : 스타일시트에 정의된 class를 요소에 지정한다. 중복 지정이 가능하다.
- **hidden** : css의 hidden과는 다르게 의미상으로도 브라우저에 노출되지 않게 된다.
- **lang** : 지정된 요소의 언어를 지정한다. 검색엔진의 크롤링 시 웹페이지의 언어를 인식할 수 있게 한다.
- **style** : 요소에 인라인 스타일을 지정한다.
- **tabindex** : 사용자가 키보드로 페이지를 내비게이션 시 이동 순서를 지정한다.
- **title** : 요소에 관한 제목을 지정한다.

<br/>

### ⑥ Comments
주석(comment)는 주로 개발자에게 코드를 설명하기 위해 사용되며 브라우저는 주석을 화면에 표시하지 않는다.

```
<!--주석은 화면에 표시되지 않는다.-->
<p>요소는 화면에 표시 된다.</p>
```

<br/>
<br/>

# 🎇 HTML5 기초태그

## ① 문서 형식 정의 Tag
`문서 형식 정의 (Document Type Definition, DTD) 태그` 는 출력할 **페이지의 형식을 브라우저에 전하는 태그** 이다. 문서의 최상위에 위치해야 하고, 대소문자를 구별하지 않는다.

- **HTML5**
```
<!DOCTYPE html>

```
- **HTML 4.01**
```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```
- **XHTML 1.0**
```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```


## ② html Tag
- `html 태그` 요소의 부모 요소이며 웹페이지에 단 하나만 존재한다. 모든 요소는 html 요소의 자식 요소이며 html 요소 내부에 기술해야 한다. 단 <!DOCTYPE>는 예외이다. 
- html은 글로벌 어트리뷰트를 지원한다. 특히 lang 어트리뷰트를 사용하는 경우가 많은데, 영어를 주언언어로 사용하려면 `en` 을 지정하면 된다.

```
<!DOCTYPE HTML>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>title</title>
  </head>
  <body>
    content
  </body>
</html>
```


## ③ head tag
`head 요소` 는 **메타데이터를 포함하기 위한 요소**이며 html 문서 내에서 단 하나만 존재한다. 메타데이터는 HTML 문서의 title, style, link, script에 대한 데이터로 화면에 표시되지 않는다.

### title tag 
문서의 제목을 정의한다. 제목은 브라우저 탭에 표시된다.
```
<!DOCTYPE html>
<html>
  <head>
    <title>제목</title>
  </head>
  <body>
  </body>
</html>
```
### style tag
HTML 문서를 위한 style 정보를 정의한다.
```
<!DOCTYPE html>
<html>
  <head>
    <title>제목</title>
    <style>
      body {
        background-color: yellow;
        color: blue;
      }
    </style>
  </head>
  <body>
  </body>
</html>
```

### link tag
외부 리소스와의 연계 정보를 정의하며, 주로 HTML과 외부 CSS 파일을 연계에 사용된다
```
<!DOCTYPE html>
<html>
  <head>
    <title>제목</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
  </body>
</html>
```

### script tag
client-side JavaScript를 정의한다.
```
<!DOCTYPE html>
<html>
  <head>
    <script>
      document.addEventListener('click', function () {
        alert('Clicked!');
      });
    </script>
  </head>
  <body>
  </body>
</html>
```


### meta tag
description, keywords, author, 기타 메타데이터 정의에 사용된다. 메타데이터는 브라우저, 검색엔진(keywords) 등에 의해 사용된다.
```
<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">

```
```
<meta name="description" content="Web tutorials on HTML and CSS">
```
```
<meta http-equiv="refresh" content="30">

```


## ④ body tag
문서의 내용을 나타내며 웹페이지에 단 하나만 존재한다.  웹페이지를 구성하는 대부분의 요소가 body 요소 내에 포함된다.


<br/>
<br/>

# 참고📚
[mozilla](https://developer.mozilla.org/ko/docs/Web/HTML)
[poiemaweb](https://poiemaweb.com/html5-semantic-web)
