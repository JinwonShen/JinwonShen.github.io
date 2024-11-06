---
layout: post
title:  "html의 구조를 나타내는"
date:   2024-11-06 22:14:00 +09:00
categories: notice
usemathjax: true
tag:
  - html
  - 콘텐츠 분할요소
  - div
  - span
discription: 
---

# 컨테이너 (div, span)

### div, span

html `<div>`요소는 흐름 콘텐츠의 일반 컨테이너이다. css를 사용해 어떤 식으로든 스타일을 정하기 전까지는 콘텐츠나 레이아웃에 영향을 미치지 않는다.<br>
`<span>`은 구문적 내용을 위한 일반적인 인라인 컨테이너로, 본질적으로 아무것도 나타내지 않는다. 스타일링 목적으로 요소를 그룹화하는데 사용할 수 있다. div요소와 매우 흡사하지만 `<div>`는 블록 수준 요소인 반면 `<span>`은 인라인 수준 요소이다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="NWQLeQN" data-pen-title="div, span" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NWQLeQN">
  div, span</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

"순수한 컨테이너로서, 이 `<div>` 요소는 본질적으로 아무것도 나타내지 않는다. 대신, 콘텐츠를 그룹화해 `class` 또는 `id` 속성을 쉽게 사용해 스타일을 지정할 수 있고, 문서의 섹션을 다른 언어로 작성되었음을 표시하는 등의 용도로 사용된다.

```
참고: div의 align속성은 더 이상 사용되지 않습니다. 더 이상 사용하지 마세요. 대신 CSS Grid 또는 CSS Flexbox<div> 와 같은 CSS 속성이나 기술을 사용하여 페이지에서 요소를 정렬하고 배치해야 합니다 .
```

<br>

### header, footer

html `<header>`는 일반적으로 소개 또는 탐색 보조 도구의 그룹을 나타낸다. 여기에는 몇 가지 제목 요소가 포함될 수 있지만, 로고 검색양식, 작성자 이름 및 기타 요소도 포함될 수 있다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="NWQLorb" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NWQLorb">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### nav

html요소 `<nav>`는 현재 문서 내부 또는 다른 문서의 탐색 링크를 제공하는 것이 목적인 페이지 섹션을 나타낸다. 일반적으로 메뉴, 목차, 인덱스 등이 있다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="ExqerNe" data-pen-title="nav" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ExqerNe">
  nav</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### aside

html 요소 `<aside>`는 문서의 주요 내용과 간접적으로만 관련이 있는 문서의 일부를 나타낸다. `<aside>`는 종종 사이드바 또는 콜아웃 상자로 표시된다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="ZEgMwLr" data-pen-title="aside" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ZEgMwLr">
  aside</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>