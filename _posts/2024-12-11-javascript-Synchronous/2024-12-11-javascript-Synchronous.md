---
layout: post
title: "(javascript/js) 동기 비동기"
date: 2024-12-11 22:50:00 +09:00
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - 동기(Synchronous)
  - 비동기(Asynchronous)
  - Callback
  - Callback Hell
  - Async & Await
  - Promise
  - try
  - Pending
  - Fulfilled
  - Rejected
  - .then()
  - .catch()
  - .finally()
  - fetch
discription:
---

## 동기(Synchronous)

하나의 작업이 끝나기 전에는 다음 작업이 시작되지 않는다.

### 간단한 예시

```js
console.log(1);
console.log(2);

alert("확인!"); // alert 창이 발생하기 전에 log(3) 이후 작업이 진행되지 않음.

console.log(3);
console.time("Loop!");
for (let i = 0; i < 100000000; i++) {}
console.timeEnd("Loop!");
console.log(4);

// 1
// 2
// 3
// Loop!: 68.593017578125 ms
// 4
```

<br>

## 비동기(Asynchronous)

특정 작업이 끝나기 전에 다음 작업이 시작될 수 있다.

### 간단한 예시

```js
console.log(1);
console.log(2);
console.log(3);
console.time("Loop!");

setTimeout(() => {
  for (let i = 0; i < 100000000; i++) {}
  console.timeEnd("Loop");
}, 0);

// 1
// 2
// 3
// 4
// Loop!: 45.551025390625 ms
// 5
```

<br>

```js
console.log(1);
const h1El = document.querySelector("h1");
// 사용자가 클릭하지 않으면 실행되지 않는다. 비동기 방식으로 실행.
h1El.addEventListener("click", () => {
  console.log("클릭!");
});
console.log(2);
```

<br>

```js
console.log(1);
// 서버와의 통신도 병렬로 즉, 비동기 방식으로 실행이 된다.
fetch("https://api.heropy.dev/v0/users")
  .then((res) => res.json())
  .then((data) => console.log(data));
console.log(2);
```

<br>

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="pvzEyyp" data-pen-title="js/비동기(Asynchronous)" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/pvzEyyp">
  js/비동기(Asynchronous)</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 비동기 - 콜백과 콜백 지옥(Callback Hell)

특정한 비동기 함수를 호출할 때 콜백함수를 전달하면서 어느 위치에서 실행할지 지정해줄 수 있다.
내가 지정된 위치해서 실행되기 때문에 원하는 동작을 만들 수 있다.

```js
// main.js
import { timer } from "./timer.js";

timer(() => {
  console.log(2); // 두 번째 실행
});
```

<br>

```js
// timer.js
export function timer(callback) {
  setTimeout(() => {
    console.log(1); // 첫 번째 실행
    callback();
  }, 2000);
}
```

<br>

**따라하기**

기존의 콜백패턴(콜백지옥)의 개선

```js
// 콜백패턴
function renderImage(callback) {
  const imgEl = document.createElement("img");
  imgEl.src = "https://picsum.photos/2000/1000";
  imgEl.addEventListener("load", () => {
    document.body.append(imgEl);
    callback();
  });
}
// 비동기 코드를 동기 방식으로 사용하며 안쪽으로 계속 들여쓰여짐 (콜백지옥 - 가독성 떨어짐 유지보수 불편)
renderImage(() => {
  console.log("Done 1");
  renderImage(() => {
    console.log("Done 2");
    renderImage(() => {
      console.log("Done 3");
      renderImage(() => {
        console.log("Done 4");
      });
    });
  });
});
```

<br>

Promise를 활용한 개선코드

```js
function renderImage() {
  return new Promise((resolve) => {
    const imgEl = document.createElement("img");
    imgEl.src = "https://picsum.photos/2000/1000";
    imgEl.addEventListener("load", () => {
      document.body.append(imgEl);
      resolve();
    });
  });
}
// 가독성이 좋아짐.. then과 Promise 와의 관계
renderImage()
  .then(() => {
    console.log("Done 1");
    return renderImage();
  })
  .then(() => {
    console.log("Done 2");
    return renderImage;
  })
  .then(() => {
    console.log("Done 3");
    return renderImage;
  })
  .then(() => {
    console.log("Done 4");
  });
```

<br>

## 비동기 - Promise

비동기 작업의 완료나 실패 시점을 지정하고 그 결과를 반환할 수 있다.
`const promise = new Promise((resolve(성공), reject(실패))=>{})`

<br>

**Promise와 then을 사용하는 방식**

```js
function loadImage(src) {
  return new Promise((resolve) => {
    const imgEl = document.createElement("img");
    imgEl.src = src;
    imgEl.addEventListener("load", () => {
      resolve(imgEl); // 원하는 시점에서 호출(특정 시점에서 약속을 이행한다.)(반환결과)
    });
  });
}
// .then() 약속이 이행되면 then 메소드를 호출한다.
loadImage("https://picsum.photos/2000/1000").then((imgEl) => {
  document.body.append(imgEl);
  console.log("Done 1");
});
loadImage("https://picsum.photos/100/200").then((imgEl) => {
  console.log(imgEl);
});
```

<br>

**async와 await 를 사용하는 방식**

```js
// 비동기
function loadImage(src) {
  return new Promise((resolve) => {
    const imgEl = document.createElement("img");
    imgEl.src = src;
    imgEl.addEventListener("load", () => {
      resolve(imgEl); // 원하는 시점에서 호출(특정 시점에서 약속을 이행한다.)(반환결과)
    });
  });
}

// async와 await 를 사용하는 방식
(async () => {
  // 즉시실행함수
  const imgEl = await loadImage("https://picsum.photos/2000/1000");
  document.body.append(imgEl);
  console.log("Done 1");

  const imgEl2 = await loadImage("https://picsum.photos/100/200");
  console.log(imgEl2);
})();
```

<br>

## 비동기 - Async & Await

서버에서 데이터를 가져오고 딜레이되는 시간에 에니메이션을 작동하기

**따라하기**

```js
// Async-Await
const h1El = document.querySelector("h1");
const ulEl = document.createElement("ul");
ulEl.classList.add("users");
document.body.append(ulEl);

// await는 async와 항상 함께쓴다. 비동기
h1El.addEventListener("click", async () => {
  const loaderEl = document.createElement("div");
  loaderEl.classList.add("loader");
  ulEl.innerHTML = ""; // 빈 문자로 내용을 비우고나서 다시 채워넣는다.
  ulEl.append(loaderEl);
  // fetch 함수 호출을 통해서는 promise 인스턴스가 반환됨 // await : 데이터를 전달받을 떄 까지 기다렸다가 실행
  const res = await fetch("https://api.heropy.dev/v0/users");
  const data = await res.json();
  console.log(data); // 데이터를 가져온 결과
  const { users } = data; // 배열데이터
  const liEls = users.map((user) => {
    // .map : 콜백에서 반환하는 데이터를 모아서 새로운 배열을 만듬
    const liEl = document.createElement("li");
    liEl.textContent = user.name;
    liEl.dataset.photo = user.photo?.url || "http://heropy.dev/favicon.png";
    if (!user.photo) {
      liEl.classList.add("no-photo");
    }
    const loaderEl = document.createElement("div");
    loaderEl.classList.add("loader");
    liEl.prepend(loaderEl); // .prepend : li요소에 가장 앞쪽에 이미지요소 추가
    return liEl;
  });
  loaderEl.remove();
  ulEl.append(...liEls);
  liEls.forEach(async (liEl) => {
    const imgEl = await loadImage(liEl.dataset.photo);
    liEl.prepend(imgEl);
    liEl.querySelector(".loader").remove();
  });
});

function loadImage(src) {
  return new Promise((resolve) => {
    const imgEl = document.createElement("img");
    imgEl.src = src;
    imgEl.addEventListener("load", () => {
      resolve(imgEl);
    });
  });
}
```

<br>

위 코드에서 예외처리를 포함해 개선한 코드

**따라하기 예외처리**

```js
// Async-Await
const h1El = document.querySelector("h1");
const ulEl = document.createElement("ul");
ulEl.classList.add("users");
document.body.append(ulEl);

// await는 async와 항상 함께쓴다. 비동기
h1El.addEventListener("click", async () => {
  const loaderEl = document.createElement("div");
  loaderEl.classList.add("loader");
  ulEl.innerHTML = ""; // 빈 문자로 내용을 비우고나서 다시 채워넣는다.
  ulEl.append(loaderEl);
  try {
    // 예외처리 try() catch(){} 키워드를 활용.
    // fetch 함수 호출을 통해서는 promise 인스턴스가 반환됨 // await : 데이터를 전달받을 떄 까지 기다렸다가 실행
    const res = await fetch("https://api.heropy.dev/v0/users");
    const data = await res.json();
    console.log(data); // 데이터를 가져온 결과
    const { users } = data; // 배열데이터
    const liEls = users.map((user) => {
      // .map : 콜백에서 반환하는 데이터를 모아서 새로운 배열을 만듬
      const liEl = document.createElement("li");
      liEl.textContent = user.name;
      liEl.dataset.photo = user.photo?.url || "http://heropy.dev/favicon.png";
      if (!user.photo) {
        liEl.classList.add("no-photo");
      }
      const loaderEl = document.createElement("div");
      loaderEl.classList.add("loader");
      liEl.prepend(loaderEl); // .prepend : li요소에 가장 앞쪽에 이미지요소 추가
      return liEl;
    });
    loaderEl.remove();
    ulEl.append(...liEls);
    liEls.forEach(async (liEl) => {
      try {
        const imgEl = await loadImage(liEl.dataset.photo);
        liEl.prepend(imgEl);
      } catch (error) {
        console.log(error);
      } finally {
        // 정상적으로 동작할 때와 그렇지 않을 때를 동일하게 만들어주기 위해 finally 구문을 추가적으로 활용
        liEl.querySelector(".loader").remove();
      }
    });
  } catch (error) {
    // try 부분에서 예외상황(에러 등)이 생기면 바로 catch 부분으로 내려옴
    console.log(error);
    ulEl.textContent = "사용자 정보를 찾을 수 없어요..";
    loaderEl.remove();
  }
});

function loadImage(src) {
  return new Promise((resolve, reject) => {
    const imgEl = document.createElement("img");
    imgEl.src = src;
    imgEl.addEventListener("load", () => {
      resolve(imgEl);
    });
    imgEl.addEventListener("error", () => {
      // 약속을 이행하지 못했을 떄의 상황(reject)
      reject(new Error("이미지를 로드할 수 없어요.."));
    });
  });
}
```

<br>

### 비동기코드를 순차적으로 반복처리할 때 주의해야할 부분

<br>

### 이행과 거부, 예외처리

`Pending` - 약속이 이행되거나 거부되기 직전의 상태(대기)

`Fulfilled` - 약속이 이행된 상태(이행)

`Rejected` - 약속이 거부된 상태(거부)

<br>

### .then() / .catch() / .finally()

`.then()` - 약속이 이행되었을 떄 호출(then)하거나,

`.catch()` - 약속이 거부되었을 때 호출(catch)하거나,

`.finally()` - 이행 및 거부와 상관없이 항상 호출(finally)하는 메소드를 제공

<br>

#### 간단한 예시

```js
loadImage("https://picsum.photo/300")
  .then((imgEl) => {
    document.body.append("imgEl");
  })
  .catch((error) => {
    console.log(error.message);
  })
  .finally((imgEl) => {
    console.log("Done!");
  });
```

<br>

### try / catch / finally 구문 (비교적 최신의)

`try` - 에러(예외)가 발생할 수 있는 코드의 실행을 시도(try)하고,

`catch` - 에러가 발생하면 시도를 종료해 에러를 잡아내며(catch)

`finally` - 에러 여부와 상관없이 항상 실행(finally)하는 코드를 정의할 수 있다.

<br>

#### 간단한 예시

```js
(async () => {
  try {
    const imgEl = await loadImage("https://picsum.photo/300");
    document.body.append(imgEl);
  } catch (error) {
    console.log(error.message);
  } finally {
    console.log("Done!");
  }
})();
```

<br>

## 네트워크 통신과 fetch 함수

```
//           요청(Request)
// 클라이언트 ---------------->
//         <---------------- 서버
//           응답(Response)
```

<br>

**요청(Request)**

- url: 요청 서버 주소
- method: 요청 종류(GET, POST, PUT, DELETE 등)
  - GET: 데이터를 조회
  - POST: 데이터를 생성해달라고 요청
  - PUT: 데이터를 수정해달라고 요청
  - DELETE: 데이터를 삭제해달라고 요청
- headers: 요청 메타 정보
- body: 요청 데이터

**응답(Response)**

- status: 응답 상태 코드(200, 400, 500 emd)
- headers: 응답 메타 정보
- body: 응답 데이터
- ok: 정상적인 처리 여부

**CRUD (method의 정보와 일치)**

- Create: POST - 데이터 생성
- Read: GET - 데이터 조회
- Update: PUT(PATCH) - 데이터 수정
- Delete: DELETE - 데이터 삭제

**URL 구조**

- https://www.heropy.dev/p/QOWqjv?key=value&a=12&b=34#h1-title
- https: 통신규약(Protocol)
  - Hyper Text Transfer Protocol Secure
- www.heropy.dev: 도메인(Domain)
  - www: subdomain
  - heropy: Domain Name
  - dev: Top-level Domain
- /p/: 경로(Path)
- QOWqjv?key=value&a=12&b=34#h1-title: 쿼리(Query String)
  - ? 뒤에는 =, &등 기호가 하나이상 등장
  - #h1-title: 해시(Hash)

**HTTP 상태 코드**

- 1xx: 처리 중
- 2xx: 성공
- 3xx: 리다이렉트(재전송)
- 4xx: 클라이언트 오류
- 5xx: 서버 오류

_그 외_

- 200: 정상적으로 처리됨
- 400: 잘못된 요청
- 401: 인증 정보가 부족함
- 403: 권한이 없음
- 404: 찾을 수 없음(ex-Page not found)
- 500: 서버 오류

<br>

## fetch 함수

`fetch(url, options)`

- options.method: 요청의 종류(GET, POST, PUT, DELETE 등)
- options.headers: 요청 메타 정보
- options.body: 요청 데이터

### 간단한 예시

```js
// 서버의 특정 사용자 데이터를 수정하는 예시
fetch("https://api.heropy.dev/v0/users/ywTTX", {
  method: "PUT", // 데이터 수정
  headers: {
    "Contents-Type": "application/json",
  },
  body: JSON.stringify({
    name: "Neon",
    age: 22,
    isValid: false,
  }),
})
  .then((res) => res.json())
  .then((data) => console.log(data));
```

<br>
