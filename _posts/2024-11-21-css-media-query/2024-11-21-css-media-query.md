---
layout: post
title:  "(css) grid"
date:   2024-11-20 17:15:00 +09:00
categories: notice
usemathjax: true
tag:
  - @media
  - media query
  - breakpoint
discription: 
---

# 반응형 디자인

반응형 웹 설계는 웹 페이지가 모든 화면 크기와 해상도에서 잘 렌더링 되도록 하면서도 사용성을 보장하는 웹 디자인 접근 방식이다. 멀티 디바이스 웹을 위한 디자인 방식.

## media query basic

미디어 쿼리를 사용하면 일련의 테스트(예: 사용자의 화면이 특정 너비 또는 특정 해상도보다 큰지 여부)를 실행하고 css룰 선택적으로 적용해 사용자의 요구에 맞게 페이지의 스타일을 지정할 수 있다.


```css
@media screen and (max-width: 300px) {
  .container {
    background-color: pink;
  }
}
```

<br>

### "논리곱" 미디어 쿼리

`and`를 사용해 미디어 기능을 결합할 수 있습니다. 이는 마치 앞에서 미디어 유형과 기능을 결합하기 위해 `and`를 사용했던 방식과 같다. 예를 들어, `min-width와` `orientation`의 논리곱 조건을 테스트해 보고 싶을 수도 있다. 여기서 HTML 본문 텍스트가 파란색이 되는 유일한 경우는 뷰포트의 너비가 최소 600픽셀 이상이고 장치가 가로 모드인 경우에만 해당한다.


```css
/* landscape : 가로모드 */
@media screen and (min-width: 600px) and (orientation: landscape) {
  body {
    color: blue;
  }
}
```

### breakpoint

#### 모바일 우선(mobile first) breakpoint

모바일 우선으로 css작성할 때 동일한 요소에 동일한 속성을 여러 조건의 미디어쿼리를 작성할 때에는 `min-width`의 작은 값을 먼저 작성해 너비값이 오름차순이 되도록 기입한다.

```css
/* 모바일 */
body {  background-color: #ccc;}

@media (min-width: 576px) {
  body {    background-color: #fcc;  }
}

@media (min-width: 768px) {
  body {    background-color: #cfc;  }
}

@media (min-width: 992px) {
  body {    background-color: #ccf;  }
}

@media (min-width: 1200px) {
  body {    background-color: #fcf;  }
}

@media (min-width: 1400px) {
  body {    background-color: #ffc;  }
}
```

<br>

#### 데스크탑 우선 breakpoint

데스크탑 우선으로 css를 작성할 떄는 동일한 요소에 속성을 여러 조건의 미디어쿼리를 작성할 때에는 max-width의 큰 값을 먼저 작성하여 너비값이 내림차순이 되게 기입한다.

```css
body {  background-color: #ccc;}

@media (max-width: 1400px) {
  body {    background-color: #ffc;  }
}

@media (max-width: 1200px) {
  body {    background-color: #fcf;  }
}

@media (max-width: 992px) {
  body {    background-color: #ccf;  }
}

@media (max-width: 768px) {
  body {    background-color: #cfc;  }
}

@media (max-width: 576px) {
  body {    background-color: #fcc;  }
}
```

<br>

### 반응형 실습 !

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="dyxBJrE" data-pen-title="반응형 실습" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/dyxBJrE">
  반응형 실습</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>