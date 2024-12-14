---
layout: post
title: "(javascript/js) Number(숫자) 표준 내장 객체"
date: 2024-12-08 13:50:00 +09:00
lastmode: 2024-12-08 13:50:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Number
  - .toFixed()
  - .toLocaleString()
  - .parseInt()
  - .parseIntFloat()
  - .isInteger()
  - .isNaN()
discription:
---

# Number(숫자) 표준 내장 객체(built-in-object)

## .toFixed()

숫자에서 지정된 문자로 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="xbKVYeO" data-pen-title="js/number(built-in-object)/.toFixed()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/xbKVYeO">
  js/number(built-in-object)/.toFixed()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .toLocaleString()

숫자에서 현지 언어형식으로 바꾼 새로운 문자를 반환한다. 목적에 따라 숫자데이터로 표기할지 문자데이터로 표기할지 선택 가능

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ByBKYEP" data-pen-title="js/number(built-in-object)/.toLocaleString()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ByBKYEP">
  js/number(built-in-object)/.toLocaleString()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## Number(), Number.parseInt(), Number.parseFloat()

데이터에서 사용하는 메소드를 `데이터 프로토타입 메소드`라고하고 클래스에서 사용되는 메소드는 `정적 메소드`라고 한다. 대문자로 시작하는 데이터를 클래스라고 한다.

```js
// 더 광범위하게 해석, 유연함, 의도하지 않은 결과가 나올 수 있다.
console.log("Number(데이터)");
console.log(Number("123"));
console.log(Number("123.456"));
console.log(Number("abc123"));
console.log(Number("123abc"));
console.log(Number(""));
console.log(Number("abc"));
console.log(Number(true));
console.log(Number(false));
console.log(Number({}));
console.log(Number([]));
```

<br>

**따라하기 (parseInt)**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="qEWZxzR" data-pen-title="js/number(built-in-object)/.parseInt()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/qEWZxzR">
  js/number(built-in-object)/.parseInt()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

**따라하기 (parseFloat)**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="LEPNQKW" data-pen-title="js/number(built-in-object)/.parseFloat()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/LEPNQKW">
  js/number(built-in-object)/.parseFloat()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .isInteger()

데이터가 정수(숫자 데이터)인지 확인한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="bNbpLPQ" data-pen-title="js/number(built-in-object)/.isInteger()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/bNbpLPQ">
  js/number(built-in-object)/.isInteger()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .isNaN()

데이터가 `NaN`인지 확인한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="raBeJXV" data-pen-title="js/number(built-in-object)/.isNaN()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/raBeJXV">
  js/number(built-in-object)/.isNaN()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
