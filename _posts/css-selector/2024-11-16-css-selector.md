---
layout: post
title:  "(css) Selector(선택자)"
date:   2024-11-16 13:38:00 +09:00
categories: notice
usemathjax: true
tag:
  - css
  - selector
  - type
  - class
  - id
  - attribute selector
  - pseudo-class selector

discription: 
---

# css Selector(선택자)

css에서, 선택자는 스타일을 지정할 웹 페이지의 html요소를 대상으로 하는 데 사용된다. 사용 가능한 다양한 css 선택자가 있으며, 스타일을 지정할 요소를 선택할 때 세밀한 정밀도를 허용한다.

## 선택자란 무엇인가 ?

css 선택자는 css 규칙의 첫 번째 부분이다. 선택자는 규칙 내부의 css 속성 값을 적용하기 위해 어떤 html 요소를 선택해야 하는지 브라우저에서 알려주는 요소 및 기타 용어의 패턴이다. 선택자에 의해 선택되는 요소를 선택자의 대상이라고 한다.

```css
h1 {
  color: blue;
  background-color: yellow;
}

p {
  color: red;
}
```

<br>

## 선택자 목록

동일한 css를 사용하는 항목이 두 개 이상인 경우 개별 선택자를 선택자 목록으로 결합해 규칙이 모든 개별 선택자에 적용되도록 할 수 있다. 예를 들어 `h1`에 동일한 css와 `.special` 클래스가 들어있는 경우 이를 두 개의 개별 규칙으로 작성할 수 있다.

```css
h1 {
  color: blue;
}

.special {
  color: blue;
}
```

또한 이들 사이에 쉼표를 추가해 선택자 목록으로 결합할 수도 있다.

```css
h1, .special {
  color: blue;
}
```

쉼표 앞이나 뒤에 공백을 사용할 수 있다. 선택자를 새 줄에 배치하면 가독성을 높일 수 있다.

```css
h1,
.special {
  color: blue;
}
```

<br>

## 선택자의 유형

선택자에는 몇 가지 다른 그룹이 있으며, 어떤 유형의 선택자가 필요한지 알면 작업에 적합한 도구를 찾는 데 도움이 된다.

### 유형, 클래스 및 ID선택자

```css
/* 요소 선택자 */
h1 {

}

/* 클래스 선택자 */
.box {

}

/* ID 선택자 */
#unique {

}

/* 범용 선택자 */
* {

}
```

<br>

**✅ 동일한 문서에서 ID를 여러 번 사용하면 스타일을 지정하기 위해 작동하는 것 처럼 보일 수 있지만, 이렇게 하면 안된다. 이로 인해 잘못된 코드가 생성되고 여러 곳에서 이상한 동작이 발생할 수 있다.**

## attribute Selector(속성 선택자)

html에 대한 연구에서 알 수 있듯이, 요소에는 마크업되는 요소에 대한 정보를 제공하는 속성이 있을 수 있다. css에서는 속성 선택자를 사용해 특정 속성이 있는 요소를 대상으로 지정할 수 있다.

### 존재 및 값 선택자

속성의 존재여부(예: `href`) 또는 속성 값에 대한 다양한 일치 항목을 기준으로 요소를 선택할 수 있다.

<br>

| 선택자                | 예시                               |    설명    |
| :------------------ | :-------------------------------- | :-------: |
| [attr] | a[title] | attr 속성이 있는 요소와 일치한다.(이름은 대괄호 안의 값.) |
| [attr=value] | a[href="https://example.com"] | 값이 정확히 value(따옴표 안의 문자열)인 attr속성이 있는 요소와 일치한다. |
| [attr~=value] | p[class~="special"] | 값이 정확히 value이거나 (공백으로 분류된) 값 목록에 value가 포함된 attr 속성이 있는 요소와 일치한다. |
| [attr\|=value] | div[lang\|="zh"] | 값이 정확히 value이거나 바로 뒤에 하이픈이 오는 value로 시작하는 attr 속성이 있는 요소와 일치한다. |

아래 예에서 이러한 선택자가 사용되는 것을 볼 수 있다.

<br>

- `li[class]`를 사용하여 클래스 속성이 있는 모든 목록 항목을 일치시킬 수 있다. 이 것은 첫 번째 항목을 제외한 모든 목록 항목과 일치한다.
- `li[class="a"]`는 클래스가 `a`인 선택자와 일치하지만 값의 일부로 공백으로 구분된 다른 클래스가 있는 `a`클래스가 있는 선택자는 일치하지 않는다. 두 번쨰 목록 항목을 선택한다.
- `il[class~="a"]`는 `a`클래스와 일치하지만 공백으로 구분된 목록의 일부로 `a`클래스를 포함하는 값과도 일치한다. 두 번째 및 세 번째 목록 항목을 선택한다.

<br>

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="oNKOzZK" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/oNKOzZK">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 하위 문자열 일치 선택자

이러한 선택자는 속성 값 내에서 하위 문자열의 고급 일치를 허용한다. 예를 들어 `box-warning` alc `box-error` 클래스가 있고 문자열 "box-x"로 시작하는 모든 항목을 일치시키려는 경우, `[class^="box-"]` 를 사용해 둘 다 선택할 수 있다. (또는 위 섹션에서 설명한 `class\|="box"`).

| 선택자                | 예시                               |    설명    |
| :------------------ | :-------------------------------- | :-------: |
| [attr^=value] | li[class^="box-"] | 값이 value로 시작하는 attr 속성이 있는 요소와 일치한다. |
| [attr$=value] | li[class$="-box"] | 값이 value로 끝나는 attr 속성이 있는 요소와 일치한다. |
| [attr*=value] | li[class*="box"] | 값이 문자열 내에서 value를 포함하는 attr 속성이 있는 요소와 일치한다. |

**(참고:`^`및 `$`는 소위 정규식에서 각각 시작 및 종료를 의미하는 닻으로 오랫동안 사용되어 왔다는 점에 유의하는 것이 도움이 될 수 있다.)**

- `li[class^="a"]`는 `a`로 시작하는 모든 속성값과 일치하므로 처음 두 목록 항목과 일치한다.
- `li[class$="a"]`는 `a`로 끝나는 모든 속성값과 일치하므로 첫 번째 및 세 번쨰 목록 항목과 일치한다.
- `li[class*="a"]`는 문자열에서 `a`가 나타나는 모든 속성 값과 일치하므로 모든 목록 항목과 일치한다.

<br>

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="OJKGRjW" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/OJKGRjW">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## Pseudo-class Selector(가상 클래스 선택자 혹은 의사 클래스 선택자)

가상 클래스 선택자 혹은 의사 클래스 및 의사 요소라고 하는 선택자로 여러 개가 있으며, 종종 매우 특정한 목적을 위해 사용된다. 사용 방법을 알게 되면 목록을 보고 달성하려는 작업에 적합한 것이 있는지 확인할 수 있다.


### 가상 클래스, 의사 클래스란 ?

가상/의사 클래스는 특정 상태에 있는 요소를 선택하는 선택자로 해당 유형의 첫 번째 요소이거나 마우스 포인터로 가리키고 있다. 그 것들은 마치 문서의 일부에 클래스를 적용한 것처럼 행동하는 경향이 있고, 종종 마크업에서도 과도한 클래스를 줄이는 데 도움이 되거나, 더 유연하고 유지관리 가능한 코드를 만들 수 있다.

가상/의사 클래스는 클론으로 시작하는 키워드. 예를 들어, `:hover`는 의사 클래스이다.

<br>

- 간단한 가상/의사 클래스

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="VwoNKrY" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/VwoNKrY">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

모든 가상/의사 클래스는 이와 같은 방식으로 작동한다. html에 클래스를 추가한 것처럼 동작해 특정 상태에 있는 문서의 일부를 대상으로 한다. mdn의 다른 예로는

- `:last-child`
- `:only-child`
- `:invalid`

<br>

### 사용자-행동 유사 클래스

일부 가상/의사 클래스는 사용자가 어떤 방식으로든 문서와 상호 작용할 때만 적용된다. 동적 가상/의사 클래스라고도 하는 이러한 사용자 행동 가상/의사 클래스는 사용자가 요소와 상호 작용할 때 클래스가 요소에 추가된 것처럼 작동한다.

- `:hover` - 위에서 언급한 내용; 이는 사용자가 요소(일반적으로 링크) 위로 포인터를 이동하는 경우에만 적용된다.
- `:focus` - 사용자가 클릭하거나 키보드 컨트롤을 사용하여 요소에 초점을 맞춘 경우에만 적용된다.

<br>

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="NWQmRYa" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NWQmRYa">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


### 가상/의사-요소란 ?

가상/의사 요소는 유사항 방식으로 동작하는데, 기존 요소에 클래스를 적용하는 것이 아니라 완전히 새로운 html요소를 마크업에 추가한 것처럼 작동한다.

의사 요소는 이중 클론 `::`으로 시작한다. `::before`는 의사 요소의 예 이다.

<br>

- 가상/의사 요소

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="NWQmRMw" data-pen-title="가상/의사 요소" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NWQmRMw">
  가상/의사 요소</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 결합자

결합자란 다른 선택자를 서로 유용한 관계와 문서의 콘텐츠 위치를 제공하는 방식으로 결합하는 선택자

### 후손 결합자

일반적으로 단일 공백(" ") 문자로 표시된다. 첫 번째 선택자와 일치하는 조상(부모, 부모의 부모, 부모의 부모의 부모 등) 요소가 있는 경우 두 번째 선택자와 일치하는 요소가 선택되도록 두 선택자를 결합한다. 후손 결합자를 활용하는 선택자를 하위 선택자라고 한다.

아래 예에서는, `.box` 클래스가 있는 요소 내부에 있는 `<p>` 요소만 일치시킨다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="QWePKxQ" data-pen-title="후손 결합자" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/QWePKxQ">
  후손 결합자</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 자식 결합자

자식 결합자(`>`)는 두 CSS 선택자 사이에 배치된다. 첫 번째와 일치하는 요소의 직계 자식인 두 번째 선택자와 일치하는 요소만 일치한다. 계층 구조에서 더 아래에 있는 하위 요소는 일치하지 않는다. 예를 들어, `<article>` 요소의 직계 자식인 `<p>` 요소만 선택하려면 다음을 수행.

다음 예제에서는, 정렬되지 않은 목록이 있으며, 내부에 정렬된 목록이 중첩되어 있다. 자식 결합자는 `<ul>`의 직계 자식 `<li>`요소만 선택하고 위쪽 테두리로 스타일을 지정한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="KKOYgBR" data-pen-title="자식 결합자" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/KKOYgBR">
  자식 결합자</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 인접 형제 결합자

인접한 형제 결합자(`+`)는 두 css 선택자 사이에 배치된다. 첫 번쨰 선택자의 다음 형제 요소인 두 번째 선택자와 일치하는 요소만 일치한다. 예를 들어 `<p>` 요소 바로 앞에 있는 모든 `<img>` 요소를 선택하려면 다음을 수행

아래 예와 같이 제목 뒤에 오는 단락으로 작업을 수행. 예에서 우리는 부모 요소를 `<h1>`과 공유하고 `<h1>` 바로 다음에 오는 모든 단락을 찾는다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="wvVZzEr" data-pen-title="인접 형제 결합자" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/wvVZzEr">
  인접 형제 결합자</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 일반 형제 결합자

요소의 형제 요소가 바로 인접하지 않더라도 선택하려면 일반 형제 연결자 (`~`)를 사용할 수 있다. `<p>` 요소 다음에 오는 모든 `<img>` 요소를 선택하려면 다음을 수행

아래 예에서는 `<h1>`뒤에 오는 모든 `<p>`요소를 선택하며 문서에도 `<div>`가 있지만 그 뒤에 오는 `<p>`가 선택된다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="zYgXKJX" data-pen-title="일반 형제 결합자" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/zYgXKJX">
  일반 형제 결합자</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 계단식 및 상속

css가 html에 적용되는 방법과 충돌을 해결하는 방법을 제어하는 css의 가장 기본적인 개념인 계단식, 우선 순위 및 상속에 대한 이해

### 규칙 충돌

css는 Cascading Style Sheet의 약자로, css라는 단어를 이해하는 데 있어 첫 번째 단어 cascading은 매우 중요하다.

일반적으로 문제는 동일한 요소에 적용할 수 있는 두 가지 규칙을 작성했을 때 나타나는데, 계단식(cascading)과 밀접하게 관련된 우선순위(specificity) 개념은 그런 충돌이 있을 때 적용되는 규칙을 제어하는 메커니즘이다. 

<b>상속</b>의 개념도 중요한데, 기본적으로 일부 css속성은 현재 요소의 부모 요소에 설정된 값을 상속하지만, 일부는 그렇지 않다. 

### 계단식(cascade)

스타일 시트 cascade 매우 간단한 수준에서는 이는 css 규칙의 순서가 중요하다는 것을 의미한다. 동일한 우선순위를 갖는 두 규칙이 적용될 때, css에서는 마지막에 오는 규칙이 사용된다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="poMBEQZ" data-pen-title="cascade" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/poMBEQZ">
  cascade</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 우선 순위(specificity)

우선 순위는 여러 규칙에 다른 선택자가 있지만, 여전히 동일한 요소에 적용될 수 있는 경우, 브라우저가 어떤 규칙을 적용할지 결정하는 방법.

- 요소(type)선택자 : 페이지에 나타내는 모든 유형의 모든 요소를 선택(우선순위 낮음)
- class선택자 : 특정 `class`속성 값이 있는 페이지의 요소만 선택(우선순위 높음)

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="NWQmRey" data-pen-title="specificity" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NWQmRey">
  specificity</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### 상속(Inheritance)

부모 요소에서 설정된 일부 css 속성 값은 자식 요소에 의해 상속되며, 일부는 그렇지 않다.

<br>

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="xxveEMK" data-pen-title="inheritance" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/xxveEMK">
  inheritance</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

#### 상속 제어하기

css는 상속을 제어하기 위한 4가지 특수 범용 속성 값을 제공. 모든 css 속성은 이러한 값을 허용한다.

`inherit` - 선택한 요소에 적용된 속성 값을 부모 요소의 속성 값과 동일하게 설정한다. (상속에 영향을 미침)

`initial` - 선택한 요소에 적용된 속성 값을 브라우저의 기본 스타일 시트에서 해당 요소의 해당 속성에 설정된 값과 동일하게 설정한다. 브라우저의 기본 스타일 시트에서 값을 설정하지 않고 속성이 자연스럽게 상속되면 속성 값이 대신 `inherit` 되도록 설정

`unset` - 속성을 nature 값으로 재설정한다. 즉, 속성이 자연적으로 상속되면 `inherit`된 것처럼 작동하고 그렇지 않으면 `initial` 처럼 작동한다.

<br>

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="abexmxo" data-pen-title="상속 제어하기" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/abexmxo">
  상속 제어하기</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>