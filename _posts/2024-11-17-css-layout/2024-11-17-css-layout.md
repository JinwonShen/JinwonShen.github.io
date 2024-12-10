---
layout: post
title: "(css) 레이아웃"
date: 2024-11-17 01:18:00 +09:00
categories: notice
usemathjax: true
tag:
  - 레이아웃
  - inline
  - block
  - inline-block
  - hidden
  - float
  - position
  - overflow
  - z-index
discription:
---

# 레이아웃

## inline, block, inline-block

css 속성 `display`는 요소를 블록 또는 인라인 상자로 처리할지 여부와 자식 요소에 사용되는 레이아웃(예:flow layout, grid 또는 flex)을 설정한다.

형식적으로, `display`속성은 요소의 내부 및 외부 디스플레이 유형을 설정한다. 외부 유형은 요소의 flow char 참여를 설정하고, 내부 유형은 자식의 레이아웃을 설정한다. 일부 값은 `display`자체 개별 사양에서 완전히 정의된다. 예를 들어 `display: flex` 선언 시 발생하는 내용의 세부 사항은 css Flexible Box Model 사양에서 정의된다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="yLmroeP" data-pen-title="display:inline, block, inline-block" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/yLmroeP">
  display:inline, block, inline-block</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

css `display` 속성은 키워드 값을 지정해 사용

```css
/* precomposed values */
display: block;
display: inline;
display: inline-block;
display: flex;
display: inline-flex;
display: grid;
display: inline-grid;
display: flow-root;

/* box generation */
display: none;
display: contents;

/* multi-keyword syntax */
display: block flex;
display: block flow;
display: block flow-root;
display: block grid;
display: inline flex;
display: inline flow;
display: inline flow-root;
display: inline grid;

/* other values */
display: table;
display: table-row; /* all table elements have an equivalent CSS display value */
display: list-item;

/* Global values */
display: inherit;
display: initial;
display: revert;
display: revert-layer;
display: unset;
```

<br>

### 그룹화된 값

키워드 값은 6가지 값 범주로 그룹화할 수 있다.

`<display-outside>`
이러한 키워드는 요소의 외부 디스플레이 유형을 지정하는데, 이는 본질적으로 흐름 레이아웃에서의 역할이다.

- `block` : 해당 요소는 블록 상자를 생성하고, 일반적인 흐름에서는 요소 앞과 뒤에 줄 바꿈을 생성한다.
- `inline` : 요소는 자체 앞이나 뒤에 줄 바꿈을 생성하지 않는 하나 이상의 인라인 상자를 생성한다. 일반적인 흐름에서 다음 요소는 공백이 있으면 같은 줄에 있다.

<br>

`<display-inside>`
이러한 키워드는 요소의 내부 표시 유형을 지정하는데, 이는 콘텐츠가 배치되는 서식 컨텍스트 유형을 정의한다.(대체되지 않은 요소인 경우).

- `flow` : 요소는 흐름 레이아웃(블록 및 인라인 레이아웃)을 사용하여 내용을 배치한다.
  외부 디스플레이 유형이 이고 inline블록 또는 인라인 포맷팅 컨텍스트에 참여하는 경우 인라인 상자를 생성한다. 그렇지 않으면 블록 상자를 생성한다. <br>
  position다른 속성(예: , float, 또는 ) 의 값 overflow과 블록 또는 인라인 서식 컨텍스트에 참여하는지 여부에 따라 콘텐츠에 대한 새 블록 서식 컨텍스트 (BFC)를 설정하거나 콘텐츠를 부모 서식 컨텍스트에 통합한다.
- `flow-root` : 해당 요소는 블록 상자를 생성하여 새로운 블록 서식 컨텍스트를 설정 하고 서식 루트가 있는 위치를 정의한다.
- `table` : 이러한 요소는 HTML `<table>`요소처럼 동작합니다. 블록 수준 상자를 정의한다.
- `flex` : 이 요소는 블록 수준 요소처럼 동작하며 flexbox 모델 에 따라 콘텐츠를 배치한다.
- `grid` : 이 요소는 블록 수준 요소처럼 동작하며 그리드 모델 에 따라 콘텐츠를 배치한다.
- `ruby` : 이 요소는 인라인 수준 요소처럼 동작하고 루비 포맷팅 모델에 따라 콘텐츠를 배치한다. 해당 HTML `<ruby>`요소처럼 동작한다.

<br>

## float

css 속성 `float`은 한 요소(element)가 보통 흐름(normal flow)으로부터 빠져 텍스트 및 인라인(inline)요소가 그 주위를 감싸는 자기 컨테이너의 좌우측을 따라 배치되어야 함을 지정한다.

<br>

```css
/* 키워드 값 */
float: left;
float: right;
float: none;
float: inline-start;
float: inline-end;

/* 전역 값 */
float: inherit;
float: initial;
float: unset;
```

<br>

### 값

- `left` : 는 요소가 자신의 포함(containing) 블록의 좌측에 부동(float, 떠움직여)해야 함을 나타내는 키워드이다.
- `right` : 는 요소가 자신의 포함 블록의 우측에 부동해야 함을 나타내는 키워드이다.
- `none` : 는 요소가 부동하지 않아야 함을 나타내는 키워드이다.
- `inline-start` : 는 요소가 자신의 포함 블록의 시작쪽에 부동해야 함을 나타내는 키워드이다. 즉, ltr(left to right) 스크립트 상에서 왼쪽 그리고 rtl(right to left) 스크립트 상에서는 오른쪽.
- `inline-end` : 는 요소가 자신의 포함 블록의 끝쪽에 부동해야 함을 나타내는 키워드이다. 즉, ltr 스크립트 상에서 오른쪽 그리고 rtl 스크립트 상에서는 왼쪽.

<br>

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="gOVyxGM" data-pen-title="float" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/gOVyxGM">
  float</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## position

css `position`속성은 문서 상에 요소를 배치하는 방법을 지정한다. `top`, `right`, `bottom`, `left`속성이 요소를 배치할 최종 위치를 결정한다.

`position` 속성은 아래의 목록에서 하나의 키워드 값을 선택해 지정할 수 있다.

### 값

- `static` : 요소를 일반적인 문서 흐름에 따라 배치한다. top, right, bottom, left, z-index 속성이 아무런 영향도 주지 않는다. 기본값이다.
- `relative` : 요소를 일반적인 문서 흐름에 따라 배치하고, 자기 자신을 기준으로 top, right, bottom, left의 값에 따라 오프셋을 적용한다. 오프셋은 다른 요소에는 영향을 주지 않는다. 따라서 페이지 레이아웃에서 요소가 차지하는 공간은 static일 때와 같다.<br>z-index의 값이 auto가 아니라면 새로운 쌓임 맥락을 생성. table-\*-group, table-row, table-column, table-cell, table-caption 요소에 적용했을 때의 작동 방식은 정의되지 않는다.
- `absolute` : 요소를 일반적인 문서 흐름에서 제거하고, 페이지 레이아웃에 공간도 배정하지 않는다. 대신 가장 가까운 위치 지정 조상 요소에 대해 상대적으로 배치한다. 단, 조상 중 위치 지정 요소가 없다면 초기 컨테이닝 블록을 기준으로 삼는다. 최종 위치는 top, right, bottom, left 값이 지정된다. <br>z-index의 값이 auto가 아니라면 새로운 쌓임 맥락을 생성한다. 절대 위치 지정 요소의 바깥 여백은 서로 상쇄되지 않는다.
- `fixed` : 요소를 일반적인 문서 흐름에서 제거하고, 페이지 레이아웃에 공간도 배정하지 않는다. 대신 뷰포트의 초기 컨테이닝 블록을 기준으로 삼아 배치한다. 단, 요소의 조상 중 하나가 transform, perspective, filter 속성 중 어느 하나라도 none이 아니라면 (CSS Transforms 명세 참조) 뷰포트 대신 그 조상을 컨테이닝 블록으로 삼는다. (perspective와 filter의 경우 브라우저별로 결과가 다름에 유의) 최종 위치는 top, right, bottom, left 값이 지정된다. <br>이 값은 항상 새로운 쌓임 맥락을 생성한다. 문서를 인쇄할 때는 해당 요소가 모든 페이지의 같은 위치에 출력된다.
- `sticky` : 요소를 일반적인 문서 흐름에 따라 배치하고, 테이블 관련 요소를 포함해 가장 가까운, 스크롤 되는 조상과, 표 관련 요소를 포함한 컨테이닝 블록(가장 가까운 블록 레벨 조상) 을 기준으로 top, right, bottom, left의 값에 따라 오프셋을 적용한다. 오프셋은 다른 요소에는 영향을 주지 않는다. <br>이 값은 항상 새로운 쌓임 맥락을 생성한다. 끈끈한 요소는 "스크롤 동작"(overflow가 hidden, scroll, auto 혹은 overlay)이 존재하는 가장 가까운 조상에 달라붙으며, 사실 그 조상은 스크롤 불가하며 실제로 스크롤 가능한 조상이 따로 존재할 경우 "끈끈한" 동작을 보이지 않는 점에 주의해야 한다. (W3C CSSWG의 Github 이슈 참조)

<br>

### 상대 위치 지정

상대적으로 배치된 요소는 문서 내 정상적인(normal) 위치에서 주어진 오프셋만큼 떨어지지만, 다른 요소에는 영향을 주지 않는다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="QWePMQO" data-pen-title="상대 위치 지정" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/QWePMQO">
  상대 위치 지정</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 절대 위치 지정

상대적으로 배치된 요소가 일반적인 문서 흐름에 따르는 것과 달리, 절대적으로 배치된 요소는 흐름에서 제거된다. 따라서 다른 요소는 그 요소가 존재하지 않는 것처럼 배치된다. 절대적으로 배치된 요소는 가장 가까운 위치 지정 조상(즉, `static`이 아닌 가장 가까운 조상)을 기준으로 배치된다. 그런 요소가 존재하지 않는다면, 초기 컨테이닝 블록이 기준이 된다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="qBewXoe" data-pen-title="절대 위치 지정" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/qBewXoe">
  절대 위치 지정</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 고정 위치 지정

고정 위치 지정은 절대 위치 지정과 비슷하지만, `fixed`는 요소의 컨테이닝 블록이 뷰포트의 초기 컨테이닝 블록이라는 점에서 다르다.(`transform`, `perspective`,`filter` 속성이 `none`이 아닌 조상이 있다면 그 조상이 컨테이닝 블록이 된다. css transforms spec 참조). 따라서 스크롤에 관계 없이 화면의 특정 지점에 고정되는, "떠다니는"(floating)요소를 생성할 수 있다. "One"상자는 페이지 위에서 80픽셀, 왼쪽에서 10픽셀 떨어진 위치에 고정된다. 스크롤을 하더라도, 뷰포트를 기준으로 같은 위치에 고정된 채로 유지된다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="xxveLjN" data-pen-title="고정 위치 지정" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/xxveLjN">
  고정 위치 지정</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## overflow

`overflow` css 단축 속성은 요소의 콘텐츠가 너무 커서 요소의 블록 서식 맥락에 맞출 수 없을 때의 처리법을 지정한다. `overflow-x`, `overflow-y`의 값을 설정한다.

<br>

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="yLmroqq" data-pen-title="overflow" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/yLmroqq">
  overflow</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

적용 가능한 방법은 잘라내기, 스크롤바 노출, 넘친 콘텐츠 그대로 노출 등이 있다.

`visible`(기본값)이 아닌 다른 값으로 `overflow` 속성을 사용할 경우 새로운 블록 서식 문맥을 생성한다. 이는 기술적인 요구사항으로, 만약 스크롤하는 요소와 `float이` 교차한다면, 각 스크롤 단계마다 내용물을 강제적으로 다시 감싸게 될 것이다. 이는 결국 스크롤 속도를 느리게 할 것이다.

overflow 속성이 효력을 갖기 위해선 반드시 블록 레벨 컨테이너의 높이(`height` 또는 `max-height`)를 설정하거나, white-space를 nowrap으로 설정해야 한다.

<br>

### 값

```css
/* 키워드 값 */
overflow: visible;
overflow: hidden;
overflow: clip;
overflow: scroll;
overflow: auto;
overflow: hidden visible;

/* 전역 값 */
overflow: inherit;
overflow: initial;
overflow: unset;
```

## z-index

css `z-index` 속성은 위치 지정 요소와, 그 자손 또는 하위 플렉스 아이템의 z축 순서를 지정한다. 더 큰 `z-index`값을 가진 요소가 작은 값의 요소 위를 덮는다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="GRVLvYN" data-pen-title="z-index" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/GRVLvYN">
  z-index</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

위치 지정 요소(`position`이 `static` 외의 다른 값인 요소)의 박스에 대해, `z-index` 속성은 다음 항목을 지정한다.

- 현재 쌓임 맥락에서 자신의 위치.
- 자신만의 쌓임 맥락 생성 여부.

### 값

```css
/* 키워드 값 */
z-index: auto;

/* <integer> 값 */
z-index: 0;
z-index: 3;
z-index: 289;
z-index: -1; /* 음수 값으로 우선순위를 낮출 수 있음 */

/* 전역 값 */
z-index: inherit;
z-index: initial;
z-index: unset;
```

<br>
