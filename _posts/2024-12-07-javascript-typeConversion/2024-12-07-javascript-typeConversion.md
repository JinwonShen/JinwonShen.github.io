---
layout: post
title: "(javascript/js) 형변환(Type Conversion)"
date: 2024-12-07 15:26:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - 형변환
  - type conversion
  - 자료형
discription:
---

## 형변환(Type Conversion)이란,

데이터가 상황에 따라 적절한 데이터 타입(자료형)으로 변환되는 것을 말한다.

### 구문

```js
const a = 1;
const b = "1";

// == 동등 연산자 (부정확)
console.log("동등 연산자", a == b);

// === 일치 연산자 (정확)
console.log("일치 연산자", a === b);

// 다음 코드는 모두 true를 출력한다.
console.log("============");
console.log(123 == "123");
console.log(1 == true);
console.log(0 == false);
console.log(null == undefined);
console.log("" == false);

// 다음 코드는 모두 false를 출력한다.
console.log("============");
console.log(123 === "123");
console.log(1 === true);
console.log(0 === false);
console.log(null === undefined);
console.log("" === false);

//query = 검색, Selector = 선택자
const h1El = document.querySelector("h1");

// console.log(h1El.textContent);
// 연결된 html에 h1태그가 없다면 Error : Cannot read properties of null(textContent)

// null은 false와 같이 부정적인 의미를 가지고 있다.
if (h1El) {
  console.log(h1El.textContent);
}
```

- 따라하기

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="RNbaGRX" data-pen-title="js/type-conversion" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/RNbaGRX">
  js/type-conversion</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
