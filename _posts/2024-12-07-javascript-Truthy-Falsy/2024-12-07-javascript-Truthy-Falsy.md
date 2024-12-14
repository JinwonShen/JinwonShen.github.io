---
layout: post
title: "(javascript/js) Truthy, Falsy"
date: 2024-12-07 15:32:00 +09:00
lastmode: 2024-12-07 15:32:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Truthy
  - Falsy
discription:
---

## Truthy(참으로 평가되는 값)

### 간단한 예시

```js
if (true) {
  console.log("참!");
}
if ({}) {
  console.log("참!");
}
if ([]) {
  console.log("참!");
}
if (42) {
  console.log("참!");
}
if ("0") {
  console.log("참!");
}
if ("false") {
  console.log("참!");
}
if (new Date()) {
  console.log("참!");
}
if (-42) {
  console.log("참!");
}
if (12n) {
  console.log("참!");
}
if (3.14) {
  console.log("참!");
}
if (-3.14) {
  console.log("참!");
}
if (Infinity) {
  console.log("참!");
}
if (-Infinity) {
  console.log("참!");
}
// ...
```

<br>

## Falsy(거짓으로 평가되는 값)

### 간단한 예시

```js
if (false) {
  console.log("거짓..");
}
if (null) {
  console.log("거짓..");
}
if (undefined) {
  console.log("거짓..");
}
if (0) {
  console.log("거짓..");
}
if (-0) {
  console.log("거짓..");
}
if (NaN) {
  console.log("거짓..");
}
if (0n) {
  console.log("거짓..");
}
if ("") {
  console.log("거짓..");
}
// 공백도 문자로 표기하기에 공백이 있으면 '참' 없다면 '거짓'으로 판단
```

<br>

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="wBwGzoW" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/wBwGzoW">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
