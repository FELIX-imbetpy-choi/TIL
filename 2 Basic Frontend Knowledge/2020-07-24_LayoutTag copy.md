

# 🎢 개발환경

- editor : visual studio code

- plugin : Live Server

![](https://images.velog.io/images/doomchit_3/post/ac9ce86c-5953-4ba6-b06b-c842278f2a53/image.png)

<br/>
<br/>

# 🥊 Hello World

## main.js

콘솔에 `Hello World!` 를 출력하는 스크립트를 작성한다.

```
console.log('Hello World!');
```


## index.html

페이지를 작성하여 main.js 를 실행시키도록 한다.

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <script src="main.js"></script>
    </head>
<body>

</body>


```

1. 작성된 코드를 실행시키기 위해서 Live Server 플러그인을 이용한다. 에디터에서 마우스 오른쪽만 클릭해도 바로 사용할 수 있다.

2. 연결된 브라우저에서 개발자 툴 (F12) 을 실행하여 console 탭을 확인하면 Hello World 가 찍힌 것을 확인할 수 있다. ( node.js 에서는 js 파일의 실행결과를 바로 확인할 수 있는데 이는 node.js 와 web api 모두 console api 가 사용되고 있기 때문이다. )


![](https://images.velog.io/images/doomchit_3/post/6ad453c8-4938-49c4-8138-ef62ea53f257/image.png)

- Web api 는 Javascript 에 포함된 것이 아니라 브라우저에서 제공하는 함수이다. 이 함수들은 표준 페이지인 MDN 에서 모두 확인 할 수 있다.

- 브라우저의 개발 Tool(개발자도구) 을 활용하면 개발에 많은 도움이 된다. 

<br/>
<br/>

# 🎐 async & defer

`async & defer` 는 HTML 에서 Javascript 파일을 주입할 때 어떤방식으로 주입하는가? 에 대한 설값들이다. 

## ① Head 안에 설정없이 주입

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <script src="main.js"></script>
    </head>
<body>

</body>
```

- 위의 방식을 사용하면 사용자가 HTML 을 불러올 때 HEAD 부분에서 js 파일을 다운로드 받게 되고, HTML 파싱은 멈추게 된다. 

- 결과적으로 HTML 요소들이 느리게 파싱되면서 사용자는 페이지가 느리게 뜨는 경험을 하게 된다.

<br/>

## ② Body 끝에 설정없이 주입

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
<body>
    <div></div>
    <script src="main.js"></script>
</body>


```

- 위의 방식은 브라우저가 HTMl 을 모두 파싱하고, js 파일을 다운로드 하고 실행한다.

- 사용자가 페이지 컨텐츠를 빠르게 접하는 것은 장점이나, 웹사이트가 js 에 의존적이라면 (js 를 통해 데이터를 받거나, Dom 요소 조작) HTML 이 정상적으로 보이더라도 동작 하지 못할 수 있다. 

<br/>

## ③ async 속성 사용
```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <script async src="main.js"></script>
    </head>
<body>
    <div></div>
</body>
```

- 위의 방식은 `async` 속성을 사용하는 것, 브라우저가 HTML 을 파싱하면서 js 를 병렬로 다운로드 받는다.

- js 다운로드가 완료되면, HTML 파싱을 멈추고 js 를 실행한다.

- js 가 html이 파싱되기 전에 실행되면 Dom 요소 조작하는 코드가 먹히지 않을 수 있다. 

- js 를 실행할 때 HTML 파싱이 멈추기 때문에 사용자가 컨텐츠를 보는 시간이 여전히 느려질 가능성이 있다.

- 다수의 스크립트를 다운로드 받게 되면, 먼저 받은 순서부터 실행된다. 정의된 순서에 의존적인 js 라면 문제가 생길 수 있다.

<br/>

## ④ defer 속성 사용
```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <script defer src="main.js"></script>
    </head>
<body>
    <div></div>
</body>

```

- 위의 방식은 `defer` 속성을 사용하는 것, 브라우저가 HTML 을 파싱하면서 js 를 병렬로 다운로드 받는다.

- `async` 방식과는 다르게 js 를 병렬로 다운로드 받고, HTML 파싱이 끝나면 js 가 실행하도록 한다.

- `defer` 는 다수의 js 파일을 받아도 정의된 순서대로 실행되므로 효율적이고 안전하다.

<br/>
<br/>

# 🧨 use strict

- type script 에서는 필요가 없지만 vanilla js 를 이용할 때는 사용하는 것이 좋다.

- js 초창기에 너무 유연하게 만들어져서 위험성이 따랐다. (선언되지 않은 변수에 값 할당 / 프로토타입 변경 )

- Ecma 5 에서 추가된 옵션으로 js 의 유연성을 막아준다.

<br/>
<br/>

# 참고📚

[MDN](https://developer.mozilla.org/ko/)


