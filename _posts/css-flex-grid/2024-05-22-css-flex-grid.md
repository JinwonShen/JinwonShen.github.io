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

> 활용예시

```html 
<style>
    .container-1 {
      display: flex; /* 부모요소 */
      align-items: center; /* item의 세로방향 가운데 정렬 */
      align-items: start; /* item 상단배치 */
      align-items: end; /* item 하단배치 */
      align-items: stretch; /* item의 최대 높이로 맞추기 */

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

> 결과 이미지
<figure>
<img src="/assets/img/flex-img-1.png" alt="display:flex">
<figcaption>flex.1 display: flex;</figcaption>
</figure>

