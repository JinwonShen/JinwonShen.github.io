---
layout: post
title: "(javascript/js) 이벤트(event)"
date: 2024-12-09 18:08:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - event
  - .addEventListener()
  - .removeEventListener()
  - .event.preventDefault()
  - .event.stopPropagation()
  - event Bubbling
  - event Capturing
  - event.isComposing
  - 마우스와 포인터 이벤트
  - 키보드 이벤트
  - 폼 양식 이벤트
discription:
---

# 이벤트(event)

## 대상.addEventListener(이벤트 종류, 핸들러)

대상에서 `청취(Listen)`할 이벤트 종류와 이벤트가 발생했을 때 호출할 `콜백(Handler)`을 등록한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="KwPzOym" data-pen-title="js/event" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/KwPzOym">
  js/event</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 대상.removeEventListener(이벤트 종류, 핸들러)

대상에 등록했던 이벤트 핸들러를 제거한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ZYzOzGM" data-pen-title="js/event/대상.removeEventListener()" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ZYzOzGM">
  js/event/대상.removeEventListener()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 이벤트 객체 / 대상.addEventListener(이벤트 종류, 핸들러)

핸들러의 첫 매개변수로, 발생한 이벤트의 정보를 가진 객체를 전달한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="wBwWwWq" data-pen-title="js/event/.addEventListener(이벤트 종류,  핸들러), 이벤트 객체" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/wBwWwWq">
  js/event/.addEventListener(이벤트 종류,  핸들러), 이벤트 객체</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## event.preventDefault()

이벤트의 기본 동작을 방지한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="NPKrKdX" data-pen-title="js/event/preventDefault()" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NPKrKdX">
  js/event/preventDefault()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 이벤트 버블링(event Bubbling) / event.stopPropagation()

하위 요소에서 상위 요소로의 이벤트 전파(버블)를 정지한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="MYgewNM" data-pen-title="js/event/event.stopPropagation()" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/MYgewNM">
  js/event/event.stopPropagation()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 이벤트 캡처링(Event Capturing) / .addEventListener(이벤트 종류, 이벤트 핸들러, 옵션)

`{ capture: true }` 는 이벤트 캡쳐를 활성화한다.

이벤트가 발생한 **가장 하위 요소에서 상위 요소로 올라가는 개념**은 이벤트의 버블링(`Event bubbling`)이라고 하고, 캡쳐를 통해 **상위 요소에서 하위 요소로 내려가는 개념**은 캡쳐링(`Event capturing`) 이라고 한다.

```
버블링(자동) : 하 -> 상

캡쳐링(수동) : 상 -> 하
```

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="dPbXWOo" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/dPbXWOo">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 한글 입력 이벤트 중복 / event.isComposing

브라우저 입력기(IME)의 CJK(중국어, 일본어, 한글) 문자 구성 중에는 이벤트 핸들러가 2번 실행될 수 있는데, `event.isComposing` 속성을 통해 그 여부를 확인한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ByBzRRd" data-pen-title="js/event/event.isComposing" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ByBzRRd">
  js/event/event.isComposing</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 마우스와 포인터 이벤트

`click` - 클릭

`dblclick` - 더블 클릭

`contextmenu` - 우클릭

`mousedown` - 버튼을 누를 때

`mouseup` - 버튼을 뗄 때

`mouseenter` - 포인터가 요소로 들어갈 때

`mouseleave` - 포인터가 요소에서 나올 때

`wheel` - 휠 버튼이 회전할 때

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="JoPKNVG" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/JoPKNVG">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 키보드 이벤트

`keydown` - 키를 누를 때

`keyup` - 키를 뗼 때

일반적으로는 `keydown`을 사용하나, 특정 상황에서 키를 뗄 때 이벤트가 필요한 이벤트가 있으면 `keyup` 을 사용한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="azoZwgL" data-pen-title="js/event/키보드 이벤트" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/azoZwgL">
  js/event/키보드 이벤트</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 양식(Form) 이벤트

`focus(focusin)` - 요소가 포커스를 얻었을 때

`blur(focusout)` - 요소가 포커스를 잃었을 때

`input` - 값이 변경되었을 때

`change` - 상태가 변경되었을 때

`submit` - 폼 요소에서 입력한 특정한 값들을 서버로 전송하기위해 `submit` 타입을 가지고 있는 버튼을 클릭했을 때 발생하는 `submit` 이벤트

`reset` - 타입이 `reset` 인 요소를 선택했을 떄 `reset` 이벤트 발생

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="XJrKarg" data-pen-title="js/form event(양식이벤트)" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/XJrKarg">
  js/form event(양식이벤트)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
