---
layout: home
---

# 변형 스타일
요소를 옮기거나 크기를 조절하고 회전시키는 등 변형 작업

## 변형(transtorm)
웹 요소의 위치를 옮기거나 크기를 조절하고 회전，왜곡시키는 것을 변형(transform)이라고 합니다.

### 2차원，3차원 좌표계
수평이나 수직으로 옮기는 것은 x축과 y축으로 이동하는 것이기 때문에 2차원 좌표에서 실행하는 일이고，
원근감을 추가하면 z축에서 앞뒤로 이동하는 것이므로 3차원 좌표계에서 실행합니다.

### transform 속성 - 웹 요소 변형하기
요소를 변경하려면 `transform`속성에 원하는 변형 함수를 함께 사용합니다.

```css
transform: 변형함수 값;
```

요소 이동함수를 이용하는 예제
```css
/* x축으로 50px，y축으로 100px 이동*/
transform: translate ( 50px,   lOOpx) ;   
```
`translate()` 함수를 이용하여 요소를 이동합니다.

transform는 다양한 변형 함수를 지원합니다.











### translate - 요소  이동시키기
요소가 지정한 크기만큼 이동합니다.

```css
transform:translate(tx, ty)
transform:translate3d(txz ty, tz)
transform:translatex(tx)
transform:translateY(ty)
transform:translateZ(tz)
```

* translate(tx, ty) : 지정한 크71만큼 수평과 수직으로 이동합니다
* tranlsate3d(tx, ty, tz) : 지정한 크기만큼 수평과 수작 앞뒤로 이동합니다.
* translateX(tx) : 지정한 크기만큼 수평으로 이동합니다. 
* translateY(ty) : 지정한 크기만큼 수직으로 이동합니다. 
* translateZ(tz) : 지정한 크기만큼 앞뒤로 이동합니다.

>  transform 속성은 아직까지 완벽한 표준이 정해지지 
않았기 때문에 속성 이름 앞에 -webkit-나 -moz- 같은브라우저 별 접두사를붙여야합니다.


### scale - 요소확대/축소하기
지정한 크기만큼 확대/축소합니다.

```css
transform:scale(sx, sy)
transform:scale3d(sx, sy, sz)
transform:scaleX(sx)
transform:scaleY(sy)
transformrscaleZ(sz)
```

* scale(sx, sy) : 지정한 크기만큼 수평과 수직으로 확대/축소합니다
* scale3d(sx, sy, sz) : 지정한 크기만큼 수평과 수작 앞뒤로 확대/축소합니다.
* scaleX(sx) : 지정한 크71만큼 수평으로 확대/축소합니다. 
* scaleY(sy) : 지정한 크기만큼 수직으로 확대/축소합니다. 
* scaleZ(sz) : 지정한 크기만큼 앞뒤로 확대/축소합니다.


### rotate - 요소회전하기
지정한각도만큼 웹 요소를 회전합니다.

```css
transform:rotate（rx, ry,  각도）
transform:rotate3d（rx, ry, rz, 각도》
transform:rotateX（각도》
transform:rotateY（각도》
transform:rotateZ（각도）
```

* rotate(rx, ry, 각도) : 지정한 각도만큼 수평과 수직으로 회전합니다 
* rotate3d(rx, ry, rz, 각도): 지정한 각도만큼 회전합니다.

* rotateX(rx, 각도》: 지정한 각도만큼 수평으로 회전합니다
* rotateY(ry, 각도》: 지정한 각도만큼 수직으로 회전합니다.
* rotateZ(rz, 각도) : 지정한 각도만큼 앞뒤로 회전합니다


### skew - 요소를  비틀어   왜곡하기
skew 변형은 지정한 각도만큼 요소를 비틀어 왜곡합니다.


```css
transform: skew （각도，각도》
transform: skewX （각도》
transform :skewY （각도）
```

* skew(x각도，y각도》: 지정한 각도만큼 수평과 수직으로 왜곡합니다.
* skewX(x각도》: 지정한 각도만큼 수평으로 왜곡합니다.
* skewY(y각도》: 지정한 각도만큼 수직으로 왜곡합니다.

## 변형과 관련된 속성들
변형할 때 기준이 되는 원점을 바꾸거나 요소의 원 
근감을 표현하거나，또는 요소의 뒷면을 표시하는 등 여러 속성을 함께 사용하면 더 많은 효과를 만들 수 있 
습니다.

### transform-origin 속성 -  변형 원점 설정하기
변형 원점을 설정

```css
transform-orgin: x축 y축 x축;
```

* X축 : 원점에서의 X 좌푯값으로, 길이 값이나 백분율, left, center, right 중에서 사용할 수 있습니다. 
* y축 : 원점에서의 y 좌푯값으로 길이 값이나 백분율. top, center, bottom 중에서 선택할 수 있습니다. 
* z축 : 원점에서의 z 좌푯값으로, 길이 값만 사용할 수 있습니다




### perspective - 원근감표현하기
perspective 속성은 잡아당기거 나밀어내어 원근감을갖게 합니다.

```css
perspective:속성 값;
```

### perspective-origin 속성 - 원근감 조절하기
perspective 속성과 함께 사용 합니다. 3D요소의 bottom 부분의 위치를 지정하는데，좀 더 높은곳에서 원근 
을 조절하는 듯한 느낌을 만들 수 있습니다

```css
perspect丄ve-or丄gin:x축 값 |    y축 값;
```

* x축 :
3D 요소가 x축에서 어디에 위치하는지 지정합니다 사용할 수 있는 값은 길이 값이나 백분율. 
left, right, center, top, bottom 입니다. 기본 값은 50%입니다.


* y축 : 
3D 요소가 노축에서 어디에 위치하는지 지정합니다. 사용할 수 있는 값은 길이 값이나 백분율,
top, center, bottom입니다. 기본 값은 50%입니다

    
### transform-style 속성 - 3D 변형 적용하기
변형이 적용된 요소의 하위 요소 
에 3D 변형을 적용할 것인지 결정합니다.

```css
transform-style:속성 값;
```


* flat : 하위 요소를 평면으로 처리합니다.
* preserve-3d : 하위 요소들에 3D 효과를 적용합니다.

> transform-style 속성은 아직까지 혭키트 계열의 브라우저（크롬과 사파리）에서만 지원하고 있습니다.

### backface-visibility 속성 - 2소의 뒷면 표시하기
요소의 뒷면，즉 반대쪽 면을 표시할 것인지를 결정하는 것입니다. 

```css
backface-visibility:속성 값;
```

* visible : 뒷면을 표시합니다. 
* hidden : 뒷면을 표시하지 않습니다.



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




