---
layout: home
---

# 색상과 배경을 위한 스타일
글자에 색상을 넣거나 여러 요소에 배경을 사용할 수 있습니다.


## 색상과 관련된 스타일
웹 문서에서 가장 자주 바뀌는 속성은 글자나 배경등의 색상변경 입니다.  
> CSS3에서는 요소에 다양한 색을 변경할 수 있는 속성과 투명도까지 조절할 수 있는 기능도 같이 제공합니다.

### color 속성 - 글자색 바꾸기
글자색을 바꿀 때는 `color` 속성을 사용합니다.

```css
color: 색상값;
```

* 16진수 표기법
* rgb 표기법
* hsl 표기법
* 색상 이름 표기법

> 글꼴이나 글자 크기 등은〈body〉태그 선택자에서 지정하면 문서 전체에 상속이 되어 하위 요소 
에서 스타일을수정하지 않는한문서 전체에 똑같이 적용됩니다.


### 투명도를 조절하는 rgba와 hsla
CSS3에서는 기존의 방법과 달리 각 색상에 알파 
값을 더 추가해 rgba라는 방식을 사용할 수 있습니 다.

```css
rgba(red 값,  green 값,  blue 값,  alpha 값);
```

알파(alpha)가불투명도 값을 나타내는 것으로 0에서 1까지 값중에서 사용할수 있습니다.

1은 완전 불투명한 것이고, 0이 되면 완전히 투명해집니다

> 투명도를 표기할때는 `0.5` 대신 소수점 앞의 0을 빼고 `.5`라고 표기해도 됩니다.


## 배경색과 배경 이미지
배경색이나 배경 이미지를 설정할 수 있고，CSS를 사용하면 배경 이미지의 크기도 다 
양하게 설정할 수 있습니다.

### background-color 속성 - 배경색 지정하기
요소에 배경색을 지정하는 것입니다.

```css
background-color: 색상 값;
```

> background-color 값은 상속되지 않습니다.


### background-image 속성-웹요소에 이미지 넣기
배경 이미지 경로를 지정합니다

```css
background-丄mage :url （파일 경로h
```

배경 이미지 크기가 요소 크기보다 작을 경우 배경 이미지가 가로와세로로 반복하면서 요소를 가 
득 채우게 되는데

> 배경 이미지를 반복하고 싶지 않다면 `background-repeat` 속성을 이용합니다.


### background-repeat 속성 -  배경 이미지 반복하기


배경 이미지를 사용할 때 그 이미지를 반복할 것인지, 반복한다면 가로나 세로 중에 한 방향으로 
반복할 것인지, 아니 면 가로와 세로로 반복할 것인지 지 정하려 면 background-repcat 속성을 사용 
합니다.

> 반복되는 배경 이미지는 왼쪽 위나 왼쪽 아래 모서리부터 시작합니다

```css
background-repeat:속성 값;
```

* repeat : 브라우저 화면에 가득 찰 때까지 배경 이미지를 가로와 세로로 반복합니다 
* repeat-x : 브라우저 창 너비와 같아질 때까지 배경 이미지를 가로로 반복합니다.
* repeat-y : 브라우저 창 높이와 같아질 때가지 배경 이미지를 세로로 반복합니다. 
* no-repeat : 배경 이미지를 한 번만 표시하고 반복하지 않습니다.



### background-position 속성 -  배경 이미天| 위치 조절하기
배경 이미지를 한번만 표시하면서 배경 이미지를 원하는 위치에 배치하려고할때 유용합니다.
 

백분율(%) 표시법
```css
background-postion: 위치(%) 위치(%);
```

길이(px) 표시법

```css
background-image:길이(px) 길이(px);
```

키워드 표시법

```css
background-position: 키워드 키워드;
```
수평 위치 
* left
* center
* right 

수직 위치 
* top
* bottom
* center


### background-attachment 속성 -  배경 이미지 고정하기
문서 내용이 긴 경우에 스크롤 막대를 내려 내용을 확인하면 배경 
이미지도 함께 이동합니다

```css
background-attachment:fixed 또는 scroll;
```
> scroll이 기본 값입니다.

scroll은 내용과 배경 이미지가 함께 스크롤되는 것이고，

fixed는 배경 이미지가 고정된 상태에서 내용만 스크롤됩니다.


### background 속성 - 속성 하나로 사용하기
background-image오卜 background-repeat, background-position, background­ 
attachment 네 가지 속성을background라는 하나의 속성으로 줄여서 사용할수 있습니다.

```css
background: url (bg.jpg) no-repeat bottom right fixed;
```

### background-size 속성 -  배경 이미지 크기 조절하기
CSS3에서는 background-size 속성을 사용하여 배경 이미지 
를사용하는 요소에 따라여러 가지 크기로 사용할수 있습니다.

```css
background-size:속성 값;
```

* auto : 원래 배경 이미지 크기만큼 표시됩니다.
* 크기 값: 너비 값과 높이 값을 지정합니다. 너비 값만 지정할 경우 원래 배경 이미지 크기를 기준으로 축소/확대 배율을 계산해 높이 값을 자동 계산합니다.
* 백분율 : 원래 배경 이미지 크기를 기준으로 확대하거나 축소합니다.

* cover : 배경 이미지의 너비/높이 비율을 유지하면서 확대하거나 축소하는데. 너비나 높이 중 큰 값을 배경 이미지가 삽입되는 요소에 맞춥니다.

* contain : 배경 이미지의 너비/높이 비율을 유지하면서 확대하거나 축소하는데, 너비나 높이 중 작은 값을 배경 이미지가 삽입되는 요소에 맞춥니다.


```css
background-size：auto auto；
```


```css
background-size:300px;
```

```css
background-size:45% auto;
```

```css
background-size:contain;
```


### background-clip 속성 - 배경 적용 범위 조절하기
CSS3에는background-clip 속성이 있어서 배경 이미지나 배경색을 어디까지 적용할지 그 범위를 지정할수 있습니다.

```css
background-clip:속성 값;
```

박스 모델의 가장 외곽인 테두리(border)까지 적용할지，테두리를 빼고 패딩 
(padding) 범위까지 적용할지，그렇지 않으면 내용 부분에 만 적용할지 선택할 수 있습니 다

* border-box : 박스 모델의 가장 외곽인 테두리(border)까지 적용합니다. 
* padding-box : 박스 모델에서 테두리를 뺀 패딩(padding) 범위까지 적용합니다. 
* content-box : 박스 모델에서 내용 부분에만 적용합니다.


### background-origin 속성 - 배경 이미지 위치 기준 조절하기
background-origin 속성은background-position 속성을 이용해 배경 이미지를 원하는 곳에 배치 
하려고 할 때 어디를 기준으로 할 것인지 지정하는 것입니다. 

```css
background-or丄gin:속성 값;
```

* border-box : 박스 모델의 가장 외곽인 테두리(border) 기준 
* padding-box : 박스 모델에서 테두리를 뺀 패딩(padding) 기준 
* content-box : 박스 모델에서 내용 영역 기준


### 그러데이션 효과로 배경 꾸미기
색상 그러데이션을 사용해 배경을 꾸밀 수도 있습니다. 아직까지는 
그러데이션(gradation) 구문이 표준화되지 않아 브라우저 접두사를 함께 사용해야 합니다.


### 선형 그러데이션
선형 그러데이션은수직 방향이나 수평 방향으로，혹은 대각선 방향으로 색상이 일정하게 변하는 
것을 말합니다. 


```css
linear-gradient （각도또는위치,  color-stop, [color-stop,.. ]）;
```

### 원형 그러데이션
원 또는 타원의 중심에 
서부터 동심원을 그리며 바깥 방향으로 색상이 바뀝니다.

```css
radial-gradient(위치，모양(및크기),  color-stop, [color-stop... ])
```






