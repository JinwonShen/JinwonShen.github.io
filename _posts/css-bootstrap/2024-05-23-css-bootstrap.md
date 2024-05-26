---
layout: post
title:  "CSS/css 프레임워크 : 부트스트랩(bootstrap), 머터리얼라이즈(Materialize) 알아보기"
date:   2024-05-23 11:47:00 +09:00
categories: notice
usemathjax: true
tag:
  - css
  - framwork
  - bootstrap
---

## CSS 프레임워크 알아보기

### Bootstrap

<mark>*Bootstrap*</mark>은 css 프레임워크 라고 불리며 특정 클래스 명으로 스타일들이 다 지정이 되어있고, 그 클래스를 불러서 사용할 수 있는 프레임워크이다.

비슷한 css 프레임워크로는 <mark>*머터리얼라이즈 디자인*</mark> 구글에서 나온 안드로이드 어플리케이션에 들어가는 비슷한 형태의 css 프레임워크라고 할 수 있다.

<br>

> 5.0 이전 버전에서는 제이쿼리를 사용했으나 5 부터 순수 바닐라 자바스크립트로 라이브러리를 제공하고 있다.

<br>

#### CDN link

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
```

<br>

Bootstrap(부트스트랩)은 프로젝트를 진행하면서 검색하고 사용하고를 반복하는 과정을 거쳐야 할 것 같다. 

<br>

---

### Materialize

 <mark>*머터리얼라이즈 디자인*</mark>은 부트스트랩과 동일하게 css 프레임워크로 사용되며 Materialize 다운로드, Sass 다운로드를 통해 사용이 가능하며 당연히 CDN으로도 사용이 가능하다.

 그 외에도 NPM방식으로 사용하는 방법도 있음.

<br>

#### CDN link

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>

```

<br>

아이콘을 활용하기에 매우 유용하게 보이는데, 이 부분도 많이 사용해보는 것이 중요할 것 같다.

<br>

---

### 사이트 링크 참고
- [Bootstrap](https://getbootstrap.com/) <br>
- [Materialize](https://materializecss.com/getting-started.html/)