---
layout: post
title:  "(css) transform"
date:   2024-11-18 14:07:00 +09:00
categories: notice
usemathjax: true
tag:
  - transform
  - scale
  - rotate
  - translate
  - skew
  - transform-origin
discription: 
---

# transform

css `transform` 속성으로 요소에 회전, 크기조절, 기울이기, 이동 효과를 부여할 수 있다. `transform`은 css 시각적 서식 모델의 좌표 공간을 변경한다.

<br>

```css
/* 키워드 값 */
transform: none;

/* 함수 값 */
transform: matrix(1, 2, 3, 4, 5, 6);
transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
transform: perspective(17px);
transform: rotate(0.5turn);
transform: rotate3d(1, 2, 3, 10deg);
transform: rotateX(10deg);
transform: rotateY(10deg);
transform: rotateZ(10deg);
transform: translate(12px, 50%);
transform: translate3d(12px, 50%, 3em);
transform: translateX(2em);
transform: translateY(3in);
transform: translateZ(2px);
transform: scale(2, 0.5);
transform: scale3d(2.5, 1.2, 0.3);
transform: scaleX(2);
transform: scaleY(0.5);
transform: scaleZ(0.3);
transform: skew(30deg, 20deg);
transform: skewX(30deg);
transform: skewY(1.07rad);

/* 다중 함수 값 */
transform: translateX(10px) rotate(10deg) translateY(5px);
transform: perspective(500px) translate(10px, 0, 20px) rotateY(3deg);

/* 전역 값 */
transform: inherit;
transform: initial;
transform: unset;
```

<br>

## scale - 크기

`scale()` css 함수는 2D 평면에서 요소의 크기를 조정하는 변환을 정의한다. 수평 및 수직 차원을 다른 스케일로 조정할 수 있다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="RwXOOXG" data-pen-title="background-scale()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/RwXOOXG">
  background-scale()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## rotate - 회전

`rotate()` css 함수는 2D 평면의 고정된 지점을 중심으로 요소를 회전시키는 변환을 정의하지만, 변형은 하지 않는다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="xxveNKK" data-pen-title="background-rotate()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/xxveNKK">
  background-rotate()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## translate - 이동

`translate()` css 함수는 요소의 위치를 수평 또는 수직 방향으로 변경하거나, 수평 및 수직 방향으로 변경한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="XWvQwrQ" data-pen-title="transform-translate" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/XWvQwrQ">
  transform-translate</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## skew - 기울이기

`skew()` css 함수는 2D 평면에서 요소를 왜곡하는 변형을 정의한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="XWvQwmw" data-pen-title="transform-skew()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/XWvQwmw">
  transform-skew()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## origin - 기준점

`transform-origin` 속성은 요소의 변형에 대한 원점을 설정한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="RwXOmrK" data-pen-title="trnasform-origin" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/RwXOmrK">
  trnasform-origin</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>


