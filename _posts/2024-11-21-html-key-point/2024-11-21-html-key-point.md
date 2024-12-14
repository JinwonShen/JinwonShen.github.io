---
layout: post
title: "(html) 핵심 html"
date: 2024-11-21 20:23:00 +09:00
lastmode: 2024-11-21 20:23:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - html
  - keypoint
discription:
---

# 핵심 html

## html 마크업 예시

```html
<div><p>마크업</p></div>
<!-- ex) <여는태그>마크업</닫는태그> -->

<img src="이미지 주소" width="300" height="100" />
<input type="text" placeholder="입력하세요" />
<!-- 콘텐츠가 태그에 포함되어 있는 경우에는, 닫는 태그가 없다. -->
```

<br>

<figure>
<img src="/assets/img/html-ranking.jpg" alt="html-ranking-img">
<figcaption>html elements ranking</figcaption>
</figure>

[출처 : Advanced WEB RAKING](https://www.advancedwebranking.com/seo/html-study)

<br>

## block vs inline

**block**

- 기본적으로 블록 레벨 요소는 <mark>부모 요소의 전체 공간을 차지</mark>하여 "블록"을 만든다.
- 브라우저는 보통 블록 레벨 요소의 앞과 뒤를 개행해서 그린다. 상자를 쌓는 것 처럼 생각할 수 있다.
- 블록 레벨 요소는 언제나 새로운 줄에서 시작하고, <mark>좌우 양쪽으로 최대한 늘어나 가능한 모든 너비를 차지</mark>한다.

**inline**

- 인라인 요소는 콘텐츠의 흐름을 끊지 않고, <mark>요소를 구성하는 태그에 할당된 공간만 차지</mark>한다.

<br>

## 시멘틱 마크업

**장점**

1. 검색 엔진 최적화(seo)
2. 접근성
3. 유지보수

<mark>시멘틱 htmt</mark>은 주어진 목적을 위해 요소를 사용하기 때문에 <mark>사람과 기계가 읽고 이해하기가 더 쉽다.</mark>

<br>

## html Emmet

마크업 개발의 속도를 붙여줄 치트키!

1. 자동완성 : `tab키` &ensp; 👉 &ensp; `div(tab키)`
2. 텍스트 : `{}` &ensp;👉&ensp; `div{안녕}`
3. 자식(하위)요소 : `>` &ensp;👉&ensp; `div>div `
4. 형제 요소 : `+` &ensp;👉&ensp; `div>p+a`
5. 올라가기 : `^` &ensp;👉&ensp; `div>p^div`
6. 반복하기 : `*` &ensp;👉&ensp; `ul>li*4`
7. 그룹화 : `()` &ensp;👉&ensp; `ul>(li>a)*4`
8. 클래스 : `.` &ensp;👉&ensp; `div.class-name`
9. 아이디 : `#` &ensp;👉&ensp; `div#id`
10. 속성 : `[attr]` &ensp;👉&ensp; `img[alt="이미지 설명"]`
11. 넘버링 : `$` &ensp;👉&ensp; `div.item$*6`

<br>

## html 학습 팁

<br>

1. 구글을 활용하면 못할 것이 없다.
2. 최대한 찾아보는 습관 가지기.
3. 검색은 영문이 유리하다.
   1. 영문 문서를 두려워하지 않기(번역기!)
4. 공식 문서나 튜토리얼 문서를 잘 확인하자
   1. [https://developer.mozilla.org/ko/docs/Web/HTML/Element](https://developer.mozilla.org/ko/docs/Web/HTML/Element)
   2. [출처 : https://www.w3schools.com/](https://www.w3schools.com/)
5. 배운 것을 기록해두자.

> html 학습 팁 // 구글 검색 시 `html input mdn` 과 같이 검색하면 공식문서에서 해당 태그를 바로 볼 수 있다.

<br>
