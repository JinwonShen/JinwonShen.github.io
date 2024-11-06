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

<br>

- 따라하기



#### 사용 시 유의할 점 한눈에 보기
- 글씨 크기를 위해 제목 태그를 사용해선 안 된다. 대신 css의 `font-size` 속성을 사용한다.
- 제목 단계를 건너 뛰는 것을 피해야 한다. 언제나 `h1` 로 시작해서 `h2` , 순차적으로 기입한다.
- 페이지 당 하나의 `h1` 을 사용한다. 여러 개를 사용해도 오류는 나지 않지만, 단일 `h1` 이 모범 사례로 꼽힌다.

<br>
 
### 본문 - P

html `<p>` 요소는 하나의 문단을 나타낸다. 문단은 블록 레벨 요소이며, 자신의 닫는 태그 `</p>` 이전에 다른 블록 레벨 태그가 분석되면 자동으로 닫힌다.

<br>

- 따라하기



<br>

### 본문 - br

html `<br>` 요소는 텍스트 안에 줄바꿈(캐리지 리턴)을 생성한다. 주소나 시조 등 줄의 구분이 중요한 내용을 작성할 때 유용하다.

<br>

- 따라하기



<br>

### 본문 - blockquote, q

html `<blockquote>` 요소는 안쪽의 텍스트가 긴 인용문임을 나타낸다. 주로 들여쓰기를 한 것으로 그려진다. 인용문의 출처 url은 `<cite>` 특성으로, 출처 텍스트는 `<cite>` 요소로 제공할 수 있다.

<br>

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="ZEgMjYw" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ZEgMjYw">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 본문 - pre






<br>

### 본문 - figure, figcaption





<br>

### 본문 - hr





<br>

### 본문 - abbr, address, cite, bdo







<br>

### 본문 - b, strong




<br>

### 본문 - i, em






### 본문 - mark, small, sub, sup


### 본문 - del, ins, code, kbd


### 본문 - a 태그와 하이퍼링크 1


### 본문 - a 태그와 하이퍼링크 2


### 본문 - 엔티티(Entity)
