---
layout: home
--- 

# border 영역

## border

컨덴츠와 패딩영역을 깜싸고 있는 외각선을 말합니다.

css로는 border, border-width, border-style, border-color 를 지정할 수 있습니다.



### border-style

테두리의 스타일을 어떻게 만들 것인지를 지정합니다.

```css
border: solid;
```

한개의 속성값을 지정하는 경우, 박스의 4면이 모두 동일한 형태의 선으로 출력됩니다.



만일, 각각의 면마다 다른 스타일로 지정을 하고자 할때에는, 여러 속성인자를 선언합니다.

```css
border-style: dotted solid dash solid;
```

속성이 적용되는 순서는 위->오른쪽->하단->좌측 순으로 반영됩니다.



또는 각각의 위치를 지정하는 속성을 통하여 외각선을 설정할 수 있습니다.

```css
border-left-style: solid;
```



### border-width

외각선의 두께를 지정합니다. 크기값 또는 thin, medium, thick 과 같은 키워드를 이용하여 지정을 할 수 있습니다.

```css
border-width:1px;
border-width: thin;
```



각각의 면에 대해서 다른 크기를 지정 할때에는 여러 값을 지정합니다.

```css
border-width: 1px 2px 4px 6px;
```



또는

```css
border-left-width:2px;
```



### border-color

외각선의 색상을 지정합니다.

```css
border-color: blue;
```



### 단축속성 border

단축 속성은 border-width, border-style, border-color를 단축하여 속성을 부여하여 사용할 수 있다.

즉, 테두리 두께, 스타일, 색상을 한번에 표기할 수 있습니다.



```css
border: 1px solid red;

border-right: 3px solid cyan;
```



### 라운드

테두리의 꼭지점을 둥글게 만듭니다.



```css
border-radius: 30px;
border-radius: 10% 20%;
```



> 동그란 모양을 만들때는 raduis 값을 50%로 적용합니다.





### box Sizing

`box sizing` 속성은 HTML 요소의 너비와 높이를 계산하는 방법을 지정합니다.

CSS 박스 모델에서 너비와 높이는 컨덴츠의 크기에 따라 적용됩니다. 그리고 여백과 외각선을 추가하게 되면 박스의 크기가 커지게 됩니다. 즉, 외각선의 굵기 만큼 컨덴츠의 크기가 커지게 됩니다.



* content-box : 기본적인 CSS 박스 크기 결정 방법입니다.



* border-box : 테두리와 안쪽의 여백을 박스크기에 고려 합니다. 테두리를 포함하여 크기를 유지해 줍니다.

  > boerder + padding+ content = width 크기로 유지합니다.

