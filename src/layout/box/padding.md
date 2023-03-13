---
layout: home
---

# 박스 Padding 속성
content와 border 사이의 영역으로 안쪽 여백 입니다.


## padding 속성 및 작성방법
`padding` 속성을 이용하여 전체 박스에 동일한 내부 여백을 추가 가능합니다.

```css
padding : 10px;
```

 

## 각각의 영역에 분리하여 적용

패딩을 상/하/좌/우 를 분리하여 적용하고자 할때에는 확장된 속성값을 사용합니다.

* padding-top
* padding-bottom
* padding-left
* padding-right



### 단축지정
`padding` 속성에 값을 2개를 주어 상/하 , 좌/우 를 구분하여 입력이 가능합니다.

```css
padding : 상하 좌우;
```

각각지정

`padding` 속성에 값을 4개를 주어 상, 우, 하 , 좌 를 구분하여 입력이 가능합니다. 시계방향으로 여백이 주어지게 됩니다.

```css
padding : 상 우 하 좌 ;
```


### padding 속성    - 콘텐츠  영역과  테두리   사이   여백   설정하기

패딩(padding)이란콘텐츠 영역과 테두리 사이의 여 
백을 말합니다. 테두리 안쪽의 여백이라고 생각하면 됩니다.

```css
padding-top:속성 값;
padding-right: 속성 값;
padding-bottom:속성 값;
padding-left:속성   값;
```

또는 한번에 지정도 가능합니다.

```css
padding:속성   값;
```


## 테두리  관련  속성들
요소에 테두리   두께，테두리  스타일, 그리고  테두리   색상 등을 지정합니다.


### border-width 속성   - 테두리   두께   지정하기

속성들은순서대로 위쪽, 오른쪽，아래쪽，왼쪽 
의 테두리 두께를 지정하는데，일반적으로 테두리 두께는 일정하게 하기 때문에 border-width 속 
성을 이용해서 한꺼번에 지정합니다.

```css
border-width: 키워드   |     크기   값;
```

* thin : 얇은  선을  그립니다.
* medium : 보통  선을  그립니다   기본  값입니다.
* thick : 굵은  선을  그립니다.
* 크기 : 테두리 굵기를 직접 지정합니다.


### border-color 속성  - 테두리   색상  지정하기
테두리의 색상을 지정합니다.

> border-color 속성만사용해서는 화면에서 결과를확인할수 없고，border­ 
width 속성과border-style 속성을 이용해 미리 테두리 두께와색상이 결정되어 있어야합니다.

```css
border-color:속성값;
```

* 색상  값 : 색상  이름이나   16진수  값. rgb 값  등을  이용하여   색상을  지정합니다.
* transparent : 투명하게   나타납니다. 기본   값입니다.


### border-style 속성   一      테두리선   스타일   지정하기
 테두리의 스타일을 지정합니다.

```css
border-style:속성값;
```

* none        
* hidden
* dotted
* dashed
* solid
* double
* groove
* ridge
* inset
* outset

### border 속성   - 테두리   스타일   묶어서   지정하기
스타일을 한꺼번에 묶어서 지 정할 수 있습니다. 
> 두께와 색상, 스타일의 순서는 상관없습니다.


## CSS3 박스 관련  속성들
CSS3에 박스 모델과 관련된 여러 속성이 추가되었습니다. 
CSS만으로도 멋진 박스 효과를 만들수 있습니다.


### border-radius 속성    - 박스  모서리   둥글게   만들기
박스의 모서리 부분을 손쉽게, 그리고 다양한 
형태로 처 리할수 있습니다.

```css
border-radius : 속성   값;
```

* 크기 : 둥글게   처리할  반지름  크71를  pxO |나  em  같은   단위와  함께  수치로  표시합니다. 

* 백분율(%) : 현재  요소의  크기를   기준으로  둥글게   처리할  반지름  크기를  %로   지정합니다.


### border-*-radius 속성 一  박스 모서리 다르게 지정하기


```css
border-*-radius :속성 값;
```

가로, 세로 비율 다르게 지정

```css
border-radius : 가로 값 / 세로 값;
```




## CSS 여백 설정하기
---
css에서 여백을 설정하는 방법은 크게 2가지가 있습니다.
안쪽 여백은 padding, 바깥쪽 여백은 margin 이라고 합니다.

### 안쪽 여백 Padding
여러개의 값이 설정될 때에는 스페이스로 한칸씩 뛰어 주어야 합니다.

* 1개: 상하좌우
모두 동일한 값으로 padding을 선택할때에는 하나의 설정값만을 입력합니다.

```css
div {
    padding: 10px;
}
```

* 2개: 상하/ 좌우
동일한 값의 위아래와 동일한 값의 좌우를 설정할때는 2개의 설정값을 입력합니다.

```css
div {
    padding: 30px 10px;
}
```
첫번째 값은 위/아래를 의미 합니다. 두번째 값은 좌/우를 의미 합니다.

* 3개

```css
div {
    padding: 30px 10px 5px;
}
```
첫번째 값은 상단,
두번째 값은 좌/우,
세번째 값은 하단

* 4개
시계방향으로 설정값이 적용이 됩니다.

```css
div {
    padding: 10px 20px 30px 40px;
}
```

상단 10px
오른쪽 20px
하단 30px
왼쪽 40px

#### 한방향 설정

padding-top
padding-bottom
padding-left
padding-right