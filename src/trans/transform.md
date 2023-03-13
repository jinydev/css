---
layout: home
---

# Transform

transform 은 HTML 요소를 회전, 크기조절, 기울이기, 이동효과를 나타날때 사용합니다.

사용법은 transform 속성값을 특수한 함수로 넣어 주면 됩니다.



> 주의사항
>
> transform을 사용하기 위해서는 display 속성이 block 또는 inline-block 이어야 합니다.




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


## Transform 함수



### translate(tx,ty)

translate() 함수는 지정한 크기많큼 요소를 이동 시키는 동작을 수행합니다.



또는 한쪽 방향으로 이동도 가능합니다.

* translateX(tx)
* translateY(ty)





### scale(sx, sy)

지정한 크기만큼 x축과 y축으로 확대 또는 축소를 합니다.



* scaleX(sx)
* scaleY(sy)



### rotate(각도)

지정한 각도만큼 회전합니다. +는 시계방향, -는 반시계방향을 의미합니다.



* rotateX : x축을 기준으로 회전합니다.
* rotateY : y축을 기준으로 회전합니다.
* rotateZ : z축을 기준으로 회전합니다.

> 축을 기반으로 회전을 할때에는 `부모요소`에게 perspective 속성을 적용해야 합니다.
>
> ```css
> perspective: 50px;
> ```
>
> 



### skew(ax, ay)

지정한 각도만큼 x축과 y축으로 왜곡합니다.



* skewX(ax)
* skewY(ax)