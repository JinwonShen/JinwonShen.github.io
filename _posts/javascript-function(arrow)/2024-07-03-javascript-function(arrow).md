---
layout: post
title:  "Javascript/조건문과 function(arrow)"
date:   2024-07-03 22:40:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - arrow
  - 조건문
---

## Javascript 조건문과 function(arrow) 알아보기

### if/else란

- if는 조건문을 이야기하는데

```javascript
const x = "10";

// == 와 === 의 차이점은 두 연산자 모두 비교한 피연산자 값이 일치하면 true 값을 반환하고 일치하지 않으면 fales 를 반환한다.
// === 는 더 엄격한 비교 연산자라고 보면 될 것 같다.
if (x === 10) {
    console.log("x is 10");
} else if (x === 20) {
    console.log("x is 20");
} else {
    console.log("x is string");
}

// console
x is string
```

### 삼항연산자 활용하기

- 조건 ? 참일경우 : 아닐경우 ; 로 활용이 가능한데 아래 예제를 보자

<br>

```javascript
const age = 20;

let group = "";

// 기존

// if(x > 20){
//     group = "senior"
// } else {
//     group = "junior"
// }

//삼항연산자를 활용했을 때 - 코드가 한결 가벼워짐

x > 20 ? group = "senior" : group = "junior";
console.log(group)

// console
junior
```

<br>

### swich case문 간단히 알아보기

```javascript
// 스위치(switch)

const animal = "apple";

switch(animal){
    case 'lion':
        console.log("big");
        break;
    case 'tiger':
        console.log("big");
        break;
    case 'monkey':
        console.log("medium");
        break;
    case 'dog':
        console.log("small");
        break;
    default:
        console.log("not animal")
        break;   
}

// console
not animal

```

<br>

### 기초적인 함수 실습으로 알아보기

- 자바스크립트에서 함수를 선언하는 가장 기본적인 형식

```javascript
// a=0, b=0 은 초기값을 설정하는
function add(a=0, b=0){
    return a + b;
}

console.log(add(5, 6))

// console
11
```

<br>

- 응용

```javascript
const sum = function(a, b){return a + b}

console.log(sum(5, 6))
```

<br>

- arrow function 이란?
- arrow function을 사용했을 때 가져올 수 있는 이점들이 있는데 코드가 간결해 진다는 것 이외에도, 함수가 윈도우 객체에 포함되지 않아 안정적이라고 할 수 있다. [아직 설명하기는 힘들 것 같다.]

```javascript
const sum = (a, b)=>{
    return a+b
}

console.log(sum(5, 6))

// console
11
```

_"간단하게 알아보았는데 개인 프로젝트를 진행하며 심도있게 알아보도록 하는 것이 좋을 것 같다."_