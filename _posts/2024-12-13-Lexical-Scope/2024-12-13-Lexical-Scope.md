---
layout: post
title: "(javascript/js) 렉시컬 스코프(Lexical Scope)"
date: 2024-12-13 17:09:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Lexical Scope
  - Static Scope
discription:
---

## 렉시컬 스코프(Lexical Scope)

`렉시컬 스코프(Lexical Scope)`는 `정적 스코프(Static Scope)`라고도 하며, 함수를 선언한 위치에서 유효하게 접근 가능한 유효 범위를 말한다.

### 간단한 예시

```js
const a = {
  fnA() {
    // 자신이 포함되어있는 상위 범위
    console.log("fnA", this);
    const b = {
      fnB() {
        // 화살표함수는 렉시컬 범위로 최상위 fnA
        console.log("fnB", this);
        const c = {
          fnC: () => {
            console.log("fnC", this); // 화살표함수는 렉시컬 범위로 최상위 fnA
            console.log("a", a);
            console.log("b", b);
            console.log("c", c);
            // console.log("x", x);
          },
        };
        return c;
      },
    };
    return b;
  },
  fnX() {
    // 자신이 포함되어있는 상위 범위
    console.log("fnX", this);
    const x = {
      fnY() {
        console.log("fnY", this);
        console.log("a", a);
        console.log("b", b);
        console.log("x", x);
      },
    };
  },
};
a.fnA().fnB().fnC();
a.fnX();
```

<br>

- 렉시컬 스코프라는 것이 this 라는 키워드와 직접적인 관련이 있는 것은 아니지만 이해를 돕기 위해 사용
- 렉시컬 스코프는 함수가 정의된 위치에서의 상위 범위를 의미한다.

<br>

### 클로저(Closure)

함수가 선언될 때의 렉시컬 스코프를 기억하고 있다가, 함수가 호출될 때 그 스코프에 접근할 수 있는 개념(특성)을 말한다.

- 변수와 함수를 독립적으로 만들어서 동작시키는 것이 아니고
- 하나의 함수로 만들어 효율적으로 관리하기위한 목적

### 간단한 예시

```js
let count1 = 0;
function c1() {
  return (count1 += 1);
}
console.log(c1());
console.log(c1());
console.log(c1());

let count2 = 77;
function c2() {
  return (count2 += 1);
}

console.log(c2());
console.log(c2());
console.log(c2());

function createCount(count) {
  return function () {
    return (count += 1);
  };
}

const c3 = createCount(0);
console.log(c3());
console.log(c3());
console.log(c3());

const c4 = createCount(77);
console.log(c4());
console.log(c4());
console.log(c4());
```

<br>

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ZYzBbrg" data-pen-title="js/클로저(closure)" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ZYzBbrg">
  js/클로저(closure)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
