---
layout: post
title: "(javascript/js) JSON(JavaScriptp Object Notation)"
date: 2024-12-08 20:19:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - JSON
  - JavaScript Object Notation
discription:
---

## JSON(JavaScript Object Notaion)

`JSON(JavaScript Object Notaion)` 은 데이터 전달을 위한 표준 데이터 포맷이다.

- 문자, 숫자, 불린, Null, 객체, 배열만 사용
- 문자는 큰 따옴표만 사용
- 후행 쉼표 사용 불가
- `.json` 확장자 파일 사용 가능

### 구문 참고

```js
// js
const user = {
  name: "Neo",
  age: 85,
  isValid: true,
  emails: ["neo@hepory.dev", "bosv031999@gmail.com"], // 후행 쉼표
};
```

<br>

```json
// json
{
  "name": "Neo",
  "age": 85,
  "isValid": true,
  "emails": ["neo@hepory.dev", "bosv031999@gmail.com"]
}
```

- json으로 같은 객페 데이터를 만들 때 위와 같이 만들 수 있다.
- test.json 파일은 하나의 객체를 가지고 있다. 라고 판단하면 된다. ex)test.json
- undefined, function 함수는 json에서 지원하지 않는다.

<br>

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="PwYNadQ" data-pen-title="js/JSON" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/PwYNadQ">
  js/JSON</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
