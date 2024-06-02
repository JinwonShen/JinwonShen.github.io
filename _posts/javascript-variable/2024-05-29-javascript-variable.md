---
layout: post
title:  "Javascript/변수와 데이터 타입"
date:   2024-06-02 21:32 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - 변수
---

## Javascript

- 인터프리터 (컴파일x)
- java !== javascript
- ECMA Script로 규격화
- 멀티패러다임 (함수, 객체지향)
- 클라이언트 => 확장

<br>

### console 명령어

console.log("hello") <br>
console.warn("hello") <br>
console.error("hello") <br>
console.time() <br>
console.timeEnd() <br>
console.log(console) <br>

> console.log 이외에도 다양한 console 명령어가 있다.


### 변수

`var` `let` `const`

#### var

현재는 사용하지 않음. let과 const라는 var의 방식을 완벽히 대체하기 때문이다.

#### let

- 한번 정의하고 다시 변경이 가능

```js
let Name = "jinwon";
Name = "Shenjinwon";

console.log(Name);
```

<br>

#### const

- 변하지 않는 변수를 선언할 때 const를 선언한다.

```js
const Name = "jinwon";
Name = "Shenjinwon";

console.log(Name);

//아래오류
main.js:4 Uncaught TypeError: Assignment to constant variable.
at main.js:4:6
```

<br>

#### String, Number, boolean, null, undefined

```js
const name = "june lee"; // string
const age = 35; // number
const weight = 86.3; // number
const isMale = true; // boolean
const money = null; // null 선언은 되었지만 빈 값일때
const girlFriend = undefined; // undefined 선언자체가 안된 것

let boyFriend ; // undefined
```


