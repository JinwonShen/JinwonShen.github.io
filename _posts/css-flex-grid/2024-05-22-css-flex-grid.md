---
layout: post
title:  "CSS/Flex와 Grid 간단히 알아보기"
date:   2024-05-22 11:08:00 +09:00
categories: notice
usemathjax: true
tag:
  - css
  - grid
  - flex
---

## CSS의 Flex와 Grid 간단히 알아보기

### Flex

- Float 없이 정렬
- 반응형 친화적
- 자식 요소 위치 잡기가 쉬움
- 마진에서 자유로움
- 작은 단위의 레이아웃을 잡을때 유용

<br>

> flex 활용예시

```html 
<style>
    .container-1 {
      display: flex; /* flex.1 부모요소 */
      align-items: center; /* item의 세로방향 가운데 정렬 */
    }
    .container-1 > div {
      border: 1px solid #ddd;
    }

    .box-1 {
      flex: 1; /* box-1, box-2, box-3 - item의 비율 설정  */
    }
    .box-2 {
      flex: 1;
    }
    .box-3 {
      flex: 1;
    }
  </style>
<body>
  <div class="container-1">
    <div class="box-1">
      <h3>box-1</h3>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident amet laborum minus neque exercitationem nisi voluptates. Consequuntur incidunt dolor nesciunt.</p>
    </div>
    <div class="box-2">
      <h3>box-2</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea tempora quia exercitationem voluptatum esse, odio ab optio minus! Vitae exercitationem laudantium velit at magni? Adipisci odit dolore repellendus qui assumenda fuga cupiditate perferendis nulla eius, soluta reprehenderit distinctio, repellat rem! Quis cupiditate ut adipisci fuga enim esse accusamus suscipit natus!</p>
    </div>
    <div class="box-3">
      <h3>box-3</h3>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident amet laborum minus neque exercitationem nisi voluptates. Consequuntur incidunt dolor nesciunt.</p>
    </div>
    
  </div>
</body>
```

<br>

> 결과 이미지

<figure>
<img src="/assets/img/flex-img-1.png" alt="display:flex">
<figcaption>flex.1 display: flex;</figcaption>
</figure>

<br>

> flex 활용예시 2

```html
<style>
    .container-1 {
      display: flex; /* 부모요소 */
      align-items: start; /* flex.2 */
      align-items: end; /* flex.3 */
      align-items: stretch; /* flex.4 item의 최대 높이로 맞추기 */

    }
    .container-1 > div {
      border: 1px solid #ddd;
    }

    .box-1 {
      flex: 1; /* box-1, box-2, box-3 - item의 비율 설정  */
    }
    .box-2 {
      flex: 1;
    }
    .box-3 {
      flex: 1;
    }
  </style>
```

<br>

> 결과 이미지

<figure>
<img src="/assets/img/flex-img-2.png" alt="display:flex">
<figcaption>flex.2 align-items: start;</figcaption>
</figure>

<br>

<figure>
<img src="/assets/img/flex-img-3.png" alt="display:flex">
<figcaption>flex.3 align-items: end;</figcaption>
</figure>

<br>

<figure>
<img src="/assets/img/flex-img-4.png" alt="display:flex">
<figcaption>flex.4 align-items: stretch;</figcaption>
</figure>

<br>

> flex 활용예시 3

```html
<style>
    .container-1 {
          display: flex; 
          align-items: stretch;
          align-items: flex-end; /* flex.8 */
          justify-content: center; /* flex.5 */
          justify-content: flex-start; /* flex.6 */
          justify-content: flex-end; /* flex.7 */
        }
        .container-1 > div {
          border: 1px solid #ddd;
          max-width: 200px;
        }
    
        .box-1 {
          flex: 1; 
        }
        .box-2 {
          flex: 1;
        }
        .box-3 {
          flex: 1;
        }
  </style>
```

<br>

> 결과 이미지

<figure>
<img src="/assets/img/flex-img-5.png" alt="display:flex">
<figcaption>flex.5 justify-content: center;</figcaption>
</figure>

<br>

<figure>
<img src="/assets/img/flex-img-6.png" alt="display:flex">
<figcaption>flex.6 justify-content: flex-start;</figcaption>
</figure>

<br>

<figure>
<img src="/assets/img/flex-img-7.png" alt="display:flex">
<figcaption>flex.7 justify-content: flex-end;</figcaption>
</figure>

<br>

<figure>
<img src="/assets/img/flex-img-8.png" alt="display:flex">
<figcaption>flex.8 align-items: flex-end; justify-content: flex-end;</figcaption>
</figure>

<br>


> flex 활용예시 4

```html
<style>
    .container-1 {
          display: flex; 
          flex-direction: column; /* flex.13 가로 -> 세로로 변경 */
          align-items: center;
          justify-content: space-around; /* flex.9 */
          justify-content: space-between; /* flex.10 */
          justify-content: space-evenly; /* flex.11 */
        }
        .container-1 > div {
          border: 1px solid #ddd;
          max-width: 200px;
        }
    
        .box-1 {
          flex: 1; 
          order: 3; /* flex.12 순서를 임의로 변경하는 */
        }
        .box-2 {
          flex: 1;
          order: 1;
        }
        .box-3 {
          flex: 1;
          order: 2;
        }
  </style>
```

<br>

> 결과 이미지

<figure>
<img src="/assets/img/flex-img-9.png" alt="display:flex">
<figcaption>flex.9 justify-content: space-around;</figcaption>
</figure>

<br>

<figure>
<img src="/assets/img/flex-img-10.png" alt="display:flex">
<figcaption>flex.10 justify-content: space-between;</figcaption>
</figure>

<br>

<figure>
<img src="/assets/img/flex-img-11.png" alt="display:flex">
<figcaption>flex.11 justify-content: space-evenly;</figcaption>
</figure>

<br>

<figure>
<img src="/assets/img/flex-img-12.png" alt="display:flex">
<figcaption>flex.12 order: n;</figcaption>
</figure>

<br>

<figure>
<img src="/assets/img/flex-img-13.png" alt="display:flex">
<figcaption>flex.13 flex-direction: column;</figcaption>
</figure>

<br>


### Grid

- Flex와 구분되는 점은 자식요소를 상당히 특이한 모습으로 활용이 가능하다는 것.

<br>

> Grid 활용예시

```html
<style>
    .wrapper {
      /* display: flex; 와 구분되는 것은 자식요소가 상당히 특이한모양을 가질 수 있다는 것  */
      display: grid;
      /* grid-template-columns: 1fr 1fr 1fr; */
      grid-template-columns: repeat(3, 1fr); /* 1ft이 세번 반복되는 것 */
      /* grid-column-gap: 10px; */
      /* grid-row-gap: 10px; */
      grid-gap: 10px;
      grid-auto-rows: minmax(100px, auto) /* 최소 100px 넘치는 부분은 자동 */
    }
    .wrapper > div {
      background-color: #efefef;
      padding: 16px;
    }
    .wrapper > div:nth-child(odd) {
      background-color: #ddd;
    }
    /* 꼭짓점을 기준으로 */
    .item1 {
      grid-column: 1/4; /* column(가로)으로 1부터 4까지 */
    }
    .item4 {
      grid-row: 2/5; /* row(세로)로 2부터 5까지 */
      grid-column: 3/4; /* column(가로)으로 3부터 4까지  */
    }
  </style>
<body>
  <div class="wrapper">
    <div class="item item1">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum soluta iste exercitationem. Consequuntur debitis nesciunt illum facere aperiam explicabo magnam.
    </div>
    <div class="item item2">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facere fuga molestiae quos ducimus beatae placeat nihil rerum doloremque quidem culpa.
    </div>
    <div class="item item3">
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequatur reiciendis, eveniet exercitationem explicabo rem earum officia odit cumque eos quasi.
    </div>
    <div class="item item4">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quas vel corporis tenetur accusantium, fugiat quisquam? Animi, tenetur similique molestias provident beatae minus ducimus pariatur cupiditate explicabo nostrum, autem eveniet saepe?
    </div>
    <div class="item item5">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quas vel corporis tenetur accusantium, fugiat quisquam? Animi, tenetur similique molestias provident beatae minus ducimus pariatur cupiditate explicabo nostrum, autem eveniet saepe?
    </div>
    <div class="item item6">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quas vel corporis tenetur accusantium, fugiat quisquam? Animi, tenetur similique molestias provident beatae minus ducimus pariatur cupiditate explicabo nostrum, autem eveniet saepe?
    </div>
    <div class="item item7">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quas vel corporis tenetur accusantium, fugiat quisquam? Animi, tenetur similique molestias provident beatae minus ducimus pariatur cupiditate explicabo nostrum, autem eveniet saepe?
    </div>
    <div class="item item8">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quas vel corporis tenetur accusantium, fugiat quisquam? Animi, tenetur similique molestias provident beatae minus ducimus pariatur cupiditate explicabo nostrum, autem eveniet saepe?
    </div>
  </div>
</body>
```

<br>

> 결과 이미지

<figure>
<img src="/assets/img/grid-img-1.png" alt="display: grid;">
<figcaption>grid.1 display: grid;</figcaption>
</figure>

<br>

--- 

<br>

**한줄평**
<!-- ## 한줄평  -->

_"여기까지 레이아웃, 그리드를 잡는 데 중요하다고 생각하는 flex와 grid를 알아보았습니다. 반응형 웹을 제작하는 데 있어 가장 중요한 역할을 하는 것 중 하나라고 생각해서 연습이 많이 필요할 것 같다."_
