---
layout: post
title: "(javascript/js) class"
date: 2024-12-10 16:51:00 +09:00
lastmode: 2024-12-10 16:51:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - class
discription:
---

## class

`class` 선언은 프로토타입 기반 상속을 사용하여, 주어진 이름의 새로운 클래스를 만든다.

### 간단한 예시

```js
class Polygon {
  constructor(height, width) {
    this.name = "Polygon";
    this.height = height;
    this.width = width;
  }
}
```

<br>

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="RNbRyyX" data-pen-title="js/class/프로토타입" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/RNbRyyX">
  js/class/프로토타입</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## Getter & Setter

클래스의 메소드 부분에 `get` 이라는 키워드가 붙어 속성처럼 사용하는 것이 가능하고 값을 얻을 때 함수가 실행이 된다.

`set` 이라는 키워드가 붙어있는 메소드이고 마치 속성처럼 사용하되 할당연산자로 값을 지정할 때 호출되는 함수다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="ogvLdRR" data-pen-title="js/class/Getter &amp;amp; Setter" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/ogvLdRR">
  js/class/Getter &amp; Setter</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>

## 정적 메소드(Static method)

정적 메소드는 주로 클래스의 유틸리티 (보조) 함수를 만들 때 사용한다. 인스턴스와는 연결되지 않으며, 클래스 자체에서 호출해야 한다.

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="jENrKoQ" data-pen-title="Untitled" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/jENrKoQ">
  Untitled</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## 상속(Inheritance)

클래스의 속성과 메소드를 다른 클래스에게 확장(Extends)해 재사용 하는 기능을 말한다.

### 간단한 예시

```js
class A {
  constructor(a) {
    this.a = a;
  }
}

class B extends A {
  constructor(a, b) {
    super(a);
    this.b = b;
  }
}

const a = new A(1);
const b = new B(1, 2);

console.log(a);
console.log(b);
```

<br>

**따라하기**

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="WbexKZW" data-pen-title="js/class/Inheritance(상속) 다른유형의" data-preview="true" data-user="sjinwon" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/sjinwon/pen/WbexKZW">
  js/class/Inheritance(상속) 다른유형의</a> by Shen Jinwon (<a href="https://codepen.io/sjinwon">@sjinwon</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

<br>
