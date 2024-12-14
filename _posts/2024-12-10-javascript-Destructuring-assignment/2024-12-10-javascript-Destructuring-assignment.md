---
layout: post
title: "(javascript/js) 구조 분해 할당(Destructuring assignment)"
date: 2024-12-10 16:18:00 +09:00
lastmode: 2024-12-10 16:18:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Destructuring assignment
discription:
---

## 구조 분해 할당(Destructuring assignment)

`배열(배열 구조 분해 할당)`이나 `객체(객체 구조 분해 할당)`의 구조에 맞게 개별 변수에 값을 할당하는 방법으로, 필요한 값만 추출하여 변수에 할당할 수 있다.

### 배열 데이터에서 구조 분해 할당 : 구문

```js
const numbers = [1, 2, 3];

// const a = numbers[0]
// const b = numbers[1]
// const c = numbers[2]
const [a, b, c] = numbers;

console.log(a, b, c); // 1 2 3
```

<br>

### 배열 데이터에서 구조 분해 할당 : 선언과 분리

```js
const numbers = [1, 2, 3];
let a; // let 이라는 변수를 if 밖에서 선언한 것은
let b; // if 내부에서 선언했을 때
let c; // 유효범위(Scope) 밖에 있기 때문이다.
if (numbers.length) {
  [a, b, c] = numbers; // let [a, b, c] = numbers; // not defined
}
console.log(a, b, c); // 1 2 3
```

<br>

### 배열 데이터에서 구조 분해 할당 : 기본값 지정

```js
const numbers = [7, , 3]
const [a = 0, b, c] = numbers
// a = 0 기본값 할당
console.log(a, b, c) 7 undefined 3
```

<br>

### 배열 데이터에서 구조 분해 할당 : 반환 값 무시

```js
const numbers = [1, 2, 3];
const [, , c] = numbers;
// 할당될 수 있는 변수가 없어 순서가 일치하는 곳에 할당된다.
console.log(c); // 3
```

<br>

### 배열 데이터에서 구조 분해 할당 : 나머지 할당

```js
const numbers = [1, 2, 3];
const [a, ...rest] = numbers;
// a 변수 부분은 순서에 맞게 1이 할당이 될 것이고,
// ...전개연산자와 변수를 통해 나머지를 모두 받아 할당된다.
console.log(a, rest); // 1 [2, 3]
```

<br>

### 객체 데이터에서 구조 분해 할당 : 구문

```js
const user = {
  name: "Neo",
  age: 22,
  isValid: true,
};
// const name = user.name
// const age = user.age
// const isValid = user.isValid
const { name, age, isValid } = user;
// 객체의 순서는 상관이 없다.

console.log(name);
console.log(age);
console.log(isValid);
```

<br>

### 객체 데이터에서 구조 분해 할당 : 선언과 분리

```js
const user = {
  name: "Neo",
  age: 22,
  isValid: true,
};

let name;
let age;
let isValid;

if (user) {
  ({ name, age, isValid } = user);
  // 내부에서 구조 분해 할당을 할 때 소괄호로 감싸고 있어야 한다.
}

console.log(name, age, isValid);
```

<br>

### 객체 데이터에서 구조 분해 할당 : 기본값 지정

```js
const user = {
  name: "Neo",
  age: 22,
};

const { isValid = false } = user;
// 기본값은 "=" 할당연산자를 사용해 지정

console.log(isValid); // false
```

<br>

### 객체 데이터에서 구조 분해 할당 : 변수명 변경

```js
const user = {
  name: "Neo",
  age: 22,
  isValid: true,
};

const { name: n, age: a, isValid: v } = user;
// ex) name 이 가지고 있는 데이터는 n 이라는 변수에 할당

console.log(n, a, v); // Neo 22 true
console.log(name, age, isValid); // error
```

<br>

### 객체 데이터에서 구조 분해 할당 : 기본값 + 변수명 변경

```js
const user = {
  name: "Neo",
  age: 22,
};

const { name: n, age: a, isValid: v = false } = user;
// ex) name 이 가지고 있는 데이터는 n 이라는 변수에 할당
// isValid: v = false 라는 기본값을 할당
// isValid가 없어 기본값 false를 반환

console.log(n, a, v); // Neo 22 false
console.log(name, age, isValid); // error
```

<br>

### 객체 데이터에서 구조 분해 할당 : 나머지 할당

```js
const user = {
  name: "Neo",
  age: 22,
  isValid: true,
};

const { age, ...rest } = user;

console.log(age, rest); // 22 { name: Neo, isValid: true }
```

<br>
