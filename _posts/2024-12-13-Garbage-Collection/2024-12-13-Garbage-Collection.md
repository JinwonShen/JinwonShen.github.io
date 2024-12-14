---
layout: post
title: "(javascript/js) 가비지 컬렉션(Garbage Collection)"
date: 2024-12-13 21:06:00 +09:00
lastmode: 2024-12-13 21:06:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Garbage Collection
  - Memory Leak
discription:
---

## 가비지 컬렉션(Garbage Collection)

`가비지 컬렉션(Garbage Collection)`이란, 더 이상 사용되지 않는 메모리를 해제하는 프로세스로 자바스크립트 엔진이 자동으로 처리한다.

## 메모리 누수(Memory Leak)

더 이상 필요치 않은 데이터가 해제되지 못해 메모리를 계속 차지되는 것을 말한다.

<br>

### 간단한 예시

**불필요한 데이터 참조를 피하세요 !**

```js
const user = {
  name: "Neo",
  age: 85,
  emails: ["bosv031999@gmail.com", "bosv031999s@naver.com"],
};
// 개선 전
// const removedEmail = user.emails.splice(1, 1);
// 개선 후
user.emails.splice(1, 1);
console.log(user.emails);
```

<br>

**불필요한 전역 변수 사용을 피하세요 ! window 객체는 가장 상위 객체(최상위 객체)**

```js
window.hello = "Hello world!";
window.heropy = { name: "Heropy", age: 85 };
```

<br>

**제거된 요소가 참조되지 않도록 주의하세요 !**

```js
// 개선 전
const h1El = document.querySelector("h1");
window.addEventListener("click", () => {
  console.log(h1El);
  h1El.remove();
});

// 개선 후
window.addEventListener("click", () => {
  const h1El = document.querySelector("h1");
  if (h1El) {
    console.log(h1El);
    h1El.remove();
  }
});
```

<br>

**불필요한 타이머를 해제하세요 !**

```js
// 개선전
let a = 0;
setInterval(() => {
  a += 1;
}, 100);
setTimeout(() => {
  console.log(a);
}, 1000);

// 개선 후
let a = 0;
const intervalId = setInterval(() => {
  a += 1;
}, 100);
setTimeout(() => {
  console.log(a);
  clearInterval(intervalId);
}, 1000);
```

<br>

**불필요한 클로저를 제거하세요 !**

```js
// 개선 전
const getFn = (x) => {
  return (name) => {
    x += 1;
    console.log(x);
    return `Hello ${name}~`;
  };
};
const fn = getFn(0);
console.log(fn("Neo"));
console.log(fn("Lewis"));
fn("Evan");
fn("Amy");

// 개선 후
const getFn = (x) => {
  return (name) => {
    return `Hello ${name}~`;
  };
};
const fn = getFn(0);
console.log(fn("Neo"));
console.log(fn("Lewis"));
fn("Evan");
fn("Amy");
```

<br>
