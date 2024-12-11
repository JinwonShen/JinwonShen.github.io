---
layout: post
title: "(css) animation"
date: 2024-11-18 22:25:00 +09:00
categories: notice
usemathjax: true
tag:
  - animaion
  - keyframe
  - animation-name
  - animation-duration
  - animation-delay
  - animation-time-function
  - animation-iteration-count
  - animation-direction
  - animation-play-state
  - animation-fill-mode
discription:
---

# animation

## @keyframe

`@keyframes` @규칙은 개발자가 애니메이션 중간중간의 특정 지점들을 거칠 수 있는 키프레임들을 설정함으로써 css 애니메이션 과정의 중간 절차를 제어할 수 있게 한다. 이를 통해 브라우저가 `transitions`으로 애니메이션을 처리하는 것 보다 더 세밀하게 중간 동작들을 제어할 수 있다.

### 간단한 예시

```css
@keyframes slidein {
  from {
    transform: translateX(0%);
  }

  to {
    transform: translateX(100%);
  }
}
```

<br>

`from`

- 시작 offset인 0% 입니다.

`to`

- 마지막 offset인 100% 입니다.

<br>

### 간단 예제

```css
@keyframes identifier {
  0% {
    top: 0;
    left: 0;
  }
  30% {
    top: 50px;
  }
  68%,
  72% {
    left: 50px;
  }
  100% {
    top: 100px;
    left: 100%;
  }
}
```

- 여기 `top` 속성은 0%, 30%, 100% 키 프레임을 이용하여 애니메이션 되며, `left` 속성은 0%, 68%, 72%, 100% 키 프레임을 사용해 애니메이션 된다.

<br>

## animation-name, animation-duration

css 속성 `animation-name` 은 요소에 적용할 애니메이션을 설명하는 하나 이상의 at-규칙의 이름을 지정한다. 여러 at-규칙은 쉼표로 구분된 이름 목록으로 지정된다. 지정된 이름이 at-규칙과 일치하지 않으면 속성에 애니메이션이 적용되지 않는다. `animation-duration` 은 애니메이션이 한 사이클을 완료하는데 걸리는 시간을 지정한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="JjgqdLX" data-pen-title="animation-name/duration" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/JjgqdLX">
  animation-name/duration</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## animation-delay, animation-timimg-funtion

`animation-delay` css 속성은 애니메이션이 시작할 시점을 지정한다. 시작 즉시, 잠시 후에, 또는 애니메이션이 일부 진행한 시점부터 시작할 수 있다. `animation-timing-function` css 속성은 각 주기동안 애니메이션이 진행되는 방식을 설정한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="oNKRjXG" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/oNKRjXG">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## animation-iteration-count, animation-direction

`animation-iteration-count` css 속성은 애니메이션 시퀀스가 끝나기 전에 재생될 횟수를 설정한다. `animation-direction` 속성은 애니메이션이 앞으로, 뒤로 또는 앞뒤로 번갈아 재생되어야하는지 여부를 지정한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="VwoOvaQ" data-pen-title="animation-iteration-count, direction" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/VwoOvaQ">
  animation-iteration-count, direction</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## animation-play-state

`animation-play-state` css 속성은 애니메이션이 실행중인지 일시 중지 되었는지 설정한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="BaXeoxX" data-pen-title="animation-play-state" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/BaXeoxX">
  animation-play-state</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## animation-fill-mode

`animation-fill-mode` css 속성은 애니메이션이 실행 전과 후에 대상에 스타일을 적용하는 방법을 지정한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="QWeRjYN" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/QWeRjYN">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## animation(shorthand)

`animation` 단축 css 속성은 스타일 사이에 에니메이션을 적용한다. `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`, `animation-iteration-count`, `animation-direction`, `animation-fill-mode`, 그리고 `animation-play-state`의 단축형이다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="poMmjXR" data-pen-title="animation(shorthand)" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/poMmjXR">
  animation(shorthand)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 간단한 예시

```css
/* @keyframes duration | easing-function | delay |
iteration-count | direction | fill-mode | play-state | name */
animation: 3s ease-in 1s 2 reverse both paused slidein;

/* @keyframes duration | easing-function | delay | name */
animation: 3s linear 1s slidein;

/* 애니메이션 두 개 */
animation: 3s linear slidein, 3s ease-out 5s slideout;
```
