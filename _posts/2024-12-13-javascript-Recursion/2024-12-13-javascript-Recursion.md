---
layout: post
title: "(javascript/js) 동기 비동기"
date: 2024-12-13 10:44:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - 함수 재귀(Recursion)
discription:
---

## 함수 재귀(Recursion)

함수가 자기 자신을 호출하는 것을 말한다.

### 간단한 예시

```js
const neo = { name: "Neo" };
const evan = { name: "Evan", parent: neo };
const lewis = { name: "Lewis", parent: evan };
const amy = { name: "Amy", parent: lewis };

const getRootUser = (user) => {
  if (user.parent) {
    return getRootUser(user.parent); // 재귀 호출
  }
  return user;
};

console.log(getRootUser(lewis));
```

<br>

### 따라하기(클래스에서 재귀호출)

```js
class User {
  constructor(name, parent) {
    this.name = name;
    this.parent = parent;
  }
  static getRootUser(user) {
    if (user.parent) {
      return User.getRootUser(user.parent);
    }
    return user;
  }
}

const neo = new User("Neo");
const evan = new User("Evan", neo);
const lewis = new User("lewis", evan);
const amy = new User("Amy", lewis);

console.log(User.getRootUser(amy));
```
