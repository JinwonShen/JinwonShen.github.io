---
layout: post
title: "(javascript/js) arithmetic operator"
date: 2024-12-07 15:38:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - arithmetic operators
  - assignment operators
discription:
---

# 연산자(operators)

## arithmetic operators(산술연산자)

산술 연산자는 사칙연산을 다루는 기본적이면서도 가장 많이 사용되는 연산자이다.

산술 연산자는 모두 두 개의 피연산자를 가지는 이항 연산자이며, 피연산자들의 결합 방향은 왼쪽에서 오른쪽이다.

<br>

## assignment operators(할당연산자)

할당(`=`) 연산자는 변수에 값을 대입하는 데 사용된다. 할당 연산은 할당된 값으로 평가된다. 할당 연산자를 연결하여 사용하면 단일 값을 여러 변수에 할당할 수 있다.

<br>

```js
// 산술 연산자(arithmetic operators)

console.log(1 + 2);
console.log(5 - 7);
console.log(3 * 4);
console.log(10 / 2);
console.log(7 % 5);

console.log("=========");

// 할당 연산자(assignment operators)

let a = 3;
console.log(a);

// a = a + 2 (더하기 할당 연산자)

a += 2;
console.log(a);

// a = a - 2 (빼기 할당 연산자)
a -= 2;
console.log(a);

// a = a * 2 (곱하기 할당 연산자)

a *= 2;
console.log(a);

// a = a / 2 (나누기 할당 연산자)

a /= 2;
console.log(a);

// a = a % 2 (나머지 할당 연산자)

a %= 2;
console.log(a);

console.log("=========");

// 증감 연산자(Increment & Decrement operators)는 변수 1씩 더하거나 빼는 연산자

// ++ 기호가 뒤에 있는 경우,

let a2 = 3;
console.log(a2++);
console.log(a2);

// ++ 기호가 앞에 있는 경우,

let b = 3;
console.log(++b);
console.log(b);

// -- 기호가 뒤에 있는 경우,

let c = 3;
console.log(c--);
console.log(c);

// -- 기호가 앞에 있는 경우,

let d = 3;
console.log(--d);
console.log(d);

console.log("=======");

// 증감 연산자보다 할당 연산자를 사용하는 것을 추천한다.
let e = 3;
e += 1;
console.log(e);

e -= 1;
console.log(e);
```
