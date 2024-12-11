---
layout: post
title: "(css) font 관련 속성"
date: 2024-11-16 21:53:00 +09:00
categories: notice
usemathjax: true
tag:
  - value(값)
  - units(단위)
  - 숫자
  - 길이
  - 절대길이
  - 상대길이
  - 백분율
  - em
  - rem
  - 위치(position)
discription:
---

# css 값과 단위

css 규칙은 선언으로 구성되어 있으며, 이는 다시 속성과 값으로 이루어져 있다. css 에서 사용되는 각 속성은 어떤 종류의 값을 가질 수 있는지를 설명하는 값 유형을 가지고 있다.

## css 값이란 무엇인가?

css 사양과 mdn의 속성 페이지에서 `<color>`또는 `<length>`와 같이 꺾쇠괄호로 묶여 있는 값을 찾을 수 있다. `<color>`값이 특정 속성에 유효한 것으로 표시되면, `<color>` 참조 페이지에 나열된 대로 유효한 속성을 해당 속성의 값으로 사용할 수 있다.

**따라하기**

```css
h1 {
  color: black;
  background-color: rgb(197, 93, 223);
}
```

## 숫자, 길이 및 백분율

css에서 사용할 수 있는 다양한 숫자 데이터 형식이 있다.

| 데이터 형식    | 설명                                                                                                                                                                 |
| :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `<integer>`    | `<integer>` 은 `1024`또는 `-55` 와 같은 정수이다.                                                                                                                    |
| `<number>`     | `<number>` 은 10진수를 나타낸다. 소수점 이하의 소수 자릿수 (예:`0.255`, `128`또는 `-1.2`)가 있을 수도 있고 없을 수도 있다.                                           |
| `<dimension>`  | `<dimension>` 은 예를 들어 `45deg`, `5s` 또는 `10px` 과 같은 단위가 붙어있는 `<number>` 이다.                                                                        |
| `<percentage>` | `<percentage>` 는 다른 값의 일부, 예를 들어 `50%` 를 나타낸다. 백분율 값을 항상 다른 수량을 기준으로 한다. 예를 들어 요소의 길이는 부모 요소의 길이를 기준으로 한다. |

### 길이

가장 자주 사용되는 숫자 형식은 `<length>`이다. 예를 들면 `10px`(픽셀) 또는 `30em`. css 에서 사용되는 길이는 상대 및 절대의 두 가지 유형이 있다. 얼마나 커질지 알기 위해서는 차이를 이해하는 것이 중요하다.

### 절대 길이 단위

다음은 모두 절대 길이 단위로 다른 것과 관련이 없으며 일반적으로 항상 동일한 크기로 간주된다.

| 단위 | 이름            | 다음과 동일함            |
| :--- | :-------------- | :----------------------- |
| `cm` | 센티미터        | 1cm = 37.8px = 25.2/64in |
| `mm` | 밀리미터        | 1mm = 1/10th of 1cm      |
| `Q`  | 4분의 1밀리미터 | 1Q = 1/40th of 1cm       |
| `in` | 인치            | 1in = 2.54cm = 96px      |
| `pc` | Picas           | 1pc = 1/6th of 1in       |
| `pt` | 포인트          | 1pt = 1/72nd of 1in      |
| `px` | 픽셀            | 1px = 1/96th of 1in      |

이러한 값으 ㅣ대부분은 화면 출력이 아닌 인쇄에 사용될 때 더 요용하다.

<br>

### 상대 길이 단위

상대 길이 단위는 다른 요소(상위요소의 글꼴 크기 또는 viewport크기)와 관련이 있다. 상대 단위를 사용하면 텍스트나 다른 요소의 크기가 페이지의 다른 모든 것에 비례하여 조정되도록 신중하게 계획할 수 있다는 이점이 있다.

| 단위         | 관련사항                                                                                                   |
| :----------- | :--------------------------------------------------------------------------------------------------------- |
| `em`         | 요소의 글꼴 크기.                                                                                          |
| `ex`         | 요소 글꼴의 x-height.                                                                                      |
| `ch`         | 요소 글꼴의 glyph "0"의 사전 길이 (너비)입니다.                                                            |
| `rem`        | 루트 요소의 글꼴 크기.                                                                                     |
| `lh`         | 요소의 라인 높이.                                                                                          |
| `rlh`        | 루트 요소의 라인 높이. 루트 요소의 font-size 또는 line-height 속성에 사용될 때 속성의 초깃값을 참조합니다. |
| `vw`         | 뷰포트의 초기 컨테이닝 블록 너비 1%와 같습니다.                                                            |
| `vh`         | 뷰포트의 초기 컨테이닝 블록 높이 1%와 같습니다.                                                            |
| `vmin`       | viewport의 작은 치수의 1%.                                                                                 |
| `vmax`       | viewport의 큰 치수의 1%.                                                                                   |
| `vb`         | 초기 컨테이닝 블록의 블록 축 크기 1%와 같습니다.                                                           |
| `vi`         | 초기 컨테이닝 블록의 인라인 축 크기 1%와 같습니다.                                                         |
| `svw`, `svh` | 작은 뷰포트 각각의 너비 및 높이 1%.                                                                        |
| `lvw`, `lvh` | 큰 뷰포트 각각의 너비 및 높이 1%.                                                                          |
| `dvw`, `dvh` | 동적인 뷰포트 각각의 너비 및 높이 1%.                                                                      |

<br>

- 예제로 일부 확인하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="qBewmZZ" data-pen-title="상대 및 절대길이" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/qBewmZZ">
  상대 및 절대길이</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### em및 rem

`em`과 `rem`은 박스에서 텍스트로 크기를 조정할 때 가장 자주 발생하는 두 개의 상대 길이다. 텍스트 스타일링 또는 css 레이아웃 보다 복잡한 주제를 시작할 때, 이러한 작동 방식과 차이점을 이해하는 것이 좋다.

먼저 `<html>`요소에서 글꼴 크기로 16px을 설정한다.

다시말해, `em` 단위는 "부모 요소의 글꼴 크기"를 의미한다. `<class>`가 있는 `<ul>`내부의 `<li>`요소는 부모로부터 크기를 가져온다. 따라서 각 중첩 부분은 글꼴 크기가 부모 글꼴 크기의 `1.3em`, 1.3배로 설정되므로 점점 더 커진다.

`rem`단위는 "루트 요소의 글꼴 크기"를 의미한다. ("root em"의 rem 이 표준) `rem` `class`가 있는 `<ul>` 내부의 `<li>`요소 루트 요소(`<html>`)에서 크기를 가져온다.

- 예제로 일부 확인하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="GRVLmjM" data-pen-title="em과 rem" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/GRVLmjM">
  em과 rem</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 함수(functions)

전통적인 프로그래밍 언어에서 찾아볼 수 있는 것과 비슷한 것은 `calc()` css 함수이다. 이 함수를 사용하면 css내에서 간단한 계산을 수행할 수 있다. 프로젝트의 css를 작성할 떄 정의할 수 없는 값을 계산하고 런타임에 브라우저가 작동해야 하는 경우 특히 유용하다.

예를 들어, 아래에서는 `calc()`를 사용하여 박스를 `20% + 100px` 너비로 만든다. 20%는 부모 container `.wrapper`의 너비에서 계산되므로 너비가 변경되면 변경된다. 우리는 부모 요소의 20%가 무엇인지 알지 못하기 때문에, 이 계산을 미리 수행할 수 없으므로 `calc()`를 사용하여 브라우저에 지시한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="XWvQRPX" data-pen-title="calc()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/XWvQRPX">
  calc()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
