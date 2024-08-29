---
layout: post
title:  "Javascript/dom 다루기"
date:   2024-08-27 23:29 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - dom
---

## html 태그를 다룰 수 있는 document 오브젝트 모델을 다루는 방법

<br>

```js
// 돔 선택
const output = document.querySelector("#button")
const wrapper = document.querySelector(".wrapper")
const items = document.querySelectorAll(".item")
const target = document.querySelector(".target")
const point = document.querySelector(".point")
const userID = document.querySelector("#userID")
const title = document.querySelector("h1")

// 프로퍼티에 접근해 속성 변경
target.style.color = "red";
target.style.fontSize = "36px";


// event는 ?

// 1
title.addEventListener("click" /* 이벤트 명 */, function() /* 함수 */{
    title.style.color = "red";
})

// 2
userID.addEventListener("input", function(e){
    // console.log(this/* 이벤트가 일어난 대상을 가리킴 */.value)
    target.innerText = this.value
})

// 3
button.addEventListener("click", () => { 
    /* aorrw function 일때는 this를 사용하지 않음 */
    target.style.width = "50px"
    target.style.height = "50px"
    target.style.backgroundColor = userID.value;
    target.style.borderRadius = "50%"
})

// 4
items.forEach(item => {
    item.addEventListener("click", () => {
        point.innerHTML = item.innerText
    })
})

console.log(items)
```

<br>

#### 이미지 활용해서 업로드 이어 진행

<br>

<figure>
<img src="/assets/img/flex-img-1.png" alt="display:flex">
<figcaption>flex.1 display: flex;</figcaption>
</figure>

