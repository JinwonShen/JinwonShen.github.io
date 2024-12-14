---
layout: post
title: "(javascript/js) boolean, null, undefined"
date: 2024-12-06 11:39:00 +09:00
lastmode: 2024-12-06 11:39:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - boolean
  - "null"
  - undefined
discription:
---

## boolean

불린 `boolean` 은 `true`와 `false` 두 가지 값인 참/거짓의 논리 데이터이다.

### 간단한 예시

```js
const a = true;
const b = false;

console.log(a, b);

// 긍정일 때
if (a) {
  console.log("참(Truthy)입니다!");
}

// 데이터를 서로 비교해, 참과 거짓을 판단한다.
const n1 = 1;
const n2 = 9;

console.log(n1 < n2);
```

<br>

## null

`null` 데이터는 존재하지 않는(nothing), 비어 있는(empty), 알 수 없는(unknown) 값을 명시적으로 나타낸다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="OPLMKMy" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/OPLMKMy">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## undefined

`undefined` 데이터는, '값이 할당되지 않은 상태'를 나타낼 때 사용한다.

변수는 선언했지만, 값은 할당하지 않았다면 해당 변수에 `undefined`가 암시적으로 할당된다.

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="XJrXvWZ" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/XJrXvWZ">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
