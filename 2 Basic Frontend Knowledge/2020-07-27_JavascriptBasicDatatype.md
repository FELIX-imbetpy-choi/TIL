
![](https://images.velog.io/images/doomchit_3/post/f02d94d4-a6e5-440b-9808-be64098a4679/image.png)

<br/>
<br/>

# 🎱 기본문법

### ① 변수
- 변수는 값을 저장하고 참조하기 위해 사용한다.

- let 은 ES6 에서 추가된 변수 선언자 이다.

- let 을 사용하면 Mutable type 변수로 지정된다. (변수의 값이 변경 가능하다)

- var 는 이제 사용하지 않는 변수지정자이다. ( var hosting-변수를 선언하기 전에도 값을 할당가능 / 블록스코프를 무시하는 특징 문제로 )

- Constant 는 값을 변경할 수 없는 변수를 지정합니다. (보안, 쓰레드가 변수에 동시접근 방지)

- 메모리에 변수가 저장되는 방식은 두가지가 있다. (primitive, object)

- `primitive 타입` 은 값자체가 메모리에 저장된다. 

- `object 타입` 은 메모리에 레퍼런스가 담겨있고, 객체 안에 있는 값은 변경이 가능하다.

```javascript
let x; // 변수의 선언
x = 6; // 정수값의 할당

let globalName = 'global name'
{
let name = 'junyeong';
console.log(name); // junyeong

name = 'hello';
console.log(name); // hello
console.log(globalName); // 전역변수는 블록 안에서도 기능함 - 메모리에 항상 탑재
}

console.log(name); // block 안에 정의된 값을 사용할 수 없음
console.log(globalName); // 전역변수는 사용가능

{
console.log(age); // undefined
age = 4;
console.log(age); // 4, var hosting
var age;
}
console.log(age); // 4 ,스코프를 무시한다.

const daysInWeek = 7;
const maxNumber = 5;
```
### ② 값
- 프로그램에 의해 변수에 할당되는 대상을 말한다.

- 자바스크립트의 모든 값은 데이터 타입을 갖는다. 

- 자바스크립트는 7가지 데이터 타입을 제공한다.( number / string / boolean / null / undefined / symbol (New in ECMAScript 6) / 객체 타입 (Object data type) / object )

- 자바스크립트는 C나 Java외는 다르게 변수를 선언할 때 데이터 타입을 미리 지정하지 않는다. 변수에 할당된 값의 타입에 의해 동적으로 변수의 타입이 결정된다. 

```javascript
// 숫자 리터럴
10.50
1001

// 문자열 리터럴
'Hello'
"World"

// 불리언 리터럴
true
false

// null 리터럴
null

// undefined 리터럴
undefined

// 객체 리터럴
{ name: 'Lee', gender: 'male' }

// 배열 리터럴
[ 1, 2, 3 ]

// 정규표현식 리터럴
/ab+c/

// 함수 리터럴
function() {}
```

### ③ 연산자

- 연산자(Operator)는 하나 이상의 표현식을 대상으로 산술, 할당, 비교, 논리, 타입 연산 등을 수행해 하나의 값을 만든다. 

- 피연산자의 타입은 반드시 일치할 필요는 없다. 이때 자바스크립트는 암묵적 타입 강제 변환을 통해 연산을 수행한다.

```javascript
// 산술 연산자
let area = 5 * 4; // 20

// 문자열 연결 연산자
let str = 'My name is ' + 'Lee'; // "My name is Lee"

// 할당 연산자
let color = 'red'; // "red"

// 비교 연산자
let foo = 3 > 5; // false

// 논리 연산자
let bar = (5 > 3) && (2 < 4);  // true

// 타입 연산자
let type = typeof 'Hi'; // "string"

// 인스턴스 생성 연산자
let today = new Date(); // Sat Dec 01 2018 00:57:19 GMT+0900 (한국 표준시)

// 암묵적 형변환
let foo = 1 + '10'; // '110'
let bar = 1 * '10'; // 10
```

### ③ 키워드

- 키워드(keyword)는 수행할 동작을 규정한 것이다. 예를 들어 var 키워드는 새로운 변수를 생성할 것을 지시한다.

```javascript
// 변수의 선언
let x = 5 + 6;

// 함수의 선언
function foo (arg) {
  // 함수 종료 및 값의 반환
  return ++arg;
}
```

### ④ 주석

- 주석(Comment)은 작성된 코드의 의미를 설명하기 위해 사용한다.

-한줄 주석은 // 다음에 작성하며 여러 줄 주석은 /*과 */의 사이에 작성한다. 주석은 해석기(parser)가 무시하며 실행되지 않는다.

### ⑤ 문

- 문은 리터럴, 연산자(Operator), 표현식(Expression), 키워드(Keyword) 등으로 구성되며 세미콜론( ; )으로 끝나야 한다.

-다른 언어와 달리 자바스크립트에서는 블록 유효범위(Block-level scope)를 생성하지 않는다. 함수 단위의 유효범위(Function-level scope)만이 생성된다.

### ⑥ 표현식

- 표현식(Expression)은 하나의 값으로 평가(Evaluation)된다. 

- 연산자의 조합은 모두 표현식이며 하나의 값으로 평가(Evaluation)된다.

```javascript
// 표현식
5             // 5
5 * 10        // 50
5 * 10 > 10   // true
(5 * 10 > 10) && (5 * 10 < 100)  // true
```

### ⑦ 문과 표현식의 비교

-  표현식은 평가되어 값을 만들지만 그 이상의 행위는 할 수 없다. 

- 문은 var, function과 같은 선언 키워드를 사용하여 변수나 함수를 생성하기도 하고 if, for, while 문과 같은 제어문을 생성하여 프로그램의 흐름을 제어하기도 한다. 

- 표현식을 통해 평가한 값을 통해 실제로 컴퓨터에게 명령을 하여 무언가를 하는 것은 문이다.

### ⑧ 함수

- 함수란 어떤 작업을 수행하기 위해 필요한 문(statement)들의 집합을 정의한 코드 블록이다. 

- 미리 정의된 함수를 재사용하는 것이 효율적이다. 

```javascript
// 함수의 정의(함수 선언문)
function square(number) {
  return number * number;
}
```

### ⑨ 객체

- 원시 타입(Primitives)을 제외한 나머지 값들(함수, 배열, 정규표현식 등)은 모두 객체이다.

- 자바스크립트 객체는 키(이름)와 값으로 구성된 프로퍼티(property)의 집합이다. 

- 자바스크립트의 함수는 일급 객체이므로 값으로 취급할 수 있다. 따라서 프로퍼티 값으로 함수를 사용할 수도 있으며 프로퍼티 값이 함수일 경우, 일반 함수와 구분하기 위해 메소드라 부른다.

```javascript
let person = {
  name: 'Lee',
  gender: 'male',
  sayHello: function () {
    console.log('Hi! My name is ' + this.name);
  }
};

console.log(typeof person); // object
console.log(person); // { name: 'Lee', gender: 'male', sayHello: [Function: sayHello] }

person.sayHello(); // Hi! My name is Lee
```


### ⑩ 배열

- 배열(array)은 1개의 변수에 여러 개의 값을 순차적으로 저장할 때 사용한다.

```javascript
var arr = [1, 2, 3, 4, 5];

console.log(arr[1]); // 2
```

<br/>
<br/>

# 🧬 데이터 타입

- 데이터 타입(Data Type)은 프로그래밍 언어에서 사용할 수 있는 데이터(숫자, 문자열, 불리언 등)의 종류를 말한다.

- 자바스크립트의 모든 값은 데이터 타입을 갖는다. ECMAScript 표준(ECMAScript 2015 (6th Edition), 이하 ES6)은 7개의 데이터 타입을 제공한다

- 데이터 타입에는 Immutable data 와 Mutable data 가 존재한다.

- Immutable data 타입 : premitive (데이터 자체를 변경하는 것이 불가능), frozen objectx (변경이 불가하다)

- Mutable data 타입 : object (object 안에 레퍼런스는 변경이 가능하다.)

- js 에서 기본적으로 모든 object 는 변경이 가능하다.

- primitive 종류 :  single item : number, string, boolean, null, undefined, symbol

- object 종류 : box container 

- function : first-class function (함수도 변수에 할당 가능)

### ① number

```javascript
const count = 17; // 정수
const size = 17.2 // 실수
console.log(`value:${count}, type: ${typeof count}`); // number
console.log(`value:${size}, type: ${typeof size}`); // number


const infinity = 1 / 0; 
const negativeInfinity = -1 / 0;  
const nAn = 'not a number' / 2; 
console.log(infinity); // infinity
console.log(negativeInfinity); // -infinity
console.log(nAn); // NaN

const bigInt = 123456498465319849684654987546498484n; // n을 붙여주면 bigint 로 인식한다.
console.log(`value:${bigInt}, type: ${typeof bigInt}`); // bigInt
Number.MAX_SAFE_INTEGER;
```

-  Dom 을 조작할 때 infinity, negativeInfinity, nAn 으로 에러날 가능성이 있다.

- bigInt (크롬, firefox 만 현재는 지원) 는 아직까지 쓰지 않는 추세이다.


### ② string

```javascript
const char = 'c';
const brendan = 'brendan';
const greeting = 'hello' + brendan;

console.log(`value:${greeting}, type: ${typeof greeting}`);  //string
const helloBob = `hi ${brendan}!`; 
console.log(`value:${helloBob}, type: ${typeof helloBob}`);  //string
```

### ③ boolean

- false : 0, null, nudefined, NaN, ''

- true : any other value


```javascript
const canRead = true;
const test = 3 < 1; //false
console.log(`value:${test}, type: ${typeof test}`);
```


### ④ null

-  개발자가 직접 빈 값을 지정할 때 사용한다.

```javascript
let nothing = null;
console.log(`value:${nothing}, type: ${typeof nothing}`);

```

### ⑤ undefined
- 아무런 값이 설정되지 않으면 자동으로 설정된다.

```javascript
let x;
console.log(`value:${x}, type: ${typeof x}`);
```



### ⑥ symbol

-  고유한 식별자를 만들거나, 우선순위를 줄 때 이용한다.

- 스트링이 같아도 다른 식별자로 인식한다.

```javascript
const symbol1 = Symbol('id');
const symbol2 = Symbol('id');
console.log(symbol1==symbol2); //false

// 스트링이 같을 때 같은 심볼로 인식하게 하려면
const symbol3 = Symbol.for('id');
const symbol4 = Symbol.for('id');
console.log(symbol3==symbol4); //true

// 심볼은 바로 출력하면 에러가 난다. description 을 이용해야 
console.log(`value:${symbol3.description}, type: ${typeof symbol3}`);

```


### ⑦ Dynamic typing 
- javascript 는 dynamically typed language 이다.

- c, java 는 변수 타입을 함께 선언해야 하지만, js 는 할당된 값에 따라서 변수 타입이 달라질 수 있다.

- 변수명을 보고 타입을 예상한다면 런타임오류가 날 가능성이 있다. ( 변수의 타입이 수시로 바뀔 수 있음 )

- 이런 특징으로 등장한 것이 Type script 이다.

```javascript
let text = 'hello';
console.log(text.charAt(0)); // h
console.log(`value:${text}, type: ${text}`); // string
 text = 2;
console.log(`value:${text}, type: ${text}`); // number
 text = '7' + 2;
console.log(`value:${text}, type: ${text}`); // 75, string
 text = '8' / '2';
console.log(`value:${text}, type: ${text}`); // 4, number

console.log(text.charAt(0)); // Error
```

<br/>
<br/>

# 참고📚

[MDN](https://developer.mozilla.org/ko/)

[poiemaweb](https://poiemaweb.com/js-prototype)
