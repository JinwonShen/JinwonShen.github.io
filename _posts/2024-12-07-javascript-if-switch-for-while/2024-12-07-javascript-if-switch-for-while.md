---
layout: post
title: "(javascript/js) operator 연산자"
date: 2024-12-07 16:51:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - operator
  - arithmetic operator
  - logical operator
  - ternary operator
  - spread operator
discription:
---

## if...else

`if` 문은 지정한 조건이 참인 경우 명령문(`statement`)을 실행한다. 조건이 거짓인 경우 또 다른 명령문이 실행 될 수 있다.

### 구문

```js
// if 조건문

if (조건) {
  // 참일 때 실행
}

if (조건) {
  // 참일 때 실행
} else {
  // 거짓일 때 실행
}

if (조건1) {
  // 참일 때 실행 참이 아닐 때 조건 2로 이동
} else if (조건2) {
  // 참일 때 실행 참이 아닐 때 조건 3로 이동
} else if (조건3) {
  // 참일 때 실행 참이 아니라면 마지막으로 이동
} else {
  // 거짓일 때 실행
}

// 아래 예시

const age = 20;

if (age >= 18) {
  console.log("성인");
}

const number = 7;

if (number % 2 === 0) {
  console.log("짝수");
} else {
  console.log("홀수");
}
```

<br>

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="qEWZqpZ" data-pen-title="js/if...else" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/qEWZqpZ">
  js/if...else</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## switch

`switch` 문은 표현식을 평가하고 표현식의 값을 일련의 `case` 절과 비교하고 일치하는 값이 있는 첫 번째 `case` 절 이후의 문장을 `break` 문이 나올 때까지 실행한다. 표현식의 값과 일치하는 `case가` 없으면 `switch` 문의 `default` 절로 점프한다.

### 구문

```js
switch (조건) {
  case 값1:
    // ...
    break;
  case 값2:
    // ...
    break;
  case 값2:
    // ...
    break;
  default:
  // ...
}

// 아래 예시

const prodItem = "마우스";

switch (prodItem) {
  case "노트북":
    console.log((3000000).toLocaleString() + "원");
    break;
  case "휴대폰":
    console.log((800000).toLocaleString() + "원");
    break;
  case "키보드":
  case "마우스":
    console.log((120000).toLocaleString() + "원");
    break;
  default:
    console.log("-");
}
```

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="QwLNGQJ" data-pen-title="js/switch" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/QwLNGQJ">
  js/switch</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## for

`for` 문은 괄호로 감싸고 세미콜론으로 구분한 세 개의 선택식과, 반복을 수행할 문(주로 블럭문)으로 이루어져 있다.

### 구문

```js
// for 문
// for (초기화; 조건; 증감) {}
for (let i = 0; i < 10; i += 1) {
  if (i % 2 !== 0) {
    continue; // 현재 반복문은 정지하고 다음으로 넘어간다.
    // break 반복이 정지된다.
  }
  console.log(i);
}
```

<br>

## for-of

`for...of` 명령문은 반복가능한 객체 (`Array`, `Map`, `Set`, `String`, `TypedArray`, `arguments` 객체 등을 포함)에 대해서 반복하고 각 개별 속성값에 대해 실행되는 문이 있는 사용자 정의 반복 후크를 호출하는 루프를 생성한다.

### 구문

```js
// for of 구문
// for (const 아이템 변수 of 배열) {}
const fruits = ["apple", "banana", "cherry", "durian"];

for (let i = 0; i < fruits.length; i += 1) {
  const fruit = fruits[i];
  console.log(fruit);
}

for (const fruit of fruits) {
  if (fruit === "cherry") {
    continue;
  }
  console.log(fruit);
  const divEl = document.createElement("div");
  divEl.textContent = fruit;
  divEl.classList.add("fruit");
  document.querySelector(".for").appendChild(divEl);
}

// for in 구문
// for (const 키변수 in 객체) {}
const user = {
  name: "jinwon",
  age: 85,
  isValid: true,
  email: "bosv031999@gmail.com",
};

for (const key in user) {
  if (key === "age") {
    continue;
  }
  console.log(key, user[key]);
  const pEl = document.createElement("p");
  pEl.innerHTML = `<b>${key}</b> : ${user[key]}`;
  document.querySelector(".for").appendChild(pEl);
}
```
