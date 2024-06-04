---
layout: post
title:  "Javascript/Object 객체"
date:   2024-06-04 22:25 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - object
  - 객체
---

## array(객체)

Object(객체)는 키(key)와 벨류(value)로 구성된 프로퍼티의 집합이다.

<br>

### 간단 예제

```javascript
const animal = {
  name: "monkey",
  weight: 10,
  food: ["banana","grape","nuts"],
  location: {
    country: "Kongo",
    home: "forest",
    isAfrica: true,
  },
}

console.log(animal)

// console
{name: 'monkey', weight: 10, food: Array(3), location: {…}}
```

<br>

### 배열에 접근하기

```javascript
console.log(animal.name)

// console
monkey


console.log(animal.location.country)

//console
Kongo
```

<br>

### JSON

> 서버로 데이터로 보내거나 받아올 때 http 통신을 할 때 데이터를 주고받는 어떠한 형태

```javascript
const animalJSON = JSON.stringify(animal) // json으로 변환
console.log(animalJSON) // 변환시킨 json을 출력

// console
{"name":"monkey","weight":10,"food":["banana","grape","nuts"],"location":{"country":"Kongo","home":"forest","isAfrica":true}}


// json으로 변환한 animal 배렬의 name에 접근
console.log(JSON.parse(animalJSON).name) 

// console
monkey
```