---
layout: post
title: "(javascript/js) Throttle과 Debounce"
date: 2024-12-13 14:20:00 +09:00
lastmode: 2024-12-13 14:20:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - Throttle
  - Debounce
discription:
---

## Throttle

`_.throttle` 정해진 시간 간격으로 함수를 실행하도록 제한한다.

```js
window.addEventListener(
  "scroll",
  _.throttle(function () {
    console.log("Scroll!");
  }, 400)
);
```

<br>

## Debounce

`_.debounce` 정해진 시간 동안 함수가 실행되지 않으면, 함수를 실행한다.

```js
async function getMovies(movieName) {
  const res = await fetch(
    `https://omdbapi.com/?apikey=7035c60c&s=${movieName}`
  );
  return await res.json();
}
const inputEl = document.querySelector("input");
inputEl.addEventListener(
  "input",
  _.debounce(async function () {
    console.log(await getMovies(inputEl.value));
  }, 400)
);
```

<br>
