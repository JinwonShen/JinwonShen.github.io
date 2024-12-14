---
layout: post
title: "(html) html의 구조를 나타내는"
date: 2024-11-06 18:03:00 +09:00
lastmode: 2024-11-06 18:03:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - html
  - 콘텐츠 분할요소
  - div
  - span
  - header
  - footer
  - article
  - aside
  - section
  - 시맨틱 태그란
discription:
---

# 컨테이너 (div, span)

### div, span

html `<div>`요소는 흐름 콘텐츠의 일반 컨테이너이다. css를 사용해 어떤 식으로든 스타일을 정하기 전까지는 콘텐츠나 레이아웃에 영향을 미치지 않는다.<br>
`<span>`은 구문적 내용을 위한 일반적인 인라인 컨테이너로, 본질적으로 아무것도 나타내지 않는다. 스타일링 목적으로 요소를 그룹화하는데 사용할 수 있다. div요소와 매우 흡사하지만 `<div>`는 블록 수준 요소인 반면 `<span>`은 인라인 수준 요소이다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="NWQLeQN" data-pen-title="div, span" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NWQLeQN">
  div, span</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

"순수한 컨테이너로서, 이 `<div>` 요소는 본질적으로 아무것도 나타내지 않는다. 대신, 콘텐츠를 그룹화해 `class` 또는 `id` 속성을 쉽게 사용해 스타일을 지정할 수 있고, 문서의 섹션을 다른 언어로 작성되었음을 표시하는 등의 용도로 사용된다.

> 참고: div의 align속성은 더 이상 사용되지 않습니다. 더 이상 사용하지 마세요. 대신 CSS Grid 또는 CSS Flexbox<div> 와 같은 CSS 속성이나 기술을 사용하여 페이지에서 요소를 정렬하고 배치해야 합니다 .

<br>

### header, footer

html `<header>`는 일반적으로 소개 또는 탐색 보조 도구의 그룹을 나타낸다. 여기에는 몇 가지 제목 요소가 포함될 수 있지만, 로고 검색양식, 작성자 이름 및 기타 요소도 포함될 수 있다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="NWQLorb" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NWQLorb">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### nav

html요소 `<nav>`는 현재 문서 내부 또는 다른 문서의 탐색 링크를 제공하는 것이 목적인 페이지 섹션을 나타낸다. 일반적으로 메뉴, 목차, 인덱스 등이 있다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="ExqerNe" data-pen-title="nav" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ExqerNe">
  nav</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### aside

html 요소 `<aside>`는 문서의 주요 내용과 간접적으로만 관련이 있는 문서의 일부를 나타낸다. `<aside>`는 종종 사이드바 또는 콜아웃 상자로 표시된다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="ZEgMwLr" data-pen-title="aside" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ZEgMwLr">
  aside</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### main

html 요소 `<main>`은 문서의 주요 내용을 나타낸다. 주요 내용 영역은 문서의 중심 주제 또는 애플리케이션의 중심 기능과 직접 관련이 있거나 이를 확장하는 내용으로 구성된다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="xxvaMrm" data-pen-title="main" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/xxvaMrm">
  main</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 유의할 점

요소의 내용은 `<main>`문서에 고유해야 한다. 사이드바, 탐색링크, 저작권 정보, 사이트 로고, 검색 양식과 같이 문서나 문서 섹션에 걸쳐 반복되는 내용은 검색 양식이 페이지의 주요 기능이 아닌 한 포함해서는 안된다.

> 엄격한 정보 제공용이다.

<br>

### article

html `<article>`요소는 문서, 페이지, 애플리케이션 또는 사이트에서 독립적으로 배포되거나 재사용될 수 있도록 의도된 자체 포함 구성을 나타낸다. 예를 들어 게시물, 잡지 또는 신문 기사, 블로그 항목, 제품 카드, 사용자가 제출한 댓글, 대화형 위젯 또는 가젯 또는 기타 독립적인 콘텐츠 항목이 있습니다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="MWNqLOV" data-pen-title="article" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/MWNqLOV">
  article</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 유의할 점

- 각 요소는 일반적으로 요소의 자식으로 `<article>` 제목(h1 - h6 <article> 요소)를 포함해 식별해야 한다.
- 요소가 중첩되면 `<article>`내부 요소는 외부 요소와 관련된 기사를 나타낸다. 예를 들어, 블로그 게시물의 댓글은 블로그 게시물을 나타내는 `<article>`은 중첩된 요소가 될 수 있다.

<br>

### section

html `<section>`요소는 문서의 일반적인 독립형 섹션을 나타내며, 이를 나타낼 더 구체적인 의미적 요소가 없다. 섹션에는 항상 제목이 있어야 하며, 예외는 거의 없다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="zYgJbZO" data-pen-title="section" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/zYgJbZO">
  section</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 시맨틱(Semantics)태그란

프로그래밍에서, 시맨틱은 코드 조각의 '의미'를 나타낸다. 예를 들어, ("이게 어떻게 시각적으로 보여질까?" 보다는), 이 javascript 라인을 생성하는 것은 어떤 효과가 있나?, 혹은 "이 html 엘리먼트가 가진 목적이나 역할은 무엇일까?"를 들 수 있다.

> html은 채워질 '데이터'를 나타내도록 코딩해야 한다. 기본적인 프레젠테이션 스타일기반이 아니다. 프레젠테이션(어떻게 보여져야 하는가)는 css만의 역할이다.

<br>

#### 의미론적 마크업을 사용했을 때 이점

- 검색 엔진은 의미론적 마크업을 페이지의 검색 순위에 영향을 줄 수 있는 중요한 키워드로 간주한다.(seo참조).
- 시각 장애가 있는 사용자가 화면 판독기로 페이지를 탐색할 때 의미론적 마크업을 안내판으로 사용할 수 있다.
- 의미없고 클래스 이름이 붙여져있거나 그렇지 않은 끈임없는 `<div>`들을 탐색하는 것보다, 의미있는 코드 블록을 찾는 것이 훨씬 쉽다.
- 개발자에겐 태그 안에 채워질 데이터 유형을 제안한다.
- 의미있는 이름짓기(Semantic naming)는 적절한 사용자 정의 요소 / 구성 요소의 이름짓기를 반영한다.

> 사용자 마크업에 접글할 때, "채울 데이터를 가장 잘 설명하고 나타내는 요소는 무엇일까?" 스스로 에게 물어보자. 예를 들어, 그 데이터는 정렬된 목록인가? 정렬되지 않은 목록인가?, 관련된 정보가 제외된 섹션이 있는 글인가?, 캡션이 필요한 그림 또는 이미지인가 ? 등등을 들 수 있다.

<br>

#### 의미론적 요소들

`<article>`
`<aside>`
`<details>`
`<figcaption>`
`<figure>`
`<footer>`
`<form>`
`<header>`
`<main>`
`<mark>`
`<nav>`
`<section>`
`<summary>`
`<time>`
