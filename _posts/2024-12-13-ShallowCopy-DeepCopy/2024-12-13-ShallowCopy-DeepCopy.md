---
layout: post
title: "(javascript/js) 얕은 복사(Shallow copy)와 깊은 복사(Deep copy)"
date: 2024-12-13 16:44:00 +09:00
lastmode: 2024-12-13 16:44:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Shallow copy
  - Deep copy
discription:
---

## 얖은 복사(Shallow copy)

참조형의 최상위 레벨만 복사하는 것을 말한다.

### 간단한 예시

```js
const c = { x: 1, y: 2 };
const d = Object.assign({}, c); // 정적 메소드를 통한 얕은 복사
// const d = { ...c }; // 얕은 복사
// 중괄호기호를 사용할 때마다 새로운 객체데이터가 만들어진다.
d.x = 99;
console.log(c);
console.log(d);

const e = [1, 2, 3];
// const f = e.slice(0); // 얕은 복사(직관적이지 않음)
const f = [...e]; // 얕은 복사
f[0] = 99;
console.log(e);
console.log(f);
```

<br>

## 깊은 복사(Deep copy)

참조형의 모든 레벨을 복사하는 것을 말한다.

### 간단한 예시

```js
const g = [
  { x: 1, y: 2 },
  { x: 3, y: 4 },
];
const h = _.cloneDeep(g); // 깊은 복사(성능적으로 좋은 영향은 주지 못해 꼭 필요한 곳에만 사용)
h[0].x = 99;
console.log(g);
console.log(h);
```

<br>

```js
const neo = {
  name: "Neo",
  age: 85,
};

const evan = {
  name: "evan",
  age: 22,
  parent: neo,
};

// const newEvan = { ...evan };
const newEvan = _.cloneDeep(evan);
newEvan.name = "Evan Yang";
newEvan.age = 11;
newEvan.parent.name = "Amy";

console.log(evan);
console.log(newEvan);
console.log(neo);
```

<br>
