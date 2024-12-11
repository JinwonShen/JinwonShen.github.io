---
layout: post
title: "(javascript/js) string"
date: 2024-12-06 11:15:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - string
  - number
discription:
---

# JS 데이터 - 원시형

## string

`string` 전역 객체는 문자열(문자의 나열)의 생성자이다.

### 간단한 예시

```js
const s1 = "신진원"; // 문자데이터
const s2 = "아침"; // 문자데이터
```

<br>

- 문자 `String`은 따옴표를 사용한다.

```js
const s3 = `안녕하세요. ${s1}님, 좋은${s2} 입니다..`;
// 안녕하세요. 신진원님, 좋은아침 입니다..
```

<br>

- 템플릿 리터럴(Literal)은 백틱을 사용하며, ${} 안에 데이터를 보간(Interpolation)한다.
- 템플릿 리터럴(Literal) : 리터럴 중에서 데이터를 중간에 채워넣을 수 있는 보간법을 사용할 수 있는 리터럴 방식의 문자 데이터를 말한다.
- 리터럴(Literal) : 특정한 기호("", '', ``)로 만든 데이터

<br>

## number

`Number`는 `37`이나 `-9.25`와 같은 숫자를 표현하고 다룰 떄 사용하는 원시 래퍼 객체이다.

`Number` 생성자는 숫자를 다루기 위해 상수와 메소드를 가지고 있다. 다른 타입의 값은 `Number()` 함수를 사용해 숫자로 바꿀 수 있다.

### 간단한 예시

```js
// 숫자(number)는 정수 및 부동소수점 숫자(floating point number)를 나타낸다.
const nn1 = 123;
const nn2 = 12.345;

// 숫자가 아닌 숫자는 NaN(Not a Number)로 표시된다.
const n3 = 123 + "abc";
const n4 = 123 + undefined;

console.log(n3);
// 숫자와 문자를 더하면 문자가 우선이기 때문에 문자로 표기됨 = 123abc
console.log(n4);
// NaN (콘솔창에 숫자는 보라색으로 표기함)
```

<br>
