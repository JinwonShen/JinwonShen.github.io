---
layout: post
title: "(javascript/js) this 키워드"
date: 2024-12-13 10:44:00 +09:00
lastmode: 2024-12-13 10:44:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - this
discription:
---

## this

`this` 키워드는 일반 함수와 화살표 함수에 따라 다르게 정의된다. 일반 함수는 호출 위치에서 this가 정의되며, 화살표 함수는 선언 위치(렉시컬 스코프)에서 `this`가 정의된다.

<br>

**간단한 예시(일반함수)**

```js
function User() {
  this.name = "User";
  return {
    name: "Neo",
    age: 85,
    getInfo() {
      // 일반함수 내부에서의 this 키워드는 호출되는 위치에서 정의된다.
      return `${this.name}는 ${this.age}세입니다.`;
    },
  };
}

const u = new User();
console.log(u.name);
console.log(u.age);
console.log(u.getInfo()); // 호출하게 되면 u 라는 인스턴스가 this가 될 수 있다.

const evan = {
  name: "Evan",
  age: 25,
};

console.log(u.getInfo.call(evan)); // 이 부분에서는 evan 객체가 this가 될 수 있다.
```

<br>

**간단한 예시(화살표함수)**

```js
function User() {
  // this 키워드가 사용된 화살표 함수를 감싸는 가장 가까운 함수가 현재 this키워드를 정의하는 영역이 된다.
  this.name = "User"; // 선언위치에서 this가 정의된다.
  return {
    name: "Neo",
    age: 85,
    getInfo: () => {
      // 화살표 함수일때의 this 는 선언위치
      return `${this.name}는 ${this.age}세입니다.`;
    },
  };
}

const u = new User();
console.log(u.name);
console.log(u.age);
console.log(u.getInfo());

const evan = {
  name: "Evan",
  age: 25,
};

console.log(u.getInfo.call(evan));
```

<br>

**간단한 예시(그 외)**

```js
function createTimer(message, duration) {
  return {
    message: message,
    timeout() {
      return setTimeout(() => {
        console.log(this.message);
      }, duration);
    },
  };
}

const t1 = createTimer("T1", 1000);
t1.timeout();
1;
const t2 = createTimer("T2", 3000);
t2.timeout();
```

<br>

```js
Array.prototype.abc = function () {
  return this.map((item) => {
    return item.toUpperCase();
  });
};

const fruits = ["apple", "banana", "cherry"];
const flowers = ["rose", "tulip", "lily"];
console.log(fruits.abc());
console.log(flowers.abc());
```
