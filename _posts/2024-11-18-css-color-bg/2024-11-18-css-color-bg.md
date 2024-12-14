---
layout: post
title: "(css) 색상과 배경"
date: 2024-11-18 11:53:00 +09:00
lastmode: 2024-11-18 11:53:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - hex(16진수)
  - rgb
  - opacity
  - background-color
  - background-image
  - background-repeat
  - background-position
  - background-oritin
  - background-size
  - background
discription:
---

# 색상과 배경

## 색상 - HEX(16진수), RGB, RGBA

`color` css 속성은 요소의 글씨 및 글씨 장식의 전경색과 `<currentcolor>`의 값을 설정한다. `currentcolor`는 다른 속성에서 사용할 수 있는 간접적인 것이며, `border-color`등 일부 속성의 기본값이다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="zYgXXwJ" data-pen-title="color" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/zYgXXwJ">
  color</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## opacity

`opacity` css 속성은 요소의 불투명도를 설정한다. 불투명도는 요소 뒤에 있는 콘텐츠가 숨겨지는 정도이며 투명도의 반대이다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="rNXbbJZ" data-pen-title="opacity" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/rNXbbJZ">
  opacity</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## background-color

css `background-color`속성은 요소의 배경 색을 지정한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="oNKOOyv" data-pen-title="background-color" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/oNKOOyv">
  background-color</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## background-image/repeat/position/origin/size

css 다양한 background- 속성을 보면,

- `background-image` css 속성은 요소의 배경 이미지를 한 개나 여러 개 지정한다.

```css
.img-cont {
  background-image: url("startransparent.gif"), url("catfront.png");
}
```

<br>

- `background-repeat` css 속성은 배경 이미지의 반복 방법을 지정한다. 가로축 및 세로축을 따라 반복할 수 있고, 아예 반복하지 않을 수도 있다.

```css
.img-cont {
  background-image: url("startransparent.gif"), url("catfront.png");
  background-repeat: no-repeat;
}

/* 키워드 값 */
background-repeat: repeat-x;
background-repeat: repeat-y;
background-repeat: repeat;
background-repeat: space;
background-repeat: round;
background-repeat: no-repeat;

/* 2개 값 구문: 가로 | 세로 */
background-repeat: repeat space;
background-repeat: repeat repeat;
background-repeat: round space;
background-repeat: no-repeat round;

/* 전역 값 */
background-repeat: inherit;
background-repeat: initial;
background-repeat: unset;
```

<br>

- `background-position` css 속성은 배경 이미지의 초기 위치를 설정한다. 위치는 `background-position`에서 설정한 위치 레이어를 기준으로 한다.

```css
.img-cont {
  background-image: url("startransparent.gif"), url("catfront.png");
  background-position: 0px 0px, right 3em bottom 2em;
}

/* Keyword values */
background-position: top;
background-position: bottom;
background-position: left;
background-position: right;
background-position: center;

/* <percentage> values */
background-position: 25% 75%;

/* <length> values */
background-position: 0 0;
background-position: 1cm 2cm;
background-position: 10ch 8em;

/* Multiple images */
background-position: 0 0, center;

/* Edge offsets values */
background-position: bottom 10px right 20px;
background-position: right 3em bottom 10px;
background-position: bottom 10px right;
background-position: top right 10px;

/* Global values */
background-position: inherit;
background-position: initial;
background-position: revert;
background-position: revert-layer;
background-position: unset;
```

<br>

- `background-origin` css 속성은 배경의 원점을 테두리 시작점, 테두리 내부, 안쪽 여백 중 하나로 지정한다.

```css
.img-cont {
  background-image: url("startransparent.gif"), url("catfront.png");
  background-origin: content-box;
}

/* 키워드 값 */
background-origin: border-box;
background-origin: padding-box;
background-origin: content-box;

/* 전역 값 */
background-origin: inherit;
background-origin: initial;
background-origin: unset;
```

<br>

- `background-size` css 속성은 배경 이미지의 크기를 설정한다. 이미지는 자연스러운 크기로 두거나, 늘리거나, 사용 가능한 공간에 맞게 제한할 수 있다.

```css
.img-cont {
  background-image: url("startransparent.gif"), url("catfront.png");
  background-size: 150px;
}
```

<br>

## background(shothand)

단축형 css 속성은 색상, 이미지, 원점 및 크기 또는 반복 방법과 같은 모든 배경 스타일 속성을 한 번에 설정한다. 단축형 속성 값 선언에 설정되지 않은 구성 요소 속성은 기본값으로 설정된다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="mdNggjP" data-pen-title="background-image" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/mdNggjP">
  background-image</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
