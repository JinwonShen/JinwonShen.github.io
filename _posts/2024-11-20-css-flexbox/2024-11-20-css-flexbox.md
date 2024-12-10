---
layout: post
title: "(css) flex box"
date: 2024-11-20 11:29:00 +09:00
categories: notice
usemathjax: true
tag:
  - flexbox
  - flex container
  - flex item
  - main axis
  - cross axis
  - flex-direction
  - flex-wrap
  - flex-flow
  - flex-grow
  - flex-basis
  - flex
  - justify-content
  - align-items
  - align-content
  - align-self
discription:
---

# flexbox

`flexbox`는 행과 열 형태로 항목 무리를 배치하는 일차원 레이아웃 메서드이다. 항목은 부족한 공간에 맞추기 위해 축소되거나 여분의 공간을 채우기 위해 변형된다. 이 문서는 근간이 되는 내용 전체를 설명한다.

## flex container, flex item, main axis, cross axis

기본적으로 flex는 부모요소와 자식요소 관계를 정확하게 알고 있어야 한다.

```html
<!-- 부모요소 -->
<div class="container">
  <!-- 자식요소/부모요소 -->
  <div class="item">
    <!-- 자식요소 -->
    <span></span>
    <span></span>
  </div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

- `flex container` : 부모요소
- `flex item` : 자식요소
- `main axis` : 주축(왼쪽 -> 오른쪽)
- `cross axis` : 교차축(위 -> 아래)

<br>

## container - display

`display` css 속성은 요소를 블록 또는 인라인 상자로 처리할지 여부와 자식 요소에 사용되는 레이아웃(예: flow layout, grid 또는 flex)을 설정한다.

형식적으로, `display`속성은 요소의 내부 및 외부 디스플레이 유형을 설정한다. 외부 유형은 요소의 흐름 레이아웃 참여를 설정하고, 내부 유형은 자식의 레이아웃을 설정한다. 일부 값은 `display`자체 개별 사양에서 완전히 정의된다. 예를 들어 `display: flex`선언 시 발생하는 내용의 세부 사항은 CSS Flexible Box Model 사양에서 정의된다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="mdNZdpj" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/mdNZdpj">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## flex-direction

`flex-direction` css 속성은 플렉스 컨테이너 내의 아이템을 배치할 떄 사용할 주축 및 방향(정방향, 역방향)을 지정한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="rNXENdM" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/rNXENdM">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## flex-wrap

css `flex-wrap` property는 `flex-item` 요소들이 강제로 한줄에 배치되게 할 것인지, 가능한 영역 내에서 벗어나지 않고 여러 행으로 나누어 표현 할 것인지 결정하는 속성이다. 요소의 방향 축을 결정할 수도 있다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="WNVqNYN" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/WNVqNYN">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## flex-flow

`flex-flow` css 속성은 `flex-direction`, `flex-wrap` 속성의 단축속성이다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="WNVqNYN" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/WNVqNYN">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## order

`order`css 속성은 플렉스 혹은 그리드 컨테이너 안에서 현재 요소의 배치 순서를 지정한다. 컨테이너 아이템의 정렬 순서는 오름차순 `order` 값이고, 같은 값일 경우 소스 코드의 순서대로 정렬된다.

<br>

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="XWvLWOR" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/XWvLWOR">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## flex-grow

`flex-grow` CSS property 는 `flex-item` 요소가, `flex-container` 요소 내부에서 할당 가능한 공간의 정도를 선언한다. 만약 형제 요소로 렌더링 된 모든 `flex-item` 요소들이 동일한 `flex-grow` 값을 갖는다면, `flex-container` 내부에서 동일한 공간을 할당받는다. 하지만 `flex-grow` 값으로 다른 소수값을 지정한다면, 그에 따라 다른 공간값을 나누어 할당받게 된다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="jOgjEew" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/jOgjEew">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## flex-shrink

`flex-shrink` CSS property는 `flex-item` 요소의 `flex-shrink` 값을 설정하는 속성이다. 만약 `flex-item` 요소의 크기가 `flex-container` 요소의 크기보다 클 때 `flex-shrink` 속성을 사용하는데, 설정된 숫자값에 따라 `flex-container` 요소 내부에서 `flex-item` 요소의 크기가 축소된다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="jOgjEew" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/jOgjEew">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## flex-basis

`flex-basis` CSS 속성은 플렉스 아이템의 초기 크기를 지정합니다. `box-sizing`을 따로 지정하지 않는다면 콘텐츠 박스의 크기를 변경합니다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="ExqBaqG" data-pen-title="flex-basis" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ExqBaqG">
  flex-basis</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

- 쉽게 이야기하면 `flex-basis`는 자신의 `width` 값이 지정되지 않았을 때 `Contents box`의 사이즈를 버리거나 원하는 크기로 지정할 수 있다.

<br>

## flex(shorthand)

`flex CSS` 속성은 하나의 플렉스 아이템이 자신의 컨테이너가 차지하는 공간에 맞추기 위해 크기를 키우거나 줄이는 방법을 설정하는 속성이다. `flex`는 `flex-grow`, `flex-shrink`, `flex-basis`의 단축 속성입니다.

<br>

### 간단한 예시

```css
/* Keyword values */
flex: auto;
flex: initial;
flex: none;

/* One value, unitless number: flex-grow */
flex: 2;

/* One value, length or percentage: flex-basis */
flex: 10em;
flex: 30%;

/* Two values: flex-grow | flex-basis */
flex: 1 30px;

/* Two values: flex-grow | flex-shrink */
flex: 2 2;

/* Three values: flex-grow | flex-shrink | flex-basis */
flex: 2 2 10%;

/* Global values */
flex: inherit;
flex: initial;
flex: unset;
```

<br>

## justify-content

CSS의 `justify-content` 속성은 브라우저가 콘텐츠 항목 사이와 주변의 공간을 플렉스 컨테이너에서는 `main-axis`, 그리고 그리드 컨테이너에서는 인라인 축을 기준으로 어떻게 정렬할 것인지를 정의한다.

### 간단한 예시

```css
/* 위치 기준 정렬 */
justify-content: center; /* 항목들을 축의 중심 부분에 정렬합니다. */
justify-content: start; /* 항목들을 축의 시작 부분에 정렬합니다.. */
justify-content: end; /* 항목들을 축의 끝 부분에 정렬합니다. */
justify-content: flex-start; /* 플렉스 항목들을 축의 시작 부분에 정렬합니다. */
justify-content: flex-end; /* 플렉스 항목들을 축의 끝 부분에 정렬합니다. */
justify-content: left; /* 항목들을 축의 왼쪽 부분에 정렬합니다. */
justify-content: right; /* 항목들을 축의 오른쪽 부분에 정렬합니다. */

/* 기준선 정렬 */
/* justify-content은 기준선에 대한 값은 갖지 않습니다. */

/* 기본 정렬 */
justify-content: normal;

/* 분산 정렬 */
justify-content: space-between; /* 항목들을 고르게 정렬합니다.
                                   첫 항목은 시작 부분에 밀착되어 정렬됩니다.
                                   마지막 항목은 끝 부분에 밀착되어 정렬됩니다. */
justify-content: space-around; /* 항목들을 고르게 정렬합니다. 
                                   각 항목들은 양쪽 여백의 절반만큼 나누어 갖습니다. */
justify-content: space-evenly; /* 항목들을 고르게 정렬합니다.
                                   각 항목들은 서로 간에 동일한 여백을 갖습니다. */
justify-content: stretch; /* 항목들을 고르게 정렬합니다.
                                   'auto' 크기로 설정된 항목들을 컨테이너에 맞게 늘립니다. */

/* 오버플로우 정렬 */
justify-content: safe center;
justify-content: unsafe center;

/* 전역 값들 */
justify-content: inherit;
justify-content: initial;
justify-content: revert;
justify-content: revert-layer;
justify-content: unset;
```

<br>

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="GRVbJqN" data-pen-title="justify-contents" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/GRVbJqN">
  justify-contents</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## align-items

CSS `align-items` 속성은 모든 직계 자식에 대해 `align-self`값을 그룹으로 설정한다. 플렉스박스의 교차축을 따라 아이템을 정렬합니다. 그리드 레이아웃의 그리드 영역내 블록 축을 따라 아이템을 정렬한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="zYgVGBb" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/zYgVGBb">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## align-content

CSS `align-content` 속성은 콘텐츠 사이와 콘텐츠 주위 빈 공간을 플렉스 박스'의 교차축 또는 그리드의 블록 축을 따라 배치하는 방식을 결정한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="jOgjPMz" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/jOgjPMz">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## align-self

css `align-self` 속성은 그리드 또는 플렉스 항목의 값을 재정의한다. 그리드에서 그리드 영역 내부에 항목을 정렬한다. 플렉스 박스에서 교차 축에 항목을 정렬한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="oNKrXBX" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/oNKrXBX">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
