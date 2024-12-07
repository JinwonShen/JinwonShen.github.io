---
layout: post
title: "(javascript/js) operator 연산자"
date: 2024-12-07 16:51:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - operator
  - arithmetic operator
  - logical operator
  - ternary operator
  - spread operator
discription:
---

# 연산자(operators)

## 산술 연산자(arithmetic operators)

산술 연산자는 사칙연산을 다루는 기본적이면서도 가장 많이 사용되는 연산자이다.

산술 연산자는 모두 두 개의 피연산자를 가지는 이항 연산자이며, 피연산자들의 결합 방향은 왼쪽에서 오른쪽이다.

<br>

## 할당연산자(assignment operators)

할당(`=`) 연산자는 변수에 값을 대입하는 데 사용된다. 할당 연산은 할당된 값으로 평가된다. 할당 연산자를 연결하여 사용하면 단일 값을 여러 변수에 할당할 수 있다.

<br>

```js
// 산술 연산자(arithmetic operators)

console.log(1 + 2);
console.log(5 - 7);
console.log(3 * 4);
console.log(10 / 2);
console.log(7 % 5);

console.log("=========");

// 할당 연산자(assignment operators)

let a = 3;
console.log(a);

// a = a + 2 (더하기 할당 연산자)

a += 2;
console.log(a);

// a = a - 2 (빼기 할당 연산자)
a -= 2;
console.log(a);

// a = a * 2 (곱하기 할당 연산자)

a *= 2;
console.log(a);

// a = a / 2 (나누기 할당 연산자)

a /= 2;
console.log(a);

// a = a % 2 (나머지 할당 연산자)

a %= 2;
console.log(a);

console.log("=========");

// 증감 연산자(Increment & Decrement operators)는 변수 1씩 더하거나 빼는 연산자

// ++ 기호가 뒤에 있는 경우,

let a2 = 3;
console.log(a2++);
console.log(a2);

// ++ 기호가 앞에 있는 경우,

let b = 3;
console.log(++b);
console.log(b);

// -- 기호가 뒤에 있는 경우,

let c = 3;
console.log(c--);
console.log(c);

// -- 기호가 앞에 있는 경우,

let d = 3;
console.log(--d);
console.log(d);

console.log("=======");

// 증감 연산자보다 할당 연산자를 사용하는 것을 추천한다.
let e = 3;
e += 1;
console.log(e);

e -= 1;
console.log(e);
```

<br>

## 부정 연산자(negation operators)란,

부정연산자(negation operators)란 참과 거짓의 반댓값을 불린 데이터로 반환한다.

<br>

## 비교 연산자(comparison operators)란,

비교 연산자(comparison operators)는 논리 문장에서 변수나 값의 동등성이나 차이를 판별하는 데 사용된다.

<br>

```js
console.log(!true); // false
console.log(!false); // true

console.log("중첩사용 =========");
console.log(!0); // true
console.log(!!0); // false
console.log(!!!0); // true
console.log(!!!!0); // false

console.log("거짓(falsy) ========");
console.log(!null); // true
console.log(!NaN); // true
console.log(!undefined); // true
console.log(!""); // true

console.log("참(truthy) ========");
console.log(!{}); // false
console.log(![]); // false
console.log(!"A"); // false

console.log("===================");

// 비교연산자(comparison operators)는 두 데이터를 비교할 때 사용된다.
const a = 1;
const b = 3;

// 동등(형 변환!) 피 연산자 끼리의 비교
console.log(a == b); // false

// 부등(형 변환!)
console.log(a != b); // true

// 일치
console.log(a === b); // false

// 불일치
console.log(a !== b); // true

// 큼
console.log(a > b); // false

// 크거나 같음
console.log(a >= b); // false

// 작음
console.log(a < b); // true

// 작거나 같음
console.log(a <= b); // true
```

<br>

## 논리 연산자(logical operators)란,

연산자에 '논리’라는 수식어가 붙긴 하지만 논리 연산자는 피연산자로 불린형뿐만 아니라 모든 타입의 값을 받을 수 있다. 연산 결과 역시 모든 타입이 될 수 있다.

<br>

```js
/// 그리고(AND) 연산자 &&
const a = true;
const b = false;

if (a && b) {
  console.log("참!"); // 출력x
}
console.log(a && b); // false

console.log("============");

/// 또는(OR) 연산자 ||

const c = true;
const d = false;

if (c || d) {
  console.log("참!"); // 출력됨
}
console.log(c || d); // true

console.log("============");

//// 그리고(AND) 연산자는 왼쪽에서부터 가장 먼저 만나는 거짓(Falsy) 데이터를 반환한다.
//// 끝까지 거짓이 없으면 가장 오른쪽의 마지막 참(Truthy) 데이터를 반환한다.
console.log(true && false); // false
console.log(1 && 0); // false
console.log(1 && 7 && 0); // 0
console.log(7 && 0 && 7); // 0
console.log(0 && 1 && 7); // 0
console.log("x" && {} && null); // null
console.log({} && "y" && []); // []

//// 또는(OR) 연산자는 왼쪽에서부터 가장 먼저 만나는 참(Truthy) 데이터를 반환한다.
//// 끝까지 참이 없으면 가장 오른쪽의 마지막 거짓(Falsy) 데이터를 반환한다.
console.log(false || true); // true
console.log(0 || 1); // 1
console.log(false || 0 || {}); // {}
console.log(false || "ab" || null); // ab
console.log(function () {} || undefined || ""); // f () {}
console.log("" || 0 || NaN || false); // false
```

<br>

## 삼항 연산자(ternary operator)

조건 (삼항) 연산자는 `JavaScript`에서 세 개의 피연산자를 받는 유일한 연산자아다. 앞에서부터 조건문, 물음표(`?`), 조건문이 참(`truthy`)일 경우 실행할 표현식, 콜론(`:`), 조건문이 거짓(`falsy`)일 경우 실행할 표현식이 배치된다. 해당 연산자는 `if...else`문의 대체재로 빈번히 사용된다.

<br>

```js
const fruits = ["apple", "banana", "cherry"];

// if 조건문
// fruits.length > 0 =
if (fruits.length) {
  console.log("과일이 있습니다.");
} else {
  console.log("과일이 없습니다.");
}

// 삼항 연산자
const message = fruits.length ? "과일이 있습니다." : "과일이 없습니다.";
console.log(message);

// 함수를 활용한
function includesText(el) {
  return el.textContent ? "글자 있음" : "글자 없습";
}

const h1El = document.querySelector("h1");
console.log(includesText(h1El));
```

<br>

## 전개 연산자(spread operator)

자기 자신을 포함해 대열 데이터의 대괄호를 삭제하는 역할을 한다.

```js
/// 배열 데이터
const numbers = [1, 2, 3];

console.log(numbers); // [1, 2, 3]
console.log(...numbers); // 1 2 3

const n1 = [1, 2, 3];
const n2 = [2, 3, 4];
const n3 = n1.concat(n2);
const n4 = [...n1, ...n2];

console.log(n3); // [1, 2, 3, 2, 3, 4]
console.log(n4); // [1, 2, 3, 2, 3, 4]

/// 객체 데이터
const o1 = { a: 1, b: 2, c: 3 };
const o2 = { b: 99, c: 100, d: 101 };
const o3 = Object.assign({}, o1, o2);
// {} 괄호안에 o1, o2를 복사해 넣는 것인데 중복되는 속성 이름이 있다면 마지막에 작성한 속성이 덮어씌운다.
const o4 = { ...o1, ...o2 };
// 전개 연산자를 활용해 ...자신과 o1과 o2를 감싸고있는 중괄호를 삭제한다.

console.log(o3); // { a: 1, b: 99, c: 100, d: 101 }
console.log(o4); // { a: 1, b: 99, c: 100, d: 101 }
```

<br>
