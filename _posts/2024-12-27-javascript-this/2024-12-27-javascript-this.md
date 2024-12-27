---
layout: post
title: "(javascript/js) 자바스크립트에서 this란?"
date: 2024-12-27 17:47:00 +09:00
lastmode: 2024-12-27 17:47:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - this
discription:
---

## this 키워드

`this` 라는 키워드는 여러 상황에서 다른 것을 참조하게 되는데 메소드에서는 `this`가 해당 객체를 참조하고, 함수에서는 `this`가 `window` 객체를 참조하게 된다. `constructor` 함수에서는 빈 객체를 참조한다.

<br>

### 메소드에서 this

메소드에서 `this`를 사용했을 때에는 `this`는 해당 객체를 가리킨다.

```js
// 메소드에서 this?
const audio = {
  title: "a",
  play() {
    console.log("play this", this);
  },
};

audio.play();
// 객체가 출력된다.
// play this > {title:'a', play: ƒ}

audio.stop = function () {
  console.log("stop this", this);
};

audio.stop();
// 동일하게 출력된다.
// stop this > {title: 'a', play: ƒ, stop: ƒ}
```

<br>

### 함수에서 this

함수에서 `this`는 `window` 객체를 가리킨다.

```js
// 함수에서 this?
// function => window object
function playAudio() {
  console.log(this);
}

playAudio();
// Window {window: Window, self: Window, document: document, name: '', location: Location, …}
```

<br>

### constructor function에서 this

생성자 함수(`constructor function`)에서 `this`는 빈 객체를 가리킨다.

```js
// 생성자 함수에서 this?
function Audio(title) {
  this.title = title;
  console.log(this);
}

const audio = new Audio("a");

// Audio {title: 'a'}
```

<br>

#### 객체안에 있는 메소드. 그 안에서의 this...

```js
const audio = {
  title: "audio",
  categories: ["rock", "pop", "hiphop"],
  displayCategories() {
    this.categories.forEach(
      function (category) {
        console.log(`title: ${this.title}, category: ${category}`);
      },
      { title: "audio" }
      // 여기서의 this는 더 이상 함수 안의 this가 아닌 메소드 안에 있는 것으로
      // audio 객체를 참조하기 때문에 audio를 출력하게 된다.
    );
  },
};
// 메소드안에 있는 this를 가장 먼저 감싸고 있는 것을 확인해야 한다.
// 함수 안에 있는 this는 window 객체를 참조하기 때문에 undefined..
// this가 audio를 참조하게 만들려면 forEach의 두 번째 매개변수에 { title: "audio" }를 입력해
// 콜백함수에서 this로 참조할 수 있게한다.

audio.displayCategories();
// title: undefined, category: rock
// title: undefined, category: pop
// title: undefined, category: hiphop

// { title: "audio" }
// title: audio, category: rock
// title: audio, category: pop
// title: audio, category: hiphop
```

<br>

#### 화살표 함수에서의 this

```js
const audio = {
  title: "audio",
  categories: ["rock", "pop", "hiphop"],
  displayCategories() {
    this.categories.forEach((category) => {
      console.log(this);
    });
  },
};

audio.displayCategories();
// 화살표함수에서 => this는 항상 상위 스코프의 this를 가리키게 된다.
// Lexical this
// {title: 'audio', categories: Array(3), displayCategories: ƒ}
// {title: 'audio', categories: Array(3), displayCategories: ƒ}
// {title: 'audio', categories: Array(3), displayCategories: ƒ}
```
