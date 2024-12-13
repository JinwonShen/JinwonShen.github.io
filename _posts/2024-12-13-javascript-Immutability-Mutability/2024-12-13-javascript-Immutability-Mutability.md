---
layout: post
title: "(javascript/js) 가변성(Immutability)과 불변성(Mutability)"
date: 2024-12-13 15:53:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Immutability
  - Mutability
discription:
---

## 불변성(Mutability)

생성된 데이터가 메모리에서 변경되지 않는 것을 의미한다.

- 원시형(문자, 숫자, 불린, null, undefined)은 불변성을 가지고있다.

<br>

## 가변성(Immutability)

생성된 데이터가 메모리에서 변경될 수 있음을 의미한다.

- 참조형(배열, 객체, 함수)은 가변성을 가지고 있다.

<br>

### 간단한 예시

```js
const user = {
  name: "Neo",
  age: 85,
  emails: ["neo@heropy.dev", "bosv031999@gmail.com", "bosv031999s@naver.com"],
};

console.log(user);

let { name, age, emails } = user;
name = "Evan";
age = 123;
emails = [...emails]; // 얕은 복사 !!
emails.splice(1, 2);

console.log(name, age, emails);
console.log(user);
```

<br>
