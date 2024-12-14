---
layout: post
title: "(javascript/js) 선택적 체이닝(Optional Chaining)"
date: 2024-12-10 16:18:00 +09:00
lastmode: 2024-12-10 16:18:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - 선택적 체이닝(Optional Chaining)
discription:
---

## 선택적 체이닝(Optional Chaining)

`?.`대괄호 혹은 점 표기법의 대상이 `null` 혹은 `undefined` 인 경우, 에러 대신 `undefined`를 반환한다.

자바스크립트는 에러가 발생하면 에러가 발생한 뒤 코드가 모두 실행되지 않는데, `?.` 선택적 체이닝을 활용하면 에러를 `undefined(false)` 로 만들어 에러 뒤 코드를 실행할 수 있다.

### 간단한 예시

```js
console.log(null?.abc); // undefined
console.log(undefined?.abc); // undefined

const el = document.querySelector("h1");
console.log(el?.textContent); // undefined

// const numbers = [1, 2, 3]
const numbers = null;
console.log(numbers?.[0]); // undefined

// const user = {
//   name: 'Neo',
//   age: 22
// }
const user = null;
console.log(user?.name); // undefined
```

<br>

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="vEBKedX" data-pen-title="js/Optional Chaining(선택적 체이닝)" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/vEBKedX">
  js/Optional Chaining(선택적 체이닝)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
