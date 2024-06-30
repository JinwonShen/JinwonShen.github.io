---
layout: post
title:  "Javascript/Array 배열"
date:   2024-06-02 23:05 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - array
  - 배열
---

## array(배열)

array(배열)는 동일한 데이터 타입의 변수들이 메모리에 연속해서 할당된 구조

<br>

### 배열의 특징

- 인덱스(index)를 통해 배열 요소에 접근할 수 있다.
- 고정된 크기를 가지며, 크기를 변경할 수 있다.
- 동일한 데이터 타입의 요소를 가지고 있다.
- 메모리의 연속된 위치에 할당된다.

### 간단 예제

```javascript
const users = ["june","mike","chulsoo","sumin"];
console.log(users)

// console
(4) ['june', 'mike', 'chulsoo', 'sumin']
```

<br>

### 원하는 위치의 인덱스 번호 출력하기

```javascript
console.log(users[2])

// console
chulsoo
```

<br>

### 마지막 인덱스 번호를 출력하려면

```javascript
console.log(users.length - 1)

// console
3
```

<br>

### 배열의 가장 마지막에 추가

```javascript
users.push("soo")

console.log(users)

// console
(5) ['june', 'mike', 'chulsoo', 'sumin', 'soo']
```

<br>

### 배열의 가장 앞에 추가

```javascript
users.unshift("jinwon")

console.log(users)

// console
(6) ['jinwon', 'june', 'mike', 'chulsoo', 'sumin', 'soo']
```

<br>

### 배열의 마지막 데이터 삭제

```javascript
users.pop()

console.log(users)

// console
(3) ['june', 'mike', 'chulsoo']
```

<br>

### chulsoo의 인덱스를 구하는 법

```javascript
console.log(users.indexOf("chulsoo"))

// console
2
```

<br>

### 인덱스 교체하기

```javascript
users[users.indexOf("mike")] = "michael"  

console.log(users)

// console
(4) ['june', 'michael', 'chulsoo', 'sumin']
```

<br>

### 변수가 배열인지 아닌지 알려주는

```javascript
console.log(Array.isArray(users))

// console
true
```

<br>

### 특정 위치의 데이터 삭제

```javascript
users.splice(2, 1); //인덱스번호 2부터 1개 삭제

console.log(users)

// console

(3) ['june', 'mike', 'sumin']
```

<br>

<!-- ## 한줄평  -->

_"이렇게 간단히 변수와 배열에 대해 알아보았는데, 물론 이 페이지에서 다루지 않겠지만 앞으로 프로젝트를 하며 계속 보완해 나가야 할 것 같다."_






























