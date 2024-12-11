---
layout: post
title: "(javascript/js) Array(배열) 표준 내장 객체"
date: 2024-12-08 16:41:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Array
  - .length()
  - .at()
  - .concat()
  - .every()
  - .filter()
  - .find()
  - .findIndex()
  - .forEach()
  - .includes()
  - .join()
  - .map()
  - .push()
discription:
---

# Array(배열) 표준 내장 객체(built-in-object)

## .length()

배열의 길이(숫자)를 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="bNbpvQG" data-pen-title="js/array(built-in-object)/.length()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/bNbpvQG">
  js/array(built-in-object)/.length()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .at()

배열을 인덱싱하며, 음수를 사용하면 뒤에서부터 인덱싱한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="pvzyLQb" data-pen-title="js/array(built-in-object)/.at()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/pvzyLQb">
  js/array(built-in-object)/.at()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .concat()

배열에서 주어진 배열을 병합해 새로운 배열을 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="xbKVWQp" data-pen-title="js/array(built-in-object)/.concat()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/xbKVWQp">
  js/array(built-in-object)/.concat()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .every()

배열의 모든 요소가(개별로) 콜백 테스트를 통과하는지 확인한다. 만약 테스트가 하나라도 실패한다면, 이후 테스트는 진행하지 않고 `false`를 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ogvxqQy" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ogvxqQy">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .filter()

배열에서 콜백 테스트를 통과하는 모든 요소로 새로운 배열을 만들어 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="LEPNdqr" data-pen-title="js/array(built-in-object)/.filter()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/LEPNdqr">
  js/array(built-in-object)/.filter()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .find()

배열에서 콜백 테스트를 처음으로 통과하는 요소를 반환한다. 처음 테스트가 통과하면, 이후 테스트는 진행하지 않는다. 모든 테스트가 실패하면, `undefined`를 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="GgKZxzL" data-pen-title="js/array(built-in-object)/.find()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/GgKZxzL">
  js/array(built-in-object)/.find()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .findIndex()

배열에서 콜백 테스트를 처음으로 통과하는 요소의 인덱스를 반환한다. 만약 테스트를 통과하면 이후 테스트는 진행하지 않는다. 만약 모든 테스트가 실패하면, `-1`을 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="QwLNmoy" data-pen-title="js/array(built-in-object)/.findIndex()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/QwLNmoy">
  js/array(built-in-object)/.findIndex()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .forEach()

배열의 각 요소에 대해 콜백을 호출한다. 만약 배열이 비어있다면, 아무런 동작도 하지 않는다. 만약 반복을 종료하고 싶다면, `for` 반복문을 사용해야 한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="PwYNRLr" data-pen-title="js/array(built-in-object)/.forEach()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/PwYNRLr">
  js/array(built-in-object)/.forEach()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .includes()

배열에서 특정 요소가 포함되어 있는지 확인한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="pvzyVJR" data-pen-title="js/array(built-in-object)/.includes()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/pvzyVJR">
  js/array(built-in-object)/.includes()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .join()

배열의 모든 요소를 연결해 하나의 문자열로 만든다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="MYgyGwo" data-pen-title="js/array(built-in-object)/.join()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/MYgyGwo">
  js/array(built-in-object)/.join()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .map()

배열의 모든 요소에 대해 각 콜백을 호출하고 반환된 결과를 새로운 배열로 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="KwPzRda" data-pen-title="js/array(built-in-object)/.map()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/KwPzRda">
  js/array(built-in-object)/.map()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .push()

배열의 마지막에 하나 이상의 요소를 추가하고, 배열의 새로운 길이를 반환한다.

배열의 원본이 변경된다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="JoPXvYB" data-pen-title="js/array(built-in-object)/.push()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/JoPXvYB">
  js/array(built-in-object)/.push()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .reduce()

배열의 각 요소에 대해 콜백을 호출하고, 각 콜백의 반환 값을 다음 콜백으로 전달해 마지막 반환 값을 최종 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="dPbMeGw" data-pen-title="js/array(built-in-object)/.reduce()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/dPbMeGw">
  js/array(built-in-object)/.reduce()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .reverse()

배열의 순서를 반전한다.

배열의 원본이 변경된다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="pvzyVEP" data-pen-title="js/array(built-in-object)/.reverse()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/pvzyVEP">
  js/array(built-in-object)/.reverse()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .slice()

배열의 일부를 추출해 새로운 배열로 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="dPbMepa" data-pen-title="js/array(built-in-object)/.slice()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/dPbMepa">
  js/array(built-in-object)/.slice()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .sume()

배열의 요소 중 콜백 테스트를 통과하는 요소가 하나라도 있는지 확인한다. 만약 테스트가 통과하면 이후 테스트는 진행하지 않는다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="pvzyVNP" data-pen-title="js/array(built-in-object)/.some()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/pvzyVNP">
  js/array(built-in-object)/.some()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .sort()

배열의 요소를 콜백의 반환 값에 따라 정렬한다. 콜백함수를 제공하지 않는다면, 요소를 유니코드 포인트 순서대로 정렬한다.

배열의 원본이 변경된다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="dPbMeOr" data-pen-title="js/array(built-in-object)/.sort()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/dPbMeOr">
  js/array(built-in-object)/.sort()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .splice(인덱스, 삭제계수, 추가요소)

배열의 요소를 추가하거나 삭제하거나 교체한다.

배열의 원본이 변경된다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="QwLNrdd" data-pen-title="js/array(built-in-object)/,splice()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/QwLNrdd">
  js/array(built-in-object)/,splice()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .unshift()

배열의 "시작" 부분에 하나 이상의 요소를 추가하고, 배열의 새로운 길이를 반환한다.

배열의 원본이 변경된다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="emOZrgy" data-pen-title="js/array(built-in-object)/.shift()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/emOZrgy">
  js/array(built-in-object)/.shift()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .callBackIndex()

배열의 메소드의 콜백은 항상 현재 반복의 인덱스를 얻을 수 있다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="mybPLWb" data-pen-title="js/array(built-in-object)/callBackIndex" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/mybPLWb">
  js/array(built-in-object)/callBackIndex</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .array-isArray()

배열 데이터인지 확인한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="QwLNrpd" data-pen-title="js/array(built-in-object)/.isArray()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/QwLNrpd">
  js/array(built-in-object)/.isArray()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## .array-from()

유사 배열(`array-like`)을 실제 배열로 반환한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="azoNGJj" data-pen-title="js/array(built-in-object)/.from()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/azoNGJj">
  js/array(built-in-object)/.from()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
