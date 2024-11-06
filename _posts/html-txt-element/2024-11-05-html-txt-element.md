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

#### 유의할 점

```
  - 글씨 크기를 위해 제목 태그를 사용해선 안 된다. 대신 css의 `font-size` 속성을 사용한다.

  - 제목 단계를 건너 뛰는 것을 피해야 한다. 언제나 `h1` 로 시작해서 `h2` , 순차적으로 기입한다.

  - 페이지 당 하나의 `h1` 을 사용한다. 여러 개를 사용해도 오류는 나지 않지만, 단일 `h1` 이 모범 사례로 꼽힌다.
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

html `<mark>` 요소는 현재 맥락에 관련이 깊거나 중요해 표시 또는 하이라이트한 부분을 나타낸다. `<small>` 요소는 덧붙이는 글이나, 저작권과 법률 표기 등의 작은 텍스트를 나타낸다. html `<sub>` 요소는 활자 배치를 아래 첨자로 해야 하는 인라인 텍스트를 지정한다. `<sup>` 태그는 `<sub>` 요소와 반대로 윗첨자(superscript) 텍스트를 표현할 때 사용한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="abeaQzo" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/abeaQzo">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 본문 - del, ins, code, kbd

html `<del>` 요소는 문서에서 제거된 텍스트의 범위를 나타낸다. 문서나 소스코드의 변경점 추적 등에 사용할 수 있다. `<ins>` 요소를 추가된 텍스트의 범위를 나타낼 수 있다. <br>
`<code>` 요소는 짧은 코드 조각을 나타내는 스타일을 사용해 자신의 콘텐츠를 표시한다. 기본 스타일은 사용자 에이전트의 고정 폭 글씨체.
`<kbd>` 요소는 키도브 입력, 음성 입력 등 임의의 장치를 사용한 사용자의 입력을 나타낸다. 관례에 따라 고정폭 글꼴로 표시하지만 강제는 아니다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="VwoGVLj" data-pen-title="del, ins, code, kbd" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/VwoGVLj">
  del, ins, code, kbd</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 본문 - a 태그와 하이퍼링크

html `<a>` 요소(앵커 요소)는 `<href>` 특성을 통해 다른 페이지나 같은 페이지의 어느 위치, 파일, 이메일 주소와 그 외 다른 url로 연결할 수 있는 하이퍼링크를 만든다. `<a>` 안의 콘텐츠는 링크 목적지의 설명을 나타내야 한다.

#### 유의할 점

href
- 하이퍼링크가 가리키는 url. 링크는 http기반 url일 필요는 없고, 브라우저가 지원하는 모든 url 스킴을 사용할 수 있다.

```
  - 페이지 구획을 가리키는 프래그먼트 url
  - 미디어 파일 일부를 가리키는 미디어 프래그먼트
  - tel : url을 사용하는 전화번호
  - mailto : url을 사용하는 이메일 주소
```

target
- 링크한 url을 표시할 위치. 가능한 값은 브라우징 맥락으로, 즉 탭, 창, iframe의 이름이나 특정 키워드이다. 다음 키워드는 특별한 뜻을 가지고 있다.

```
  _self : url을 현재 브라우징 맥락에 표시한다(기본값)
  _blank : url을 새로운 브라우징 맥락에 표시한다. 보통 새 탭이지만, 사용자가 브라우저 설정을 통해 새 창으로 바꿀 수 있다.
  _Parent : url을 현재 브라우징 맥락의 부모에 표시한다. 부모가 존재하지 않으면 _self와 동일하게 행동한다.
  - top : url을 최상단 브라우징 맥락(현재 맥락의 부모면서 자신의 부모가 존재하지 않는, 제일 높은 맥락)에 표시한다. 부모가 존재하지 않으면 _self와 동일하게 행동한다.
```

#### href 특정이 존재할 경우

가능한 ARIA 역할

`button`
`checkbox`
`menuitem`
`menuitemcheckbox`
`menuitemradio`
`option`
`radio`
`switch`
`tab`
`treeitem`

<br>

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="RwXYqVg" data-pen-title="a href" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/RwXYqVg">
  a href</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 본문 - 엔터티(Entity)

html 엔터티(Entity)는 앰퍼샌드(&)로 시작하고 세미콜론(;)으로 끝나는 텍스트 조각('문자열')이다. 엔터티는 예약된 문자(html 코드로 해석됨)와 보이지 않는 문자(예, 줄바꿈 없는 공백)를 표시하는데 자주 사용된다. 표준 키보드로 입력하기 어려운 다른 문자 대신 사용할 수 있다.


> 참고: 대부분의 문자는 기억할만한 엔터티를 가지고 있다. 예를 들어, 저작권 기호의 엔터티 (©)는 &copy; 이다. &#8212;나 &#x2014; 처럼 기억에 남지 않는 문자들은, 참조 차트 또는 디코더 도구를 사용할 수 있다.


이러한 문자들을 텍스트료 표시하려면, 아래 표시된 대로 해당 문자 엔터티로 변경해준다.

```
& : %amp; - 엔터티 또는 문자 참조의 시작으로 해석
< : &lt; - 태그의 시작으로 해석
> : &rt; - 태그의 끝으로 해석
" : &quot; - 특성 값의 시작과 끝으로 해석 
  : &nbsp; - 줄 바꿈 없는 공백으로 해석
– : &ndash; - 앤 대시(em단위 너비의 절반)로 해석
— : &mdash; - 앰 대시(em단위의 너비와 동일)로 해석
© : &copy; - 저작권 표시로 해석

... 
```