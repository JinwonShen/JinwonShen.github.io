---
layout: post
title: "(javascript/js) nagation operators"
date: 2024-12-07 16:51:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - operators
  - negation operators
  - comparison operators
discription:
---

## 부정연산자(negation operators)란,

부정연산자(negation operators)란 참과 거짓의 반댓값을 불린 데이터로 반환한다.

<br>

## 비교연산자(comparison operators)란,

비교 연산자(comparison operators)는 논리 문장에서 변수나 값의 동등성이나 차이를 판별하는 데 사용된다.

<br>

```js
console.log(!true); // false
console.log(!false); // true

console.log("중첩사용 =========");
console.log(!0); // true
console.log(!!0); // false
console.log(!!!0); // true
console.log(!!!!0); // false

console.log("거짓(falsy) ========");
console.log(!null); // true
console.log(!NaN); // true
console.log(!undefined); // true
console.log(!""); // true

console.log("참(truthy) ========");
console.log(!{}); // false
console.log(![]); // false
console.log(!"A"); // false

console.log("===================");

// 비교연산자(comparison operators)는 두 데이터를 비교할 때 사용된다.
const a = 1;
const b = 3;

// 동등(형 변환!) 피 연산자 끼리의 비교
console.log(a == b); // false

// 부등(형 변환!)
console.log(a != b); // true

// 일치
console.log(a === b); // false

// 불일치
console.log(a !== b); // true

// 큼
console.log(a > b); // false

// 크거나 같음
console.log(a >= b); // false

// 작음
console.log(a < b); // true

// 작거나 같음
console.log(a <= b); // true
```
