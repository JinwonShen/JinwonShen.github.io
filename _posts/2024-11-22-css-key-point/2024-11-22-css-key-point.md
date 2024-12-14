---
layout: post
title: "(css) 핵심 css"
date: 2024-11-21 20:41:00 +09:00
lastmode: 2024-11-21 20:41:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - css
  - keypoint
discription:
---

# 핵심 css

## 핵심 css 표기 팁

- 스타일시트를 작성할 때마다 일정한 규칙을 가지고 작성하는 것이 중요하다.

```css
/* 레이아웃 */
box-sizing: border-box;
position: relative | absolute | fixed | sticky;
display: flex | block | inline-block | block;
/* 여백 */
margin: 100px;
padding: 100px;
/* 사이즈 및 bg */
width: 100px;
height: 100px;
border: 1px solid #000;
background: #fff;
/* 폰트 속성 */
font-size: 16px;
font-weight: 300 (thin) | 400 (normal) | 500 (medium) | 700 (bord);
color: #000;
text-align: center | left | right;
/* 등등등.. */
overflow: auto | scroll | hidden;
z-index: 1;
```

<br>

## overflow

`overflow` css 단축속성은 요소의 콘텐츠가 너무 커서 요소의 블록 서식 맥락에 맞출 수 없을 때의 처리법을 지정한다. 초과되는 컨텐츠에 대한 내용으로 적용 가능한 방법은 잘라내기, 스크롤바 노출, 넘친 콘텐츠 그대로 노출 등이 있다.

```css
overflow: visible;
  콘텐츠를 자르지 않으며 안쪽 여백 상자 밖에도 그릴 수 있다.
overflow: hidden;
  콘텐츠를 안쪽 여백 상자에 맞추기 위해 잘라낸다. 스크롤바를 제공하지 않는다.
overflow: scroll;
  콘텐츠를 안쪽 여백 상자에 맞추기 위해 잘라낸다. 항상 스크롤바를 노출하므로 내용의 변화에 따라 스크롤바가 생기거나 사라지지 않는다.
overflow: auto;
  사용자 에이전트가 결정한다. 콘텐츠가 안쪽 여백 상자에 들어간다면 `visible`과 동일하게 보이며, 데스크롭 브라우저의 경우 콘텐츠가 넘칠 때 스크롤바를 노출한다.
```

<br>

## 선택자

```
1. 기본 선택자
 - * (전체 선택자), div (요소(태그) 선택자), . (클래스 선택자), # (아이디 선택자), [attr] (속성 선택자)
2. 그룹 선택자
 - ","
3. 결합자
 - "공백"(자손 결합자), > (자식 결합자), ~ (일반 형제 결합자), + (인접형제 결합자)
4. 가상 클래스 선택자
 - :hover, :focus, :focus-visible, :active, :checked, :disabled, :not()
 - :first-cild, :last-child, :nth-child, :only-child
5. 가상 요소 선택자
 - ::before, ::after, ::placeholder
```

<br>

## css Emmet

[참고 docs.emmet.io](https://docs.emmet.io/cheat-sheet)

**많이 사용하는 Emmet**

- mt10 &ensp; 👉 &ensp; `margin-top: 10px;`
- pb10 &ensp; 👉 &ensp; `padding-bottom: 10px;`
- w100 &ensp; 👉 &ensp; `width: 100px;`
- h100p &ensp; 👉 &ensp; `height: 100%;`
- bd &ensp; 👉 &ensp; `border: 1px solid #000;`
- bgc &ensp; 👉 &ensp; `background-color: #fff;`
- fsz10 &ensp; 👉 &ensp; `font-size: 10px;`
- fw700 &ensp; 👉 &ensp; `font-weight: 700px;`
- c#ddd &ensp; 👉 &ensp; `color: #ddd;`
- z10 &ensp; 👉 &ensp; `z-index: 10;`

<br>

## css 학습 팁

1. html과 마찬가지로 구글을 적극적으로 활용하기.
2. 최대한 찾아보는 습관 가지기.
3. 검색은 영문이 유리하다.
   1. 영문 문서를 두려워하지 않기(번역기!)
4. 공식 문서나 튜토리얼 문서를 잘 확인하자
   1. [https://developer.mozilla.org/ko/docs/Web/HTML/Element](https://developer.mozilla.org/ko/docs/Web/HTML/Element)
   2. [출처 : https://www.w3schools.com/](https://www.w3schools.com/)
5. 배운 것을 기록해두자.

> 사실 html 학습 팁과 동일한데, 모든 문제는 구글 혹은 공식문서를 통하면 해결하지 못할 문제는 없는 것 같다.스스로 해결하는 능력 기르기 !

<br>
