---
layout: post
title: "(html) 임베디드 요소"
date: 2024-11-07 23:31:00 +09:00
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

```
참고 : 이미지가 로드되기 전에 브라우저에서 이미지의 종횡비를 계산할 수 있도록 포함하고 `height`와 `width`를 활성화한다. 이 종횡비는 이미지를 표시하는 데 필요한 공간을 예약하는 데 사용되며, 이미지를 다운로드해 화면에 그릴 떄 레이아웃 이동을 줄이거나 방지한다.
```

<br>

#### 웹에서 사용되는 일반적인 이미지 파일 형식

- `APNG` - 손실없는 애니메이션 시퀀스에 적합함 <br>
- `AVIF` - 성능이 뛰어나 이미지와 애니메이션 모두에 적합함 <br>
- `GIF` - 간단한 이미지와 애니메이션에 적합함 <br>
- `JPEG` - 정지 이미지의 손실 압축에 적합함 <br>
- `PNG` - 정지 이미지의 손실 없는 압축에 좋은 선택 <br>
- `SVG` - 벡터 이미지 형식 <br>
- `WebP` - 이미지와 애니메이션 이미지 모두에 적함함 <br>

PNG, JPEG, GIF보다 정지 이미지와 애니메이션 이미지 모두에서 WebP 및 AVIF와 같은 형식이 훨씬 더 뛰어난 성능을 제공해 권장한다.<br>
svg는 다양한 크기로 정확하게 그려야 하는 이미지의 경우 여전히 권장되는 형식이다.

<br>

#### srcset

사용자 에이전트가 사용할 수 있는 이미지 소스를 나타내는 쉼표로 구분된 하나 이상의 문자열

1. 이미지에 대한 url
2. 선택적으로 공백 뒤 하나를 붙일 수 있다.
   - 너비 설명자(바로 뒤에오는 양의 정수 w). 너비 설명자는 속성에 주어진 소스 크기로 나누어 `sizes` 속성을 통해 효과적인 밀도를 계산
   - 픽셀 밀도 설명자 (바로 뒤에 오는 양으 ㅣ부동 소수점 숫자 `x`).

설명자가 지정되지 않으면 소스에 기본 설명자가 할당 `1x`.

`srcset` 속성이 너비 설명자를 사용하는 경우 `sizes` 속성도 반드시 존재해야 하며, 그렇지 않으면 속성 `srcset`자체가 무시된다.

<br>

#### sizes

쉼표로 구분된 하나 이상의 문자열로, 소스 크기 세트를 나타낸다.

1. 미디어 조건. 목록의 마지막 항목에서는 생략해야함
2. 소스 크기 값.

미디어 조건은 이미지의 속성이 아닌 뷰포트의 속성을 설명한다. 예를 들어, 뷰포트가 500px보다 높지 않으면 1000px 너비의 소스를 사용하도록 제안한다.`(max-height:500px) 1000px`

소스 크기값은 이미지의 의도된 표시 크기를 지정한다. 사용자 에이전트는 현재 크기를 사용해 `srcset` 해당 소스가 width(`w`) 설명자를 사용해 설명할 때 속성에서 제공하는 소스 중 하나를 선택한다. 선택된 소스는 이미지의 내재적 크기 css 스타일이 적용되지 않은 경우 이미지의 표시 크기에 영향을 미친다. `srcset` 속성이 없거나 width설명자가 있는 값이 없는 경우 `sizes`속성은 효과가 없다.

<br>

### video

html 요소 `video`는 비디오 재생을 지원하는 미디어 플레이어를 문서에 내장한다. 오디오 콘텐츠에도 사용할 수 있지만, `audio`요소보다 더 적절한 사용자 경험을 제공할 수 있다.

- 따라하기(확장자를 봐주세요.)

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="oNKQvGm" data-pen-title="img (srcset, sizes)" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/oNKQvGm">
  img (srcset, sizes)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

위의 예는 `<video>` 요소의 간단한 사용법을 보여준다. `<img>` 요소와 마찬가지로 속성 내부에 표시하려는 미디어 경로를 포함한다. `src` 속성값에 비디오 너비와 높이, 자동 재생 및 반복 여부, 브라우저의 기본 비디오 컨트롤 표시 등과 같은 정보를 지정하기 위해 다른 속성을 포함할 수 있다.

여는 태그와 닫는 태그 `<video></video>`태그 안의 내용은 해당 요소를 지원하지 않는 브라우저에서는 폴백으로 표시된다.

#### 속성

`autoplay` - 부울 속성으로 이 속성을 지정하면 데이터 로드를 완료하기 위해 멈추지 않고 가능한 한 빨리 비디오가 자동 재생을 시작한다.

> 참고 : 최신 브라우저는 오디오(또는 음소거가 되지 않은 오디오 트랙이 있는 비디오)의 자동 재생을 차단한다. 오디오를 자동으로 재생하는 사이트는 사용자에게 불쾌한 경험을 줄 수 있기 때문.

`controls` - 이 속성이 있으면 브라우저는 볼륨, 탐색, 재생 일시정지/다시시작을 포함해 사용자가 비디오 재생을 제어할 수 있는 컨트롤을 제공

`loop` - 부울 속성으로 이 속성을 지정하면 브라우저가 비디오 끝에 도달하면 자동으로 시작 부분으로 돌아감

`muted` - 비디오에 포함된 기본 오디오 음소거 설정을 나타내는 부울 속성으로 설정된 경우 오디오는 처음에 음소거된다.

<br>

### audio

html `audio` 요소는 문서에 사운드 콘텐츠를 포함하는 데 사요오딘다. 속성 또는 요소를 사용해 표현되는 하나 이상의 오디오 소스를 포함할 수 있다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="KKOrPoq" data-pen-title="Untitled" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/KKOrPoq">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

### canvas

캔버스 스크립팅 API나 WebGL API와 함께 `<canvas>`요소를 사용해 그래픽과 애니메이션을 그린다.

#### 속성

`height` - css 픽셀 단위의 좌표 공간 높이. 기본값이 150px.

`weight` - css 픽셀 단위의 좌표 공간 너비. 기본값이 300px.

닫는 `</canvas>` 태그

`<img>` 요소와 달리 `<canvas>` 요소에는 닫는 태그`</canvas>` 가 필요하다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="abeQoKR" data-pen-title="canvas" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/abeQoKR">
  canvas</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

html - html 문서에 캐넙스 요소를 추가한다. 브라우저가 캔버스를 읽거나 렌더링할 수 없는 경우 대체 텍스트가 제공된다.

js - javascript 코드에서 다음을 호출해 `HTMLCanvasElement.getContext()` 그리기 컨텍스트를 가져오고 캔버스에 그리기를 시작한다.

<br>

### iframe

html `<iframe>` 요소는 중첩된 브라우징 컨텍스트를 나타내며 현재 페이지에 다른 html 페이지를 포함한다.

- 따라하기

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="NWQEKOd" data-pen-title="iframe" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/NWQEKOd">
  iframe</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
