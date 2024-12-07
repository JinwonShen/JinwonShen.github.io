---
layout: post
title: "(javascript/js) ternary operator"
date: 2024-12-07 16:51:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - operator
  - ternary operator
discription:
---

## 삼항 연산자(ternary operator)

조건 (삼항) 연산자는 `JavaScript`에서 세 개의 피연산자를 받는 유일한 연산자아다. 앞에서부터 조건문, 물음표(`?`), 조건문이 참(`truthy`)일 경우 실행할 표현식, 콜론(`:`), 조건문이 거짓(`falsy`)일 경우 실행할 표현식이 배치된다. 해당 연산자는 `if...else`문의 대체재로 빈번히 사용된다.

<br>

```js
const fruits = ["apple", "banana", "cherry"];

// if 조건문
// fruits.length > 0 =
if (fruits.length) {
  console.log("과일이 있습니다.");
} else {
  console.log("과일이 없습니다.");
}

// 삼항 연산자
const message = fruits.length ? "과일이 있습니다." : "과일이 없습니다.";
console.log(message);

// 함수를 활용한
function includesText(el) {
  return el.textContent ? "글자 있음" : "글자 없습";
}

const h1El = document.querySelector("h1");
console.log(includesText(h1El));
```
