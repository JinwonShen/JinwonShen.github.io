---
layout: post
title: "(javascript/js) string(문자) 표준 내장 객체"
date: 2024-12-08 01:32:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - string
  - .length
  - .includes()
  - .replace()
  - .replaceAll()
  - .slice()
  - .split()
  - .toLowerCase()
  - .toUpperCase()
  - .trim()
discription:
---

# String(문자) 표준 내장 객체(Built-in-Object)

## .length

문자의 길이(숫자)를 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="GgKZvNR" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/GgKZvNR">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .includes()

문자에서 특정 문자가 포함되어 있는지 확인한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="dPbMzNL" data-pen-title="js/string/.includes()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/dPbMzNL">
  js/string/.includes()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .replace()

문자에서 특정 문자를 다른 문자로 "모두" 바꾼 새로운 문자를 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="raBezyd" data-pen-title="js/string/.replcae()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/raBezyd">
  js/string/.replcae()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .replaceAll()

문자에서 특정 문자를 다른 문자로 바꾼 새로운 문자를 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="LEPNjyq" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/LEPNjyq">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .slice()

문자에서 일부를 추출해 새로운 문자를 반환한다.

`(*, *)` 두 번째 인수의 바로 직전까지만 추출 마지막 글자까지 추출하려면 첫 번째 인수만 작성한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="WbewEZp" data-pen-title="js/string(built-in-object)/.slice()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/WbewEZp">
  js/string(built-in-object)/.slice()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .split()

문자를 구분자로 나누어 배열로 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ogvxeoR" data-pen-title="js/string(built-in-object)/.split()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ogvxeoR">
  js/string(built-in-object)/.split()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## toLowerCase(), toUpperCase()

문자를 영어 소문자로 혹은 대문자로 바꾼 새로운 문자로 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ByBKdJL" data-pen-title="js/string(built-in-object)/.toLowerCase() &amp;amp; .toUpperCase()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ByBKdJL">
  js/string(built-in-object)/.toLowerCase() &amp; .toUpperCase()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .trim()

문자에서 앞뒤 공백을 제거한 새로운 문자를 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="dPbMzJB" data-pen-title="js/string(built-in-object)/.trim()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/dPbMzJB">
  js/string(built-in-object)/.trim()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
