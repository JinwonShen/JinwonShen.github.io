---
layout: post
title: "(javascript/js) 상품 필터 기능 앱"
date: 2024-12-20 22:24:00 +09:00
lastmode: 2024-12-20 22:24:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - 구조분해할당
discription:
---

## 상품 필터 기능 앱 만들기

상품을 카테고리별로 분류하고 검색을 통해 상품 검색하기

<br>

```js
// product container
const productsContainerEl = document.querySelector(".products-container");

// 불변성을 지킴 - 원본데이터를 최대한 보존 = 이전과 이후 비교가 가능
// 얕은복사
// 재할당을 위해 let으로 변수할당
let filteredProducts = [...products];

// search
const formEl = document.querySelector(".input-form");
const searchInputEl = document.querySelector(".search-input");

formEl.addEventListener("keyup", () => {
  const inputValue = searchInputEl.value;
  filteredProducts = products.filter((product) => {
    return product.title.toLocaleLowerCase().includes(inputValue);
  });

  displayProducts();
});
```

<br>

모듈로 만들어 관리하지 않고, html에서 스크립트를 두 번 불러와 사용.. (순서 중요)

`<script src="products.js"></script>`<br>
`<script src="app.js"></script>`

<br>

```js
// product
const displayProducts = () => {
  productsContainerEl.innerHTML = filteredProducts
    .map((product) => {
      const { id, title, image, price } = product;
      return `<article class="product" data-id="${id}">
          <img
            src=${image}
            class="product-img img"
            alt="product-img"
          />
          <div>
            <h5 class="product-name">${title}</h5>
            <span class="product-price">${price}</span>
          </div>
        </article>`;
    })
    .join("");
};
displayProducts();
```

<br>

`const { id, title, image, price } = product;` 구조 분해 할당은 배열이나 객체의 속성을 해체해 그 값을 개별 변수에 담을 수 있게 하는 표현식이다.

<br>

```js
// company buttons
const companiesEl = document.querySelector(".companies");

// company button
const displayButtons = () => {
  const buttons = [
    "all",
    ...new Set(products.map((product) => product.company)),
  ];

  console.log(buttons);

  companiesEl.innerHTML = buttons
    .map((company) => {
      return `<button class="company-btn" data-id="${company}">${company}</button>`;
    })
    .join("");
};

displayButtons();
```

<br>

```js
// click event 발생
companiesEl.addEventListener("click", (e) => {
  const el = e.target;
  console.log(el);
  if (el.classList.contains("company-btn")) {
    if (el.dataset.id === "all") {
      filteredProducts = [...products];
    } else {
      filteredProducts = products.filter((product) => {
        return product.company === el.dataset.id;
      });
    }
    displayProducts();
  }
});
```

<br>
