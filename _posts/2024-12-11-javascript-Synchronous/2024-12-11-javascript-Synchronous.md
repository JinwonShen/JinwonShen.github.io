---
layout: post
title: "(javascript/js) 동기 비동기"
date: 2024-12-11 22:50:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - 동기(Synchronous)
discription:
---

## 동기(Synchronous)

하나의 작업이 끝나기 전에는 다음 작업이 시작되지 않는다.

### 간단한 예시

```js
console.log(1);
console.log(2);

alert("확인!"); // alert 창이 발생하기 전에 log(3) 이후 작업이 진행되지 않음.

console.log(3);
console.time("Loop!");
for (let i = 0; i < 100000000; i++) {}
console.timeEnd("Loop!");
console.log(4);

// 1
// 2
// 3
// Loop!: 68.593017578125 ms
// 4
```

<br>

## 비동기(Asynchronous)

특정 작업이 끝나기 전에 다음 작업이 시작될 수 있다.

### 간단한 예시

```js
console.log(1);
console.log(2);
console.log(3);
console.time("Loop!");

setTimeout(() => {
  for (let i = 0; i < 100000000; i++) {}
  console.timeEnd("Loop");
}, 0);

// 1
// 2
// 3
// 4
// Loop!: 45.551025390625 ms
// 5
```

<br>

```js
console.log(1);
const h1El = document.querySelector("h1");
// 사용자가 클릭하지 않으면 실행되지 않는다. 비동기 방식으로 실행.
h1El.addEventListener("click", () => {
  console.log("클릭!");
});
console.log(2);
```

<br>

```js
console.log(1);
// 서버와의 통신도 병렬로 즉, 비동기 방식으로 실행이 된다.
fetch("https://api.heropy.dev/v0/users")
  .then((res) => res.json())
  .then((data) => console.log(data));
console.log(2);
```

<br>

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="pvzEyyp" data-pen-title="js/비동기(Asynchronous)" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/pvzEyyp">
  js/비동기(Asynchronous)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
