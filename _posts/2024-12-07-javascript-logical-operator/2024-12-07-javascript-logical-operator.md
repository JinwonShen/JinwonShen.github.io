---
layout: post
title: "(javascript/js) logical operators"
date: 2024-12-07 16:51:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - operators
  - logical operators
discription:
---

## 논리연산자(logical operators)란,

연산자에 '논리’라는 수식어가 붙긴 하지만 논리 연산자는 피연산자로 불린형뿐만 아니라 모든 타입의 값을 받을 수 있다. 연산 결과 역시 모든 타입이 될 수 있다.

<br>

```js
/// 그리고(AND) 연산자 &&
const a = true;
const b = false;

if (a && b) {
  console.log("참!"); // 출력x
}
console.log(a && b); // false

console.log("============");

/// 또는(OR) 연산자 ||

const c = true;
const d = false;

if (c || d) {
  console.log("참!"); // 출력됨
}
console.log(c || d); // true

console.log("============");

//// 그리고(AND) 연산자는 왼쪽에서부터 가장 먼저 만나는 거짓(Falsy) 데이터를 반환한다.
//// 끝까지 거짓이 없으면 가장 오른쪽의 마지막 참(Truthy) 데이터를 반환한다.
console.log(true && false); // false
console.log(1 && 0); // false
console.log(1 && 7 && 0); // 0
console.log(7 && 0 && 7); // 0
console.log(0 && 1 && 7); // 0
console.log("x" && {} && null); // null
console.log({} && "y" && []); // []

//// 또는(OR) 연산자는 왼쪽에서부터 가장 먼저 만나는 참(Truthy) 데이터를 반환한다.
//// 끝까지 참이 없으면 가장 오른쪽의 마지막 거짓(Falsy) 데이터를 반환한다.
console.log(false || true); // true
console.log(0 || 1); // 1
console.log(false || 0 || {}); // {}
console.log(false || "ab" || null); // ab
console.log(function () {} || undefined || ""); // f () {}
console.log("" || 0 || NaN || false); // false
```
