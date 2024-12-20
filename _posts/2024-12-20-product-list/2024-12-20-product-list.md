---
layout: post
title: "(javascript/js) 상품 리스트 앱"
date: 2024-12-20 22:30:00 +09:00
lastmode: 2024-12-20 22:30:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - e.preventDefault()
  - appendChild
  - createTextNode
  - insertBefore
  - class
  - constructor
discription:
---

## 상품 리스트 필터기능 만들기

상품 페이지의 상품들을 카테고리에 맞춰 필터링해주는 기능

<br>

```js
// script
import { UI } from "./ui.js";
import { Product } from "./product.js";

const formEl = document.getElementById("product-form");
const nameInputEl = document.getElementById("name");
const priceInputEl = document.getElementById("price");
const yearInputEl = document.getElementById("year");

formEl.addEventListener("submit", (e) => {
  e.preventDefault(); // refresh 방지

  const name = nameInputEl.value;
  const price = priceInputEl.value;
  const year = yearInputEl.value;

  const product = new Product(name, price, year);

  const ui = new UI();

  // 유효성 체크

  if (name === "" || price === "" || year === "") {
    // 오류메시지
    return ui.showMessage("모든 필드에 데이터를 삽입 하십시오.", "error");
  }
  // 추가
  ui.addProduct(product);

  // 성공메시지
  ui.showMessage("제품이 성공적으로 추가되었습니다.", "success");

  // field 초기화
  ui.resetForm();

  // Delete
  document.getElementById("product-list").addEventListener("click", (e) => {
    const ui = new UI();
    ui.deleteProduct(e.target);
  });
});
```

<br>

```js
// UI
export class UI {
  addProduct(product) {
    const productList = document.getElementById("product-list");
    const element = document.createElement("div");

    element.innerHTML = `
    <div class="u-full-width">
        <div>
            <strong>상품 이름</strong>: ${product.name} -
            <strong>상품 가격</strong>: ${product.price} -
            <strong>상품 연도</strong>: ${product.year} -
            <a href="#" name="delete">X</a>
        </div>
    </div>
    `;
    productList.appendChild(element);
  }

  showMessage(message, cssClass) {
    const div = document.createElement("div");
    div.className = `alert ${cssClass}`;
    div.appendChild(document.createTextNode(message));

    const container = document.querySelector(".container");
    const form = document.querySelector("#product-form");

    container.insertBefore(div, form);

    setTimeout(() => {
      document.querySelector("alert").remove();
    }, 3000);
  }

  resetForm() {
    document.getElementById("product-form").reset();
  }

  deleteProduct(element) {
    if (element.name === "delete") {
      element.parentElement.parentElement.remove();
      this.showMessage("제품이 성공적으로 삭제되었습니다.", "success");
    }
  }
}
```

<br>

```js
// product
export class Product {
  constructor(name, price, year) {
    this.name = name;
    this.price = price;
    this.year = year;
  }
}
```

<br>
