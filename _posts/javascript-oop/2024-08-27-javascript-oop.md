---
layout: post
title:  "Javascript/oop(객체지향) 프로그래밍"
date:   2024-08-27 22:52 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - oop
  - 객체지향언어
---

## javascript oop(객체지향) 실습으로 알아보기


```js
// 1. 일반적인 함수 -> 생성자를 가진 함수로 만들기
// constructor function
function song(title, singer){
  // const title = "All I want is christmas";
  // const singer = "Mariah Carrey"; 아래형태로 실행
  this.title = title;
  this.singer = singer;
} 

const song1 = new Song();


// console
Song {title: undefined, singer: undefined}
singer: undefined
title: undefined
[[Prototype]]: Object

// 함수가 아닌 오브젝트가 반환된 것을 알 수 있음.
new 키워드를 사용해 this가 오브젝트를 가리키게 함(new 키워드없이 사용했을 때 window를 가리킴)

---

// 2.
const song1 = new Song("All I want is Christmas", "Mariah Carrey");

// console
Song {title: 'All I want is Christmas', singer: 'Mariah Carrey'}
singer: "Mariah Carrey"
title: "All I want is Christmas"
[[Prototype]]: Object

// 넘겨받은 값을 this 안에 넣어준다고 생각

---

// 3. 함수도 함께 할당하기
function Song(title, singer, year){
  this.title = title;
  this.singer = singer;
  this.year = year;
  this.getInfo = function(){
    return `이 곡의 제목은 ${this.title} 이고 가수는 ${this.singer} 입니다.`
  }
} 

const song1 = new Song("All I want is Christmas", "Mariah Carrey", 1995);

console.log(song1.getInfo(), song1)

// console
// song1.getInfo()
이 곡의 제목은 All I want is Christmas 이고 가수는 Mariah Carrey 입니다. 

// song1
Song {title: 'All I want is Christmas', singer: 'Mariah Carrey', year: 1995, getInfo: ƒ}
getInfo: ƒ ()
singer: "Mariah Carrey"
title: "All I want is Christmas"
year: 1995
[[Prototype]]: Object


```

