---
layout: post
title: "(javascript/js) function"
date: 2024-12-07 14:12:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - function
  - function return
  - 기명함수와 익명함수
  - 호이스팅(hoisting)
  - 인수(Argument)
  - 매개변수(Parameter)
  - 화살표함수(Arrow function)
discription:
---

## 함수(function)

함수(function)란, 어떤 작업을 수행하기 위해 필요한 여러 코드의 집합으로, 코드를 추상화하고 재사용성을 확보한다. 이 함수를 자바스크립트에서는 하나의 데이터 종류로 취급한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="EaYKyGo" data-pen-title="function" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/EaYKyGo">
  function</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 데이터와 호출

### 간단한 예시

```js
// 데이터와 호출
function hi() {
  return "hi~";
}

// 함수 데이터
console.log(hi);
console.log(typeof hi);

// 함수 호출
console.log(hi());
console.log(typeof hi());
```

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ByBKQVV" data-pen-title="js/function-return" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ByBKQVV">
  js/function-return</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 기명함수와 익명함수

### 간단한 예시

```js
// 기명함수와 익명함수

const h1El = document.querySelector(".function h1");

// 기명함수 - function 이름() {}
function handler() {
  console.log(h1El.textContent);
}
h1El.addEventListener("click", handler);

// 익명함수 - function() {}

h1El.addEventListener("click", function () {
  console.log(h1El.textContent);
});
```

<br>

## 호이스팅

`JavaScript` 호이스팅은 인터프리터가 코드를 실행하기 전에 함수, 변수, 클래스 또는 임포트(`import`)의 선언문을 해당 범위의 맨 위로 끌어올리는 것처럼 보이는 현상을 뜻한다.

### 간단한 예시

```js
// 호이스팅 (Hoisting) : 끌어올려지는 것
hello(); // Ok !
// world() // Error..

// 선언문과 표현식의 차이는 호이스팅 가능 여부이다.
// 함수 선언문(Declaration) 자바스크립트는 기본적으로 위에서 아래로 해석이 되는데
// 함수 선언방식으로 선언했을 때에는 스크립트가 자동으로 끌어올려지는 현상을 가지고 있다.(호이스팅 발생)
function hello() {
  console.log("hello~");
}

// 함수 표현식(expression) 익명의 함수를 변수에 할당하는 것. (호이스팅 현상이 발생하지 않음)
const world = function () {
  console.log("world!");
};

world(); // Ok !

console.log("==========");

// 추상화(abstraction) : 변수나 함수명을 통해 의미를 이해할 수 있는

const fruits = getFruits();
const movies = getMovies();

function getFruits() {
  // 코드n
  // 코드n
  // 코드n
  // 코드n
  // ...
  // return fruits
}

const getMovies = function () {
  // 코드n
  // 코드n
  // 코드n
  // 코드n
  // ...
  // return movies
};
```

## 인수(Argument)와 매개변수(Parameter)

매개변수와 인수의 차이점은 쓰임의 차이에 있다. 함수를 정의할 때 사용되는 변수를 매개변수, 실제로 함수가 호출될 때 넘기는 변수값을 인수라고 한다.

### 간단한 예시

```js
// 인수(Argument)와 매개변수(Parameter)

function add(a, b) {
  return a + b;
}

console.log(add(2, 1));
console.log(add("A", "B"));

console.log("==============");

// 매개변수 기본값(Default Value)
function add(a, b = 1) {
  if (a === undefined) {
    console.log("첫 번째 인수는 필수입니다!");
    return;
  }
  return a + b;
}
console.log(add(2));
console.log(add(2, undefined));
console.log(add(7, 5));

console.log("==============");

// 나머지 매개변수(Reset Parameter)
function add(a, b, ...rest) {
  console.log(a, b, rest);
  return rest.reduce((acc, cur) => acc + cur, 0);
}
const res = add(1, 2, 3, 4, 5, 6, 7, 8);
// 3부터 8까지 ...전개연산자를 통해 배열로 만드는데 이 것을 나머지 매개변수(Rest Parameter)라고한다.
console.log(res);
```

<br>

## 화살표함수(Arrow function)

화살표 함수 표현식(화살표 함수 `expression`)은 함수 표현식에 대한 간결한 대안으로, 약간의 의미적 차이와 의도적인 사용상의 제한을 가지고 있다.

### 간단한 예시

```js
/// 일반 함수
function hello1() {
  return "Hello~";
}
const add1 = function (a, b) {
  return a + b;
};
const log1 = function (c) {
  console.log(c);
};

/// 화살표 함수
const hello2 = () => "Hello~";

const add2 = (a, b) => a + b;

const log2 = (c) => {
  console.log(c);
};

/// 화살표함수의 소괄호(매개변수를 감싸고있는) 생략
const a = () => {}; // 매개변수가 없으면 생략 불가능
const b = (x) => {}; // 매개변수가 하나일 때 생략 가능 !!
const b2 = (x = 1) => {}; // 매개변수의 기본 값을 할당할 때에는 불가능
const c = (x, y) => {}; // 매개변수가 두 개 이상 일때는 생략 불가능

/// 화살표함수의 중괄호 생략

const a2 = (x) => {
  return x * x; // 생략 가능
};

const a22 = (x) => x * x;

// return 키워드로 코드가 시작해야 중괄호 생략이 가능

const c2 = (x) => {
  console.log(x * x); // return 키워드로 코드가 시작하지 않음
  return x * x;
};

// return 배열 반환

const d = () => {
  return [1, 2, 3]; // 생략 가능
};

const d2 = () => [1, 2, 3];

// 중괄호를 사용하는 객체데이터를 반환하려면 자바스크립트가 오해하지 않도록
// 소괄호로 감싸서 생략해 아래와 같이 사용이 가능하다.

const g = () => {
  return { a: 1 };
};

const g2 = () => ({ a: 1 });

/// 객체 데이터의 메소드 축약

const obj = {
  fnA() {}, // 일반함수를 할당하는 함수 fnB의 축약형
  fnB: function () {}, // 일반 함수
  fnC: () => {}, // 화살표 함수
};
```

<br>

## 즉시 실행 함수 표현(IIFE)

즉시 실행 함수 표현(`IIFE`, Immediately Invoked Function Expression) 은 정의되자마자 즉시 실행되는 `Javascript Function` 를 말한다. `IIFE`라는 이름은 Ben Alman이 블로그에서 처음으로 시작되었다.

### 간단한 예시

```js
// ;(함수)()
(function () {
  console.log("123");
})();

// 즉시실행함수의 다양한 사용법
(() => {})();
(function () {})();
(function () {})();
!(function () {})();
+(function () {})();
```

<br>

**따라하기(function schedule)**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="wBwGoEx" data-pen-title="js/function-schedule" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/wBwGoEx">
  js/function-schedule</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
