![](https://images.velog.io/images/doomchit_3/post/509ca899-4c2f-40f4-996b-311628106415/image.png)

# 🧨 HyperText
`HyperText` 의 Hyper 는 텍스트 정보가 다중으로 연결되어 있는 상태를 의미한다.

- HTML 의 특징인 link 개념과 연결되는데 문서의 선형성, 고정성에서 벗어나 사용자가 원하는 순서대로 원하는 정보를 취득할 수 있도록 한다.
- 한 텍스트에서 다른 텍스트로 건너뛰어 읽을 수 있는 기능을 하이퍼링크(hyper link)라 한다.

## ① a

HTML link는 hyperlink를 의미하며 a tag가 그 역할을 담당한다.
```
    <a href="http://www.google.com">Visit google.com!</a>

```

<br/>
<br/>

# 🎁 href 어트리뷰트
- href 어트리뷰트는 이동하고자 하는 파일의 위치(경로)를 값으로 받는다.
- 경로(path)란 파일 시스템 상에서 특정 파일의 위치를 의미한다.

## ① 디렉토리(Directory)
`디렉토리` 는 파일과 다른 디렉터리를 갖는 파일 시스템 내의 존재물로서 `폴더` 라고도 불리운다.
- 루트 디렉터리
파일 시스템 계층 구조 상의 최상위 디렉터리이다.
**Unix** : `/`
**Windows** : `C:\`
- 홈 디렉터리
시스템의 사용자에게 각각 할당된 개별 디렉터리이다.
**Unix** : `/Users/{계정명}`
**Windows** : `C:\Users\{계정명}`
- 작업 디렉터리
작업 중인 파일의 위치한 디렉터리이다.
**공통** : `./`
- 부모 디렉터리
작업 디렉터리의 부모 디렉토리이다.
**공통** : `../`

<br/>

## ② 파일 경로(File path)
파일 경로는 파일 시스템에서 파일의 위치를 나타내는 방법이다. 경로에는 절대경로와 상대경로가 있다.
- 절대경로(Absolute path)
현재 작업 디렉터리와 관계없이 특정 파일의 절대적인 위치를 가리킨다. 루트 디렉터리를 기준으로 파일의 위치를 나타낸다.
`http://www.HELLO.com/index.html`
`/Users/HELLO/Desktop/myImage.jpg`
`C:\users\HELLO\Desktop\myImage.jpg`
`/index.html`
- 상대경로(Relative path)
현재 작업 디렉터리를 기준으로 특정 파일의 상대적인 위치를 가리킨다.
`./index.html`
`../dist/index.js`
`../../dist/index.js`

<br/>

## ③ href 어트리뷰트에 사용 가능한 값
- 절대 URL 
웹사이트 URL (href=”http://www.example.com/default.html”)

- 상대 URL 
자신의 위치를 기준으로한 대상의 URL (href=”html/default.html”)

- fragment identifier 
페이지 내의 특정 id를 갖는 요소에의 링크 (href=”#top”)

- 메일 
mailto:

- script 
href=”javascript:alert(‘Hello’);”

```
    <a href="http://www.google.com">URL</a><br>
    <a href="html/my.html">Local file</a><br>
    <a href="file/my.pdf" download>Download file</a><br>
    <a href="#">fragment identifier</a><br>
    <a href="mailto:someone@example.com?Subject=Hello again">Send Mail</a><br>
    <a href="javascript:alert('Hello');">Javascript</a>
```

<br/>
<br/>

# 🧶 target 어트리뷰트

`target 어트리뷰트` 는 링크를 클릭했을 때 윈도우를 어떻게 오픈할 지를 지정한다.

- `_self` : 링크를 클릭했을 때 연결문서를 현재 윈도우에서 오픈한다 (기본값)
	
- `_blank` : 링크를 클릭했을 때 연결문서를 새로운 윈도우나 탭에서 오픈한다

```
    <a href="http://www.google.com" target="_blank">Visit google.com!</a>

```

<br/>
<br/>

# 참고📚
[mozilla](https://developer.mozilla.org/ko/docs/Web/HTML)
[poiemaweb](https://poiemaweb.com/html5-semantic-web)