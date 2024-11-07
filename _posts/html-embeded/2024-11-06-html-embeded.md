---
layout: post
title:  "(html) 임베디드 요소"
date:   2024-11-06 23:31:00 +09:00
categories: notice
usemathjax: true
tag:
  - html
  - 임베디드(embeded)
  - img(src)
  - 이미지 유형
  - 반응형 이미지
  - video
  - audio
  - canvas, iframe
discription: 
---

# 임베디드(embeded) 요소

### img - src

html `<img>`요소는 문서에 이미지는 포함한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="bGXmONQ" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/bGXmONQ">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

위의 예는 `<img>` 요소의 사용법을 보여준다.
- 해당 `src`속성은 필수이고, 포함하려는 이미지의 경로를 포함한다.
- 속성 `alt`는 이미지에 대한 대체 텍스트를 보여주며, 필수적이고 접근성에 매우 유용하다. 화면 판독기는 속성 값을 사용자에게 읽어주어 이미지의 의미를 알 수 있도록 한다. 

<br>

> PNG, JPEG, GIF보다 정지 이미지와 애니메이션 이미지 모두에서 WebP 및 AVIF와 같은 형식이 훨씬 더 뛰어난 성능을 제공해 권장한다.<br>
svg는 다양한 크기로 정확하게 그려야 하는 이미지의 경우 여전히 권장되는 형식이다.


<br>