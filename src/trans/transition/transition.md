---
layout: home
title: "CSS - Learn html5"
keyword: "css, css3, html5"
description: "hcss3에 대해서 학습합니다."
breadcrumb:
- css
---

> CSS3
## transition
CSS에서 움직이는 표현을 처리하는 기술로 animation과 transition 이 있습니다.

## 동작조건
transition 을 처리하기 위해서는 특수한 조건이 필요 합니다.



## 설정위치
transition 동작 조건의 이전단계에 설정을 해야 합니다.



## transition-property
적용하고자 하는 transition 효과를 제한합니다.

```css
transition-property: border-radius;
```

여러개의 효과를 허용하기 위해서는 `콤마`로 구분합니다.


## transition-duration
효과를 적용하는 시간

```css
transition-duration: 2s;
```

transition은 시작할때도 적용되지만, 반대 동작에도 적용됩니다.

## transition-delay
transition 동작을 일정한 시간동안 지연시킨 다음에 시작을 합니다.

```css
transition-delay: 0.5s;
```

## tansition-timing-function
동작하는 효과를 지정할 수 있습니다.

부드러운 동작을 처리할 수 있습니다.
* ease
* ease-in
* ease-out


## 잛게 표현

```css
transition: background 2s 05s ease;
```


```css
transition: background 2s 05s ease, border-radius 3s;
```


## all
모든 효과를 허용합니다.

```css
transition: all .5s;
```














