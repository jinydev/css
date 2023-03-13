---
layout: home
---

# CSS-animation

요소에 적용되는 CSS 스타일을 다른 CSS 스타일로 부드럽게 전환시켜 주는 것을 말합니다.



이때 CSS 스타일이 변화되는 중간지점을 `키프레임`이라고 합니다.

즉, `@keyframes`은 애니메이션의 중간 상태라고 할 수 있습니다.

에니메이션은 트랜지션보다 훨씬 더 규모가 크고 복잡합니다. 애니메이션은 다양한 능력을 가지고 있기 때문에 더 정밀한 효과를 구현할 수 있습니다.




## 애니메이션 속성
animation 
속성을 이용하면 트랜지션보다 애니메이션을 더 쉽게 만들 수 있습니다.


### animation 속성과 transition 속성

animation 속성은 애니메이션에 소요되는 시간이나 지연 시간 등을 지정하는 것은 transition 속성 
과 같지만，애니메이션의 시작에서부터 끝날 때까지 어느 지점이든 ©keyframe 속성을 사용해 애 
니 메 이 션을 정 의할 수 있다는 점은 트랜지 션과 다릅니 다.


### animation-duration 속성 - 애니메이션 실행 시간
 애니메이션을 얼마 동안 재생할 것인지 설정합니다.


```css
animation-duration: Is;  /* 애니메이션 진행 시간 1초 */
```

### animation-name 속성
CSS로 애니메이션을 만들 때 @keyframes 속성을 이용해 여러 개의 애니메이션을 정의할 수 있는 
데，특정 요소에 어떤 애니메이션을 적용할 것인지 정의하는속성이 animation-name 속성입니다.


```css
/* 애니메이션 정의 */
animat丄on-name: 이름;  
```

### animation-iteration-count 속성 - 반복 횟수 지정하기
애니메이션은 기본적으로 한 번만 실행하고 끝납니다.

```css
animation-iteration-count: in社nite;   /* 애니메이션 반복 횟수 무제한 반복 */
```

### animation-direction 속성 - 애니메이션 반대 방향으로 실행하기
애니메이션이 실행되고 나면 기본으로 원래 위치로 돌아가지만

애니 메이션의 방향을 조절할 수 있습니 다.

```css
animation-direction: alternate;   /* 애니메이션 끝난 후 반대 방향으로 실행 */
```

### animation 속성 - 애니메이션 관련 속성 한꺼번에 표기하기
animation 속성을 사용하면 필요 
한 애니메이션 속성들을 한줄로 표기할수 있습니다.

```css
animation:name 값 | duration 값 | timing-function 값 | delay 값 | iteration-count direction 값;
```





## Keyframes 정의

`@keyframes`으로 에니메이션을 생성합니다.



from(시작)~to(끝) 를 이용한 애니메이션 shape 생성

```css
@keyframes shape {
    from {
        border: 1px solid transparent;
    }
    
    to {
        border: 1px solid #000;
        border-radius:50%;
    }
}
```



from(시작)~{percent}-to(끝) 를 이용한 애니메이션 background 생성



```css
@keyframes background {
    from {
        background-color:red;
    }
    
    50% {
        background-color:green;
    }    
    
    to {
        background-color:blue;
    }
}
```





## animation 속성



animation-name

에니메이션의 중간 상태를 지정하기 위한 이름을 정의합니다. 중간상태는 `@keyframes` 규칙을 이용하여 기술합니다.



```css
animation-name:shape;
@keyframes shape {
    
}
```



animation-duration

한 싸이클의 애니메이션이 얼마에 걸쳐 일어날지 지정합니다.



animation-delay

엘리먼트가 로드되고 나서 언제 애니메이션이 시작될지 지정합니다.



animation-iteration-count

애니메이션이 몇 번 반복될지 지정합니다. infinite로 지정하여 무한히 반복할 수 있습니다.



animation-pay-state

애니메이션을 멈추거나 다시 시작할 수 있습니다.



animation-timing-function

중간 상태들의 전환을 어떤 시간 간격으로 진행할지 지정합니다.



animation-fill-mode

애니메이션이 사직되기 전이나 끝나고 난 후 어떤 값이 적용될지 지정합니다.



animation

`animation-*`들의 단축 속성으로 한꺼번에 작성이 가능합니다.



