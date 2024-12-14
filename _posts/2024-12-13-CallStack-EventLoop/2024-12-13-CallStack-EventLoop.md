---
layout: post
title: "(javascript/js) 콜 스택(Call Stack)과 이벤트 루프(Event Loop)"
date: 2024-12-13 22:53:00 +09:00
lastmode: 2024-12-13 22:53:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Call Stack(LIFO)
  - Event Loop
discription:
---

## 콜 스택과 이벤트 루프

자바스크립트는 저수준의 오래 걸릴 수 있는 일(`Timer`, `Network` 등)은 `Web API`에게 위임하고, 고수준의 작업은 자바스크립트 엔진(싱글 스레드)에서 처리하는 방식으로 빠른 속도와 높은 확장성을 유지한다.

- `FIFO(First In First Out)`: 선입선출, 먼저 들어온 데이터가 먼저 나감
- `LIFO(Last In First Out)`: 후입선출, 마지막에 들어온 데이터가 먼저 나감

<br>

**간단한 예시**

```js
function a() {
  // Call Stack(LIFO)
  console.log("A");
  function b() {
    setTimeout(() => {
      // Web APIs -> Event Loop(FIFO)
      console.log("B1");
      console.log("B2");
      // 4. B1
      // 5. B2
      // 싱글 스레드 방식에서 자바스크립트는 Timer, Network 등을 Wep APIs에게 위임하고
      // 모든 Call Stack이 종료되면 Event Loop로 이동해 호출 및 종료한다.
    }, 0);
  }
  b();
}
function c() {
  // Call Stack(LIFO)
  console.log("C");
}
function first() {
  // Call Stack(LIFO)
  a();
  // 1. A
  c();
  // 2. C
}
function second() {
  // Call Stack(LIFO)
  c();
  // 3. C
}
first();
second();
```

<br>

<figure>
<img src="/assets/img/CallStack-EventLoop-img.svg" alt="CallStack-EventLoop">
<figcaption>Call Stack(LIFO)과 Event Loop(FIFO)</figcaption>
</figure>

<br>

> 스택에 함수를 쌓고 소비하고 비우고 하는 과정들을 반복하는데 최대로 쌓을 수 있는 스택이 차버린 경우에는 더이상 스텍의 함수를 쌓을 수 없기 떄문에 자바스크립트는 최대 호출 스택 크기를 초과했다는 메시지를 보여주고, 더이상 스택에 쌓을 수 없는 함수들은 실행할 수 없게 된다. 기본적으로는 1mb 정도가 최대로보인다.
