---
layout: post
title: "(javascript/js) 모듈(Module)"
date: 2024-12-10 16:51:00 +09:00
lastmode: 2024-12-10 16:51:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - 모듈(Module)
  - import
  - export
discription:
---

# 모듈(Module) - import & export

작성할 수 있는 자바스크립트의 코드를 별도의 파일로 구분해 그 파일에서 데이터를 내보내거나 가지고 와서 사용하는 것

## 가져오기(import)

js파일 최상단에 위치해야 한다.

```js
import {} from "./module.js";
```

<br>

## 내보내기(export)

#### 기본 내보내기(Default export)

- 이름이 필요하지 않는다.
- 모듈에서 한 번만 사용할 수 있다.

```js
export default 데이터;
```

<br>

#### 이름 내보내기(Named export)

- 이름이 필수이다.
- 모듈에서 여러번 사용할 수 있다.

```js
export const 이름1 = 데이터1;
export const 이름2 = 데이터2;
export function 이름3() {}

// 변수나 함수, 클래스 앞 export를 하나씩 작성하지 않고,
// export 아래 문법을 통해 한 번에 내보내는 방법도 있다.
const a = 1;
const b = "Banana";
function c() {}
class D {} // 클래스는 파스칼케이스로 대문자로 작성한다.

// 객체 데이터가 아니고 export 데이터를 사용해 내보내기 위한 문법!!
export { a, b, c, D };
```

<br>

<br>

#### 기본 가져오기(Default import)

```js
// 기본 내보내기는 가지고 오면서 이름을 결정함 abc
import abc from "./module.js";
```

<br>

#### 이름 가져오기(Named import)

```js
// 이름 내보내기는 기존에 지정된 이름을 {} 중괄호로 입력해 가져온다.
import abc, { a, b, c, D } from "./module.js";
```

<br>

#### 모두 가져오기

```js
// * 는 와일드카드로 전체를 말한다. as abc 로 이름 변경해서 가지고 오기
import * as abc from "./module.js";
```

<br>

### index.html

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>JS Test</title>
  <!-- defer : 스크립트 지연 -->
  <script type="module" defer src="./main.js"></script>
  <script type="module" defer src="./sub.js"></script>
  <!-- 인덱스 파일에서 script 소스를 연결할 때 type="module" 속성을 반드시 지정해
  주어야한다. -->
</head>
```

<br>

### main.js

```js
import { add, sub } from "./core/calculator.js";
import { getUserBirthYear, neo, lewis } from "./core/user.js";
import { fruits, addFruits } from "./core/fruits.js";
// import { 내가 가지고올 함수나 배열 객체 등 } from "경로"

console.log(add(2, 7));
console.log(sub(2, 7));

console.log(getUserBirthYear(neo));
console.log(getUserBirthYear(lewis));

addFruits("Orange");
addFruits("Mango");
console.log(fruits);
```

<br>

### calculator.js

```js
// 내보낼 함수 앞에 export
export function add(a, b) {
  return a + b;
}

export function sub(a, b) {
  return a - b;
}
```

<br>

### sub.js

```js
// 새로 사용할 파일을 만들어도 index.html 에서 소스에 type="module" 작성해주고, 파일로 돌아와 import {} form "경로" 후 사용할 수 있다.
import { add } from "./core/calculator.js";

console.log(add(8, 7));
console.log(add(15, 22));
```

<br>
