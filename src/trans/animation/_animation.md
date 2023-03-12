---
layout: home
title: "CSS - Learn html5"
keyword: "css, css3, html5"
description: "hcss3에 대해서 학습합니다."
breadcrumb:
- css
- animation
---

## animation
에니메이션은 트랜지션과 달리 동작조건을 부여하지 않아도,
자체적으로 효과를 수행할 수 있도록 지정할 수 있습니다.


## 프레임 정하기
에니메이션에 대한 프레임 갯수를 지정합니다.

```css
@keyframes 이름 {
            
}
```

## 동작횟수 지정하기
기본적으로 에니메이션은 페이지 로딩후 1번만 수행이 됩니다.
만일 여러번의 동작을 수행해야 하는 경우 횟루를 지정할 수 있습니다.

```css
animation-iteration-count: 5;
```

무한반복을 설정하고자 할때에는 infinite 로 값을 지정합니다.

```css
animation-iteration-count: infinite;
```

## 동작함수

```css
animation-timing-function: ease; 
```


## 시작/끝 동작
동작의 시작과 끝에 대한 동작을 지정할 수 있습니다.

* alternate
0->100 , 100->0으로 동작합니다.


```css
animation-direction: alternate; 
```

## 잛게 표현

animation 속성을 통하여 여러 동작 효과를 한줄로 작성을 할 수 있습니다.

```css
animation: 키프레임명 실행시간 움직임 딜레이 반복 처리방법;
```


