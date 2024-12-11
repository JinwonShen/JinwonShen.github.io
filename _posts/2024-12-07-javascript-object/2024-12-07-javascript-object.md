---
layout: post
title: "(javascript/js) object"
date: 2024-12-07 01:16:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - object
discription:
---

## object

`object` 객체 데이터는 순서가 없는 `Key`(키)와 `Value`(값)의 쌍으로 이루어진 데이터 집합이다.

객체에 포함된 각 데이터를 속성(`Property`)라고 부르고, 그 데이터가 함수인 경우에는, 메소드(`method`)라고 부른다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="xbKVxKq" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/xbKVxKq">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### `object` 생성자는 주어진 값에 대한 객체 래퍼를 생성한다.

- 값이 `null` 또는 `undefined`이면 빈 객체를 생성하여 반환한다.
- 그렇지 않으면 주어진 값에 해당하는 타입의 객체를 반환한다.
- 값이 이미 객체인 경우 그 값을 반환한다.
