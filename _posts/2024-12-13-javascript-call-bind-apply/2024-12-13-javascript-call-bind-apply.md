---
layout: post
title: "(javascript/js) call, bind, apply"
date: 2024-12-13 10:44:00 +09:00
lastmode: 2024-12-13 10:44:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - .call()
  - .bind()
  - .apply()
discription:
---

## .call(), .apply(), .bind()

`.call(this, 인수1, 인수2...)` - 대상 함수를 주어진 객체(this)의 메소드로 실행한다.

`.apply(this, [인수1, 인수2, ...])` - 대상 함수를 주어진 객체(this)의 메소드로 실행한다.

`.bind(this)` - 대상 함수를 주어진 객체(this)의 메소드로 실행할 수 있는 새로운 함수를 반환한다.

### 간단한 예시

```js
const neo = {
  name: "Neo",
};

const amy = {
  name: "Amy",
  getInfo(age, city) {
    return `${this.name}는 ${age}세이고, ${city}에 삽니다.`;
  },
};
console.log(amy.getInfo(22, "서울"));

// call
console.log(amy.getInfo.call(neo, 85, "서울"));

// apply
console.log(amy.getInfo.apply(neo, [22, "대구"]));

// bind
const neoGetInfo = amy.getInfo.bind(neo);

setTimeout(() => {
  console.log(neoGetInfo(85, "서울"));
}, 1000);
```

<br>

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="KwPNPPW" data-pen-title="js/call(),apply(),bind()" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/KwPNPPW">
  js/call(),apply(),bind()</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
