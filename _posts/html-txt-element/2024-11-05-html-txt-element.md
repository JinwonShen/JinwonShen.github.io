---
layout: post
title:  "html 텍스트 요소"
date:   2024-11-05 22:14:00 +09:00
categories: notice
usemathjax: true
tag:
  - html
  - 텍스트요소
  - 본문태그
discription: 
---

# html 텍스트 요소

### 제목태그 h1 - h6

html 요소는 6단계의 구획 제목을 나타냅니다. 구획 단계는 `<h1>`이 가장 높고 `<h6>`이 가장 낮습니다.

#### 사용 시 유의할 점 한눈에 보기

```
글씨 크기를 위해 제목 태그를 사용해선 안 된다. 대신 css의 `font-size` 속성을 사용한다.

제목 단계를 건너 뛰는 것을 피해야 한다. 언제나 `h1` 로 시작해서 `h2` , 순차적으로 기입한다.

페이지 당 하나의 `h1` 을 사용한다. 여러 개를 사용해도 오류는 나지 않지만, 단일 `h1` 이 모범 사례로 꼽힌다.
```

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="WNVgKaP" data-pen-title="text - element" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/WNVgKaP">
  text - element</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
 
### 본문 - P

html `<p>` 요소는 하나의 문단을 나타낸다. 문단은 블록 레벨 요소이며, 자신의 닫는 태그 `</p>` 이전에 다른 블록 레벨 태그가 분석되면 자동으로 닫힌다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="wvVExQQ" data-pen-title="p" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/wvVExQQ">
  p</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 본문 - br

html `<br>` 요소는 텍스트 안에 줄바꿈(캐리지 리턴)을 생성한다. 주소나 시조 등 줄의 구분이 중요한 내용을 작성할 때 유용하다.

<br>

### 본문 - blockquote, q

html `<blockquote>` 요소는 안쪽의 텍스트가 긴 인용문임을 나타낸다. 주로 들여쓰기를 한 것으로 그려진다. 인용문의 출처 url은 `<cite>` 특성으로, 출처 텍스트는 `<cite>` 요소로 제공할 수 있다.



<br>

### 본문 - pre

html `<pre>` 요소는 미리 서식을 지정한 텍스트로 나타내며, html에 작성한 내용 그대로 표현한다. 텍스트는 보통 고정폭 글꼴을 사용해 렌더링하며, 요소 내 공백문자를 그대로 유지한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="xxvaJmR" data-pen-title="pre" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/xxvaJmR">
  pre</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 본문 - figure, figcaption

html `<figure>` 요소는 독립적인 콘텐츠를 표현한다. `<figcaption>` 요소를 사용해 설명을 붙일 수 있다. 피규어, 설명, 콘텐츠는 하나의 단위로 참조

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="ZEgMjwY" data-pen-title="figure" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ZEgMjwY">
  figure</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 본문 - hr

html `<hr>` 요소는 이야기 장면 전환, 구획 내 주제 변경 등, 문단 레벨 요소에서 주제의 분리를 나타낸다.

<br>

### 본문 - abbr, address, cite, bdo

html `<abbr>` 요소는 준말 또는 머리글자를 나타낸다. 선택 속성인 `<title>` 을 사용하면 준말의 전체 뜻이나 설명을 제공할 수 있다.   `<title>` 속성은 전체 설명만을 가져야 한다.

> 마우스 커서를 올렸을 때 나타나는 툴팁 확인

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="eYqLjop" data-pen-title="abbr" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/eYqLjop">
  abbr</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 본문 - b, strong

html `<b>` 요소는 독자의 주의를 요소의 콘텐츠로 끌기 위한 용도로 사용한다. 그 외의 다른 특별한 중요도는 주어지지 않는다. 그러나 `<b>` 를 사용해 텍스트를 꾸며선 안 된다. css를 사용해 굵은 글씨체를 적용하거나, `<strong>` 을 사용해 특별히 중요한 텍스트를 나타내는 것이 좋다.

> 둘 다 굵은 글씨인 것으로 눈으로 보여지는 것에는 다른 점을 찾기 힘들다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="GRVXBaG" data-pen-title="b, strong" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/GRVXBaG">
  b, strong</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 본문 - i, em

html `<i>` 요소는 텍스트에서 어떤 이유로 주위와 구분해야 하는 부분을 나타낸다. 기술용어, 외국어 구절, 등장인물의 생각 등을 예시로 들 수 있다. 보통 기울임꼴로 표시

`<em>` 요소 또한 텍스트의 강세를 나타낸다. 단순히 기울임 꼴이 필요해서 `<i>` `<em>` 사용해선 안 된다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="JjgaBgN" data-pen-title="i, em" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/JjgaBgN">
  i, em</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 본문 - mark, small, sub, sup


<br>

### 본문 - del, ins, code, kbd




<br>

### 본문 - a 태그와 하이퍼링크 1



<br>

### 본문 - a 태그와 하이퍼링크 2



<br>

### 본문 - 엔티티(Entity)
