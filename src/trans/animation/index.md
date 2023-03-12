# CSS-animation

요소에 적용되는 CSS 스타일을 다른 CSS 스타일로 부드럽게 전환시켜 주는 것을 말합니다.



이때 CSS 스타일이 변화되는 중간지점을 `키프레임`이라고 합니다.

즉, `@keyframes`은 애니메이션의 중간 상태라고 할 수 있습니다.

에니메이션은 트랜지션보다 훨씬 더 규모가 크고 복잡합니다. 애니메이션은 다양한 능력을 가지고 있기 때문에 더 정밀한 효과를 구현할 수 있습니다.



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



