---
layout: home
title: "html5"
keyword: "html5"
description: "html을 학습합니다."
---

# class 속성을 이용하여 요소를 선택합니다.

## 클래스
테그에 클래스 속성을 정의 할 수 있습니다.

### 속성지정

```html
<h1 class="heading">Hello World</h1>
```

## CSS 선택
css를 이용하여 클래스 속성을 선택할 수 있습니다.

### 단일 선택
클래스를 선택할 때에는 `.`를 사용합니다.
```css
.heading {
    color:red;
}
```

### 다중 틀래스 선택
여러개의 클래스 속성값을 가지는 요소를 선택할 수 있습니다.

```css
.a.b.c {
    color:red;
}
```
클래스 a, 클래스 b, 클래스 c 3개가 선택되어 있는 요소를 선택합니다.


## 클래스 적용

### 다중 클래스 적용
하나의 테그는 여러개의 클래스를 선택할 수 있습니다.
여러개의 클래스를 선택할 때에는 `스페이스`로 구분을 합니다.

```html
<h1 class="heading bold">Hello World</h1>
```

