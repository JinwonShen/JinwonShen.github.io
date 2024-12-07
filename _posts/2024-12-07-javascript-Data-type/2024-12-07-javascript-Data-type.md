---
layout: post
title: "(javascript/js) Data type"
date: 2024-12-07 15:38:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - data type
  - string
  - number
  - boolean
  - object
  - undefined
  - function
discription:
---

## typeof

`typeof` 연산자는 피연산자의 평가 전 자료형을 나타내는 문자열을 반환한다.

### 구문

```js
const data = {
  string: "123",
  number: 123,
  boolean: true,
  null: null,
  undefined: undefined,
  array: [1, 2, 3],
  object: { a: 1, b: 2 },
  function: function () {},
};

console.log("typeof data");
console.log(typeof data.string === "string");
console.log(typeof data.number === "number");
console.log(typeof data.boolean === "boolean");
console.log(typeof data.null === "object");
console.log(typeof data.undefined === "undefined");
console.log(typeof data.array === "object");
console.log(typeof data.object === "object");
// null, array, object 이 세 가지를 구분하기에는 무리가 있다.
console.log(typeof data.function === "function"); // 메소드

console.log("data.constructor");
console.log(data.string.constructor === String);
console.log(data.number.constructor === Number);
console.log(data.boolean.constructor === Boolean);
// console.log(data.null.constructor)
// console.log(data.undefined.constructor)
// null은 typeof와 constructor 모두 구분하기 어렵다. undefined는 typeof로 구분할 수 있다.
console.log(data.array.constructor === Array);
console.log(data.object.constructor === Object);
console.log(data.function.constructor === Function);
```
