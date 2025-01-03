---
layout: post
title: "(javascript/js) prototype"
date: 2025-01-04 02:25:00 +09:00
lastmode: 2025-01-04 02:25:00 +09:00
sitemap.changefreq: weekly
sitemap.priority: 0.5
categories: notice
usemathjax: true
tag:
  - javascript
  - js
  - prototype
  - OOP(Object Oriented Programming)
discription:
---

## 객체지향 프로그래밍(OOP, Object Oriented Programming)

- 코드의 간결함을 유지하고 재사용성을 향상시키기 위한 프로그래밍 방법론
- 프로그램을 명령어의 나열이 아닌 독립된 개념들의 상호작용으로 바라보는 것
- class와 object개념을 활용
- class로 object의 상태와 기능을 기술할 수 있고, 이를 이용하여 object를 생산할 수 있다.

### OOP 이해를 위한 필수 개념 !!

- 객체(object) : 특정 정보를 구성하는 독립적인 개념 / 단위를 일컫는 말

- 클래스(class) : 객체를 생성할 수 있는 내부 변수와 함수를 정의한 설계도

- 멤버변수(member variable) : 클래스 객체의 각종 상태값을 저장하고 있는 자체 변수

- 메서드(method) : 클래스 또는 클래스 객체가 보유한 자체 함수

- 생성자(constructor) : 클래스로 객체를 생성할때 사용하는 객체 초기화 함수

- 인스턴스(instance) : 클래스를 이용해 생성된 메모리에 올라간 객체(객체 생성 코드가 "실행" 된 것)

- 캡슐화(encapsulation) : 객체의 상태정보와 기능을 클래스라는 테두리 안에 가두어 설계하는 것

- 상속(inheritance) : 이미 존재하는 클래스를 기반삼아 더 확장된 기능을 가진 클래스를 만드는 것

<br>

### js에서 OOP 하기

- 일반적인 OOP언어들은 class-based language이다 (대표적으로 java, python 등)
- javascript는 prototype-based language라 불린다.
- javascript는 모든 객체가 기본적으로 object라는 built-in prototype을 탑재하고 있다.
- 생성자 함수와 new라는 키워드만 있으면 새로운 프로토타입을 만들 수 있다.

#### 일반 용어의 js버전

- 클래스(class) => 프로토타입(prototype)
- 멤버변수(member variable) => 프로퍼티(property)

<br>

## 프로토타입(prototype)

- js에서 어떠한 객체(=개념)를 설계할 수 있는 수단
- js에서 객체의 설계도를 상속받을 수 있는 메커니즘
- 프로토타입 체인 : prototype을 이용한 상속의 연결고리
- 객체의 프로토타입에 액세스 하는 방법
  - obj.`__proto__` (현재는 사용되지 않는 것으로 확인)
  - Object.getPrototype(obj)

<br>
