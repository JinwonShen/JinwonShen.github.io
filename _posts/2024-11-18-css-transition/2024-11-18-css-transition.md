---
layout: post
title: "(css) transition"
date: 2024-11-18 14:57:00 +09:00
lastmode: 2024-11-18 14:57:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - transition
  - transition-property-1
  - transition-property-2
  - transition-timing-function
  - transition
  - transform
discription:
---

# transition

`transition` css 속성은 `transition-property`, `transition-duration`, `transition-timing-function`과 `transition-delay`를 위한 단축 속성으로 엘리먼트의 두 가지 상태 사이에 변화를 줄 수 있다. 엘리먼트의 각 상태는 가상 클래스를 사용해 정의된 `:hover`나 `:active` 또는 자바스크립트를 사용해 동적으로 만들어진 것들이다.

<br>

초기값

- transition-delay : 0s
- transition-duration : 0s
- transition-property : all
- transition-timimg-funtion : ease

<br>

### 간단한 예시

```css
/* Apply to 1 property */
/* property name | duration */
transition: margin-left 4s;

/* property name | duration | delay */
transition: margin-left 4s 1s;

/* property name | duration | timing function | delay */
transition: margin-left 4s ease-in-out 1s;

/* Apply to 2 properties */
transition: margin-left 4s, color 1s;

/* Apply to all changed properties */
transition: all 0.5s ease-out;
```

이 속성에서 각 항목의 순서는 중요하다. 시간으로 해석될 수 있는 값이 첫 번째에 위치한다면 `transition-duration` 으로 적용되고, 두 번째에 위치한다면 `transition-delay`로 적용된다.

<br>

## transition-property, transition-duration

`transition-property` CSS 속성은 transition effect 을 적용해야 하는 CSS 속성을 명시한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="mdNYedL" data-pen-title="transition-" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/mdNYedL">
  transition-</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## transition-delay, trnasition-timing-function

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="bGXJyKm" data-pen-title="transition-property" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/bGXJyKm">
  transition-property</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## trnasition + transform 활용예시

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="xxveNMR" data-pen-title="transition + transform 활용" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/xxveNMR">
  transition + transform 활용</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
