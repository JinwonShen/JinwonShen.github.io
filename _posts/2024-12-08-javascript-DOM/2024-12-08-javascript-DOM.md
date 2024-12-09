---
layout: post
title: "(javascript/js) DOM(Document Object Model)"
date: 2024-12-08 20:19:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - DOM
  - Document Object Model
  - 노드(Node)
  - 요소(Element)
discription:
---

## DOM(Document Object Model)

`DOM(Document Object Model)` 이란, `HTML` 문서를 객체로 표현한 것으로 `JS` 에서 `HTML` 을 제어할 수 있게 해준다.

### 노트(Node)

요소, 텍스트, 주석 등의 각 구조를 의미한다.

### 요소(Element)

노드의 하위 객체로 요소를 의미한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="MYgyXPd" data-pen-title="js/DOM &amp;amp; Node &amp;amp; Element" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/MYgyXPd">
  js/DOM &amp; Node &amp; Element</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 검색과 탐색

### document.querySelector(선택자)

선택자로 검색한 요소를 하나 반환한다. 만약 검색자가 없으면, `null`을 반환한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="NPKNJOK" data-pen-title="js/document.querySelector(선택자)" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NPKNJOK">
  js/document.querySelector(선택자)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### document.querySelectorAll(선택자)

선택자로 검색한 모든 요소를 `NodeList` 객체로 반환한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ByBKbGg" data-pen-title="js/document.querySelectorAll(선택자)" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ByBKbGg">
  js/document.querySelectorAll(선택자)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

NodeList 객체는 유사배열이며, `.forEach()` 메소드는 내장되어 있지만, 기타 배열 메소드는 사용할 수 없다.

<br>

### document.getElementById(아이디)

html `id` 속성(Attributes) 값으로 검색한 요소를 하나 반환한다. 만약 검색 결과가 없다면, `null` 을 반환한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="qEWZvvo" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/qEWZvvo">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 노드.parentElement

노드의 부모요소를 반환한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="NPKNJmP" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NPKNJmP">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 요소.previousElementSibling / nextElementSibling

요소의 이전 형제 요소/다음 형제 요소를 반환한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="bNbpZyG" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/bNbpZyG">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 요소.children

요소의 모든 자식 요소를 반환한다.

### 요소.firstElementChild / 요소.lastElementChild

요소의 첫 번째/마지막 자식 요소를 반환한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="wBwGOVv" data-pen-title="js/요소.children &amp;amp; firstElementChild &amp;amp; lastElementChild" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/wBwGOVv">
  js/요소.children &amp; firstElementChild &amp; lastElementChild</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## DOM - 생성, 조회, 수정

### document.createElement(태그이름)

html 요소를 메모리상에 생성해 반환한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="jENqRdG" data-pen-title="js/createElement(태그이름)" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/jENqRdG">
  js/createElement(태그이름)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 요소.prepend(노드1, 노드2, ...)

하나 이상의 노드를 요소의 첫 번째 자식으로 삽입한다.

### 요소.append(노드1, 노드2, ...)

하나 이상의 노드를 요소의 마지막 자식으로 삽입한다.

### 노드.appendChild(노드1)

하나 이상의 노드를 마지막 자식으로 삽입하고 삽입한 노드를 반환한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ByBKEep" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ByBKEep">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 요소.remove()

요소를 제거한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="pvzyBXL" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/pvzyBXL">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 노드.contains()

주어진 노드가 대상 노드를 포함한 후손인지 확인한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="MYgyRNX" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/MYgyRNX">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 노드.textContent

노드의 모든 텍스트를 확인(get)하거나 지정(set)한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="pvzymzL" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/pvzymzL">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 요소.innerHTML

요소의 내부 html을 확인(Get)하거나 지정(Set)한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="VYZaOwL" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/VYZaOwL">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 요소.dataset

요소의 `data-` 속성을 확인(Get)하거나 지정(Set)한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="dPbMEMo" data-pen-title="js/요소.dataset" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/dPbMEMo">
  js/요소.dataset</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

- 따라하기(다른유형의 .dataset)

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="GgKZaNr" data-pen-title="js/요소.dataset(2)" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/GgKZaNr">
  js/요소.dataset(2)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 요소.classList / 요소.classList.add() / 요소.classList.remove() / 요소.classList.toggle() / 요소.classList.contains()

요소의 `class` 속성을 제어한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="KwPzLZG" data-pen-title="js/classList &amp;amp; .add() &amp;amp; .remove() &amp;amp; .toggle() &amp;amp; .contains()" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/KwPzLZG">
  js/classList &amp; .add() &amp; .remove() &amp; .toggle() &amp; .contains()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 요소.style

요소의 `style` 속성을 확인(Get)하거나 지정(Set)한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="zxOqQWO" data-pen-title="js/요소.style" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
<span>See the Pen <a href="https://codepen.io/sjinwon/pen/zxOqQWO">
js/요소.style</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

- 따라하기(다른유형의)

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="NPKNZbJ" data-pen-title="js/요소.style(다른유형의)" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NPKNZbJ">
  js/요소.style(다른유형의)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 요소.getAttribute(속성) / 요소.setAttribute(속성, 값) / 요소.hasAttribute(속성) / 요소.removeAttribute(속성)

`요소.getAttribute(속성)` - 요소의 속성을 확인한다.

`요소.setAttribute(속성)` - 요소의 속성과 값을 지정한다.

`요소.hasAttribute(속성)` - 요소의 속성이 있는지 확인한다.

`요소.removeAttribute(속성)` - 요소의 속성을 제거한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="WbewqpB" data-pen-title="js/요소.getAttribute(속성) &amp;amp; .setAttribute(속성, 값) &amp;amp; .hasAttribute(속성) &amp;amp; .removeAttribute(속성)" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/WbewqpB">
  js/요소.getAttribute(속성) &amp; .setAttribute(속성, 값) &amp; .hasAttribute(속성) &amp; .removeAttribute(속성)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## DOM - 크기와 좌표

### window.innerWidth / window.innerHeight / window.scrollX / window.scrollY

`window.innerWidth` - 화면(Viewport)의 너비를 얻는다.

`window.innerHeight` - 화면의 높이를 얻는다.

`window.scrollX` - 화면에서 스크롤된 X축의 위치를 얻는다.

`window.scrollY` - 화면에서 스크롤된 Y축의 위치를 얻는다.

- 따라하기

<br>

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="qEWZzVP" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/qEWZzVP">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### window.scrollTo(), 요소.scrollTo()

지정된 좌표로 대상을 스크롤한다.

### 구문

```js
// 첫 번째 방식
대상.scrollTo(x좌표, y좌표);

// 두 번째 방식
대상.scrollTo({
  left: x좌표,
  top: y좌표,
  behavior: "smooth", // 자연스럽게 이동
});
```

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="VYZaJGd" data-pen-title="js/window.innerWidth / window.innerHeight / window.scrollX / window.scrollY(2)" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/VYZaJGd">
  js/window.innerWidth / window.innerHeight / window.scrollX / window.scrollY(2)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 요소.offsetWidth / 요소.offsetHeight / 요소.clientWidth / 요소.clientHeight / 요소.scrollWidth / 요소.scrollHeight

`요소.offsetWidth` - 테두리 선을 포함한 요소의 너비를 얻는다.

`요소.offsetHeight` - 테두리 선을 포함한 요소의 높이를 얻는다.

`요소.clientWidth` - 테두리 선을 제외한 요소의 너비를 얻는다.

`요소.clientHeight` - 테두리 선을 제외한 요소의 높이를 얻는다.

`요소.scrollWidth` - 테두리 선을 제외한 요소의 스크롤 영역 너비를 얻는다.

`요소.scrollHeight` - 테두리 선을 제외한 요소의 스크롤 영역 높이를 얻는다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ZYzWdmB" data-pen-title="js/요소.offsetWidth(Height) / 요소.clientWidth(Height) / 요소.scrollWidth(Height)" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ZYzWdmB">
  js/요소.offsetWidth(Height) / 요소.clientWidth(Height) / 요소.scrollWidth(Height)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
