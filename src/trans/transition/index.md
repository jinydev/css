---
layout: home
title: "CSS - Learn html5"
keyword: "css, css3, html5"
description: "hcss3에 대해서 학습합니다."
breadcrumb:
- css
---


# CSS-transition

transition의 사전적 의미는 "전환"입니다. transition은 속성 값이 변화 될때 더욱더 부드럽게 전환이 가능하도록 도와주는 속성이라 할 수 있습니다.


## 시간에 따른 변화를 만들어 주는 트랜지션
트랜지션(transition)이란 한 스타일에서 다른 스타일로 바뀌는 것을 말합니다. 

플래시나 자바스크립트 
를 사용하지 않고 CSS 소스만으로 애니메이션 효과를 내는 방법에 대해 알아봅니다. 

### transition-property 속성 - 적용할 트랜지션 지정하기
트랜지션 효과를 만드는 첫 번째 단계는 CSS 속성 중 어떤 속성에 트랜지션을 적용할 것인지 선택 
하는 것입니다.

```css
transition-property:속성 값;
```


* none : 트랜지션 동안 아무 속성도 바뀌지 않습니다.

* all : all 값을 사용하거나 transition-property를 생략할 경우 요소의 모든 속성이 트랜지션 대상이 됩니 
다. 기본 값입니다.

* 속성이름 : 트랜지션 효과를 적용할 속성 이름을 지정합니다. 예를 들어. 배경색만 바꿀 것인자 width 값을 바 
꿀 것인지 원하는 것만 골라 지정할 수 있습니다. 속성이 여럿일 경우 쉼표0로 구분하여 나열합니다.


### transition-duration 속성 - 트랜지션 진행 시간 지정하기
트랜지션이 진행될 시간을 지정합니다.
속성이 여럿이라면 트랜지션 진행 시간도 쉼 
표(,)로 구분하여 순서대로 여러 개 지정할수 있습니다.

```css
transition-duration : 시간；
```
> 시간 단위는 초(seconds) 또는 밀리초(milliseconds)입니다.

### transition-timing-^function 속성 - 트랜지션 형태 선택하기
 트랜지션 효과의 시작과 중간, 그리고 끝에서의 속도 곡선을 
선택합니다

```css
transition-timing-function: 속성 값;
```

* linear : 시작에서 끝까지 똑같은 속도로 트랜지션을 진행합니다.
* ease : 처음에는 천천히 시작하고 점점 빨라지다가 마지막엔 천천히 끝냅니다. 기본 값입니다. 
* ease-in : 트랜지션 시작을 느리게 합니다.
* ease-out : 트랜지션을 느리게 끝냅니다. 
* ease-in-out : 느리게 시작하고 느리게 끝냅니다

* cubic-bezier(n,n,n,n) : 직접 베지에 함수를 정의해서 사용합니다. 시에서 사용할 수 있는 값은 0에서 1   사이입니다.

### transition-delay 속성 - 지연 시간 설정하기
효과를 언제부터 시작할 것인지 정하는 지연 시간을 설정

```css
transition-delay: 시간;
```

### transition 속성 - 트랜지션 속성 한꺼번에 표기하기
 transition ■속성을 시'용하면 transtion-property오］" transition-duration, transition-timing- 
function, transition-delay 속성을한줄로 표기할수 있습니다.

```css
transition:property 값 |        duration 값 |        timing-function 값 |         delay 값;
```


## transition 속성

transition이 적용되는 부모요소에 적용합니다.



### Transition-property

어떤 속성에 트랜지션 효과를 줄 것인지를 지정합니다.

* transition-property: 속성1, 속성2; 와 같이 저장합니다.
* all 모든 속성을 지정합니다.
* none : 아무것도 지정하지 않습니다.



### transition-duration

트랜지션 효과를 몇 초 동안 실행할 것인지를 지정합니다.



### transition-delay

지정한 초 만큼 기다렸다가 실행할 때 사용합니다.



### transition-timing-function

트랜지션이 시작하면서 끝날때의 타이밍, 즉 속도를 지저아는 것입니다.

* linear
* ease-in
* ease-out



### transition

단축속성으로 여러 값을 한번에 설정합니다.


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














