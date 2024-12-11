---
layout: post
title: "(javascript/js) Date(날짜) 표준 내장 객체"
date: 2024-12-08 16:00:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Date
  - new Date()
  - .getTime()
  - Date.now()
discription:
---

# Date(날짜) 표준 내장 객체(Built-in-Object)

## new Date()

`new Date()`를 통해 반환된 인스턴스를 `타임스탬프(Timestamp)`라고 한다.

`new`라는 키워드와 함께 호출하는 함수(클리스)를 `생성자 함수`라고 한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="pvzyLPv" data-pen-title="js/Date(built-in-object)/.new Date()/get-" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/pvzyLPv">
  js/Date(built-in-object)/.new Date()/get-</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .getTime() / Date.now()

`.getTime()` 유닉스 타임(UNIX Time)으로부터 경과한 시간(ms)을 반환한다.
`Date.now()` 현재 시간을 유닉스 타임으로 반환한다.

유닉스 타임이란, 1970.01.01 00:00:00 시간을 의미한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="QwLNmgL" data-pen-title="js/Date(built-in-object)/.getTime() &amp;amp; Date.now()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/QwLNmgL">
  js/Date(built-in-object)/.getTime() &amp; Date.now()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
