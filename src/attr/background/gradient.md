---
layout: home
title: "CSS - Learn html5"
keyword: "css, css3, html5"
description: "hcss3에 대해서 학습합니다."
breadcrumb:
- css
---

# gradient
---

멀티 백그라운드 기능을 같이 사용할 수도 없습니다.

* linear
* radial

## 2색 지정

```css
div {
    background: linear-gradient(pink, purple);
}
```

> 예제코드: ./sample/gradient01.html

기본값으로 첫번째 지정한 색이 `위쪽`, 두번째 지정한 색이 `아래쪽`에 배치를 하게 됩니다.


### 방향으로 지정하기

`to 방향`을 추가하여 `도작 지점`을 지정합니다.

왼쪽에서 오른쪽으로 gradient 적용하기

```css
div {
    background: linear-gradient(to right, pink, purple);
}
```

> 예제코드: ./sample/gradient02.html

오른쪽에서 왼쪽쪽으로 gradient 적용하기

```css
div {
    background: linear-gradient(to left, pink, purple);
}
```

> 예제코드: ./sample/gradient03.html

대각선 적용

```css
div {
    background: linear-gradient(to top right, pink, purple);
}
```

### 각도로 지정하기

각도값을 +/- 로 지정을 합니다.

```css
div {
    background: linear-gradient(90deg, pink, purple);
}
```

## 여러색 적용하기

여러개의 색을 적용을 할때에는 지정한 색의 수많큼 균등분할하여 적용이 됩니다.


```css
div {
    background: linear-gradient(90deg, pink, purple, blue);
}
```

## gradient와 배경색 같이 넣기
기본적으로 gradient와 배경색을 같이 표시를 할 수 없습니다.
다만, gradient를 색상값을 투명도가 지정된 방식으로 적용할 경우, 배경색을 같이 사용을 할 수 있습니다.

```css
div {
    background: linear-gradient(to left, rega(), rega()) 배경색;
}
```

## 반복 적용하기
gradient의 적용범위를 지정하여 반복할 수 있습니다.

```css
div {
    background: repeating-linear-gradient(to left, pink 10%, purple 20%);
}
```
범위를 지정하여 패턴화 하여 적용할 수도 있습니다.


## 원형 gradient

```css
div {
    background: radial-gradient(pink, purple, red);
}
```

> 예제코드: ./sample/gradient21.html

### 비율 지정하기

```css
div {
    background: radial-gradient(pink 15%, purple 25%, red 60%);
}
```

> 예제코드: ./sample/gradient22.html

### circle 설정
radial은 삽입하고자 하는 영역의 비율대로 원형모향으로 들어가게 됩니다.

만일 영역이 정사각이 아닌 직사각형 일때 원형이 아닌 `타원` 모양으로 들거가게 됩니다.

```css
div {
    width:400px; height:200px;
    border: 1px slid red;

    background: radial-gradient( pink 15%, purple 25%, red 60%);
}
```

> 예제코드: ./sample/gradient23.html

이를 원형 모양으로 들어가게 보정을 하기 위해서는 `circle` 옵션을 부여합니다.

```css
div {
    width:200px; height:200px;
    border: 1px slid red;

    background: radial-gradient(circle, pink 15%, purple 25%, red 60%);
}
```

> 예제코드: ./sample/gradient24.html


## gradient 실습하기
실습을 통하여 다양한 gradient 를 학습해 보도록 합니다.

### 무지개 만들기

> 예제코드: ./sample/gradient31.html


## 포토샵 구현




