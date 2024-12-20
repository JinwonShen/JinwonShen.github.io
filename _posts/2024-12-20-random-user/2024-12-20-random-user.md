---
layout: post
title: "(javascript/js) 랜덤 유저 앱"
date: 2024-12-20 13:45:00 +09:00
lastmode: 2024-12-20 13:45:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - module
  - import
  - export
discription:
---

## 랜덤 유저 앱 만들기

`RANDOM USER` 버튼을 클릭하면 새로운 유저를 가져와 다양한 버튼을 클릭해 유저의 데이터를 확인할 수 있는 앱

<br>

### 예제

**모듈로 관리하기**

```js
// getElement
const getElement = (selection) => {
  const element = document.querySelector(selection);
  // element에서 인수로 받는 요소가 없는 요소일 경우에는 강제로 에러를 내보내주는 "throw"
  if (element) return element;
  throw new Error("...");
};

// default 내보내기
export default getElement;
```

<br>

`throw` 문은 사용자 정의 예외를 발생(`throw`)할 수 있다. 예외가 발생하면 현재 함수의 실행이 중지되고 (`throw` 이후의 명령문은 실행되지 않는다.)

재사용을 위해 `const getElement` 라는 함수를 만들어 `selection` 이라는 인수로 요소를 받아 사용

<br>

```js
// fetchUser
const URL = "https://randomuser.me/api/";
const getUser = async () => {
  const response = await fetch(URL);
  const data = await response.json();
  console.log(data);
  const person = data.results[0];
  const { phone, email } = person;
  const { large: image } = person.picture;
  const { password } = person.login;
  const { first, last } = person.name;
  const {
    dob: { age },
  } = person;
  const {
    street: { number, name },
  } = person.location;
  return {
    image,
    phone,
    email,
    password,
    age,
    street: `${number} ${name}`,
    name: `${first} ${last}`,
  };
};

export default getUser;
```

<br>

`const URL = "https://randomuser.me/api/";` 요청을 보낼 경로를 지정한다.

비동기 요청을 위해 `async`와 `await` 문법을 사용해 프라미스를 좀 더 편하게 사용할 수 있다. `async`는 `function` 앞에 붙여 사용하고 해당 함수는 항상 프라미스를 반환한다.

`await`는 `async` 함수 안에서만 동작한다.

`fetch()` 메서드는 네트워크에서 리소스를 취득하는 절차를 시작하고, 응답이 사용 가능해지만 이행하는 프로미스를 반환한다.

<br>

```js
// removeActive
export default function removeActive(items) {
  items.forEach((btn) => {
    btn.classList.remove("active");
  });
}
```

<br>

`export default` 를 생성한 함수 바로앞에 입력해 내보내기

<br>

```js
// displayUser
const userImage = getElement(".user-img");
const title = getElement(".user-title");
const value = getElement(".user-value");
const btns = [...document.querySelectorAll(".icon")];

const displayUser = (person) => {
  userImage.src = person.image;
  value.textContent = person.name;
  title.textContent = "My name is";
  removeActive(btns);
  btns.forEach((btn) => {
    const label = btn.dataset.label;
    btn.addEventListener("click", () => {
      title.textContent = `My ${label} is `;
      value.textContent = person[label];
      removeActive(btns);
      btn.classList.add("active");
    });
  });
};

export default displayUser;
```

<br>

```js
// 관리할 스크립트에서 가져오기
import displayUser from "./utils/displayUser.js";
import getUser from "./utils/fetchUser.js";
import getElement from "./utils/getElement.js";
// 내보낼 때 default로 내보내 {}를 생략

const btn = getElement(".btn");

const showUser = async () => {
  const person = await getUser();
  displayUser(person);
};

window.addEventListener("DOMContentLoaded", showUser);
btn.addEventListener("click", showUser);
```

<br>

`import` 받은 함수들을 그대로 사용할 수 있음.

<br>
