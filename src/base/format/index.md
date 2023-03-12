---
layout: home
---

# 스타일 형식
웹 문서에서 자주 사용하는글꼴이나 색상，텍스트와 이미지를 어떻게 배치할 것인지 등의 규칙을모아놓은 것이 스타일입니다.


## CSS 표현
---
CSS 는 `선택자`와 `속성` 및 `값`으로 구성됩니다. 작성방법은 다음과 같습니다.

```css
선택자 { 속성:값; }
```

선택자 뒤에는 속성과 값을 `{`와 `}`로 감싸서 표현을 합니다. 이를 CSS 블럭이라고 말합니다.
> `{}`는 코드의 블럭을 표현하는 기호 입니다.

속성과 값을 구분할 때에는 사이에 콜론`:`을 삽입합니다. 또한, 마지막에는 세미콜론`;`이 위치합니다.

다음은 문단 `<p>`테그에 글자 속성을 부여하는 예제 입니다.
```css
p {
    color:red;
}
```


## 선택자
CSS 표현에서 선택자는 html 요소를 가리킵니다. 요소의 선택은 테그명 또는 속성명등을 결합하여 선택이 가능합니다. 
제일 많이 사용하는 속성명은 클래스 입니다.

* 테그
* `.` : 클래스 선택
* `#` : id 선택

> css는 지정한 선택자와 일치하는 모든 HTML 요소를 찾아 style 속성을 부여 합니다.


## 속성과 값
선택자 다음에는 대괄호가 있고，그 안에는 속성과속성 값이 옵니다. 
하나의 속성은 하나의 값만을 가지게 됩니다. 만일 선택된 요소에 여러개의 속성을 부여하고자 할때에는 세미콜론 `;`을 통하여
구분을 합니다.

```css
h2 {
    font-size:20px; color:purple;
}
```

> CSS는 공백을 무시합니다.   

코드의 가독성을 위하여 한줄로 길게 쓰는 것보다는 다음줄에 걸쳐 보기 좋게 작성을 합니다.

```css
h2 {
    font-size:20px; 
    color:purple;
}
```


## CSS의 주석
CSS에서 주석을 표시할 때는 `/*`와 `*/` 형태로 지정된 블럭을 모두 주석으로 처리 합니다.












## 다양한 모양의 스타일 적용방식
---
스타일은 모두 동일 하지 않습니다. 운영체제, 브라우저 등에 따라서 다르게 스타일이 적용되어 있습니다.

### 운영체제 스타일
테스크탑 운영체제별로 다르게 적용되는 스타일을 말합니다.

### 브라우저 스타일
브라우저마다 적용되는 스타일의 모양이 다르다.

### 사용자 스타일
사용자가 브라우저, 운영체제등의 `설정`을 직접 변경하여 적용하는 스타일을 말합니다.
글씨의 크기를 크게 하거나, 색맹, 시각등의 장애를 가지고 있는 사람들이 많이 이용을 합니다.

### 제작 스타일
사이트를 만드는 사람이 스타일을 변경하는 것을 말합니다.

<br>




## 제작 스타일
---
개발자가 스타일을 변경할 수 있는 방법은 크게 4가지가 있습니다.

### 인라인 스타일(inline Style)
html 요소에 직접 CSS를 지정하는 것을 말합니다.

```html
<p style="color:red">안녕하세요</p>
```

### 임베디드 스타일(Embedded Style)
html 문서의 head 영역에 삽입을 하는 스타일 적용 방식을 말합니다.
`<style>` 테그를 삽입하여 스타일을 지정합니다.

```html
<html>
    <head>
        <style>
            p {
                color:red;
            }
        </style>
    </head>
    <body>
        <p>안녕하세요</p>
    </body>
</html>
```

임베디스 스타일은 현재의 `작업중인 문서`에만 적용이 됩니다.

> 임베디스 스타일은 여러개의 웹문서를 제작할때 일괄적인 수정이 어렵다는 단점이 있습니다.
> 유지보수, 운영에 어렵습니다. 페이지의 디자인을 테스트 할때 많이 사용을 합니다.

### 링크드 스타일(Linked Style)
별도의 스타일시트 파일(*.css)을 생성하여 링크를 영결하는 것입니다.

```html
<link rel="stylesheet" type="text/css" href="default.css">
```

> 실무에서 가장 많이 사용하는 스타일 적용방식입니다.
> 외부 파일로 정의되어 있기 대문에 다수의 페이지에 일괄 수정하기 용이합니다.

### 삽입 스타일(Import style)
css 선언안에 추가 css를 적용할때 유용합니다.

```css
<style>
    @import url('default.css');
</style>
```

<br>

## CSS의 우선순위
---
CSS는 선택자가 있습니다.

선택자에 따라서 우선적으로 적용되는 점수가 있습니다.


### 0. 전체 선택자 `*`
전체 선택자는 모든 요소를 선택합니다.

```css
* {
    color:red;
}
```

전체 선택자를 지정하여 스타일이 적용되면, 모든 요소들의 스타일이 변경을 하게 됩니다.

### 1. 타입 선택자
html의 테그 요소를 선택합니다.

```css
div {
    color:red;
}
```

### 10. 클래스 선택자, praise 클래스 선택자
특정 요소에 이름을 부여합니다. 클래스를 통하여 부여한 이름을 통하여 선택자를 사용합니다.

```css
.aa {
    color:blue;
}
```

```html
<div class="aa">안녕하세요</div>
```


### 100. id 선택자
`id`를 통하여 부여된 이름을 선택자로 사용을 합니다.
id로 부여된 이름은 `#`기호로 사용을 합니다.


```css
.bb {
    color:orange;
}
```

### 1000. 인라인 스타일
테그 요소에서 직접 스타일을 지정을 하는 방법입니다.

```html
<div style="color:gray">안녕하세요</div>
```

### 절대 최고값, !important
위의 모든 우선순위를 무시하고 적용하는 초고 우선순위를 말합니다.
우선순위를 무시합니다.

```css
* {
    color:red !important;
}
div {
    color:blue;
}
```


`*` 보다 우선순위가 높은 div 테그의 스타일이 적용되어야 하나, `!important`로 인하여 우선순위가 낮은 `*` 선택자가 적용되는 것을 확인할 수 있습니다.

> `!important`는 세미콜론 안쪽에 넣어 줍니다.




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

<br>

### 마진
바깥쪽 여백을 의미합니다.

* 1개 : 전체

* 2개 : 상하/좌우

* 3개 : 상 / 좌우 / 하

* 4개 : 위쪽 / 오른쪽 / 하단 / 왼쪽


#### 한방향 설정
margin-top
margin-bottom
margin-left
margin-right



## margin: 0 auto
`블록요소`의 성격을 가지는 요소를 중앙에 배치할때 사용을 합니다.

```css
div {
    margin: 0 auto;
}
```


## 박스모델
모든 요소들은 사각형의 형태를 가지고 있습니다.


### 박스의 크기

```css
div {
    width: 100px;
    height: 100px;
}
```

가로 세로 100px의 박스 크기가 됩니다.

### padding 추가
박스에서 패딩 설정시 박스의 크기는 padding 설정값 많큼 `크게` 됩니다.

```css
div {
    width: 100px;
    height: 100px;

    padding: 20px;
}
```

패딩이 추가돠어 가로 세로 140px 의 크기가 됩니다.

> 실제 박스의 크기를 동일하게 하기 위해서는 가로사이즈 - 안쪽여백 = 현재 사이즈


### margin 추가
마진은 바깥쪽 여백으로 박스 `사이즈의 크기 변화는 없습니다`. 하지만, 마진으로 인하여 박스의 위치가 틀어지게 됩니다.

```css
div {
    width: 100px;
    height: 100px;
    padding: 20px;

    margin: 50px;
}
```

<br>

### 선 추가
박스모델에서 선이 추가 되면, 선의 굵기 많큼 박스의 크기가 커지게 됩니다.

## box-sizing
박스의 크기를 자동으로 계산해 줍니다.
css3에서 추가된 기능입니다. ie7 이하에서는 지원하지 않습니다.

```css
box-sizing:border-box;
```

<br>

## position
요소의 위치를 이동합니다.

### static 
기본값으로 요소의 좌표를 이동할 수 없습니다.

```css
div {
    position: static;
}
```

객체의 위치를 초기화 할때 사용합니다.

### relative
요소를 상대적 위치로 이동을 합니다.

```css
div {
    position: relative;
}
```

> 예제코드: relative01.html
relative 속성이 부여되었다고 해서 현재의 위치에 아무런 변화가 없습니다.

### 위치이동
요소의 위치속성을 relative로 설정한 후에는 좌표의 이동이 같이 해주어야 합니다.
위치의 이동은 상하좌우 4방향으로 이동을 할 수 있습니다.
* top
* left
* right
* bottom

> 예제코드: relative02.html

`기존의 위치`로 부터 이동을 합니다.

> 위치이동은 상위 요소가 position 속성값이 없는 상태에서는
적용이 되지 않습니다.



### absolute
절대위치로 요소를 이동합니다.
만일, 절대위치를 적요한 요소의 상위요소가 relative가 되면,
relative 요소를 부모로 하여 기준좌표가 변경이 됩니다.

```css
div {
    position: absolute;
}
```

> 예제코드: absolute01.html

절대좌표가 적용되면, 요소는 레이어와 같이 중간에 뜬 상태가 됩니다.
따라서 위의 `~`과 아래 `~`이 같이 붙여져서 표현을 하게 되고.

위치를 이동할 수 있습니다.
기준점은 `브라우저`의 상단 좌측 입니다.


### fixed
요소를 브라우저의 특정위치에 고장하는 것을 말합니다.

relative와 absolute는 웹페이지를 기준으로 배치를 합니다.
반면에 fixed는 모니터의 브라우저 화면을 기준으로 고정배치를 합니다.





## 상호관계
relative와 absolute 와의 관계를 실습합니다.

> 예제코드: position41.html

absolute 속성을 이용하여 위츠를 이동해 봅니다.
> 예제코드: position42.html

브라우저의 기준으로 파란색 박스가 이동한 것을 볼 수 있습니다.

상위 div 요소에 relative 속성을 부여합니다.
> 예제코드: position43.html

바디 요소의 설정많큼 박스가 움직이게 됩니다.
상위 박스가 relative가 되면, 하위 absolute의 기준점은 상위 박스가 됩니다.

<br>

## z-index
요소가 겹쳐져 있을때 화면에 보이는 순서를 변경할 수 있습니다.

예를 들어 여러개의 요소들이 절대값으로 인하여 동일한 위치에 있을경우
마지막에 있는 요소만 보이게 됩니다.

이를 순서를 변경하기 위해서는 z-index 옵션을 사용해 주어야 합니다.


```css
z-index:숫자;
```

<br>

## 위치 실습
---

### 정 가운데 박스 그리기

* margin을 이용하여 위치 보정하기

```css
margin: -px 0 0 -px;
```


### margin 으로 박스 이동하기
margin은 바깥쪽 속성으로 값 지정시 요소의 위치를 이동하게 됩니다.

`+`값은 오른쪽으로 이동을 하며, `-`는 왼쪽으로 이동을 하게 됩니다.

만일, 요소가 다른 요소의 위치에 영향을 주는 경우에는.
마진 변경으로 같이 이동을 하게 됩니다.

### relative 이동
maring은 다른 요소에 영향을 주면서 위치를 이동합니다.
반면에 relative 속성을 이용하여 이동을 하게 되면, 다른 요소에는 영향을 주기 안고 해당 요소만을 이동을 할 수 있습니다.



## float
---
`블럭`의 속성을 가지는 요소들을 배치합니다.
float은 요소를 정렬하기 위해서 사용을 합니다.
float의 요소값은 다음과 같이 3가지가 있습니다.

* left
* right
* none

> 예제코드 : float01.html

위의 예제코드와 같이 ul/li 요소는 한줄단위로 출력됩니다.
li는 블럭 요소를 가지고 있기 대문 입니다.

### left

float 속성을 이용하여 한줄로 표시를 합니다.

> 예제코드 : float02.html
요소들이 왼쪽을 기준으로 순차적으로 배치됩니다.


### right
right는 오른쪽 부터 요소를 배치하게 됩니다.
첫번째 요소가 가장 오른쪽에 배치를 하기 때문에, 순서가 역순으로 배치되는 것을 확인 할 수 있습니다.

> 예제코드 : float03.html

보정하기
li의 요소는 순차적으로 배치를 하고, ul 요소를 float으로 하여 오른쪽으로 배치를 할 수 있습니다.

> 예제코드 : float04.html


## 폰트 스타일
---

### font-family
서체를 의미 합니다. 

만일 `돋움` 서체를 적용하고자 할때에는 다음과 같이 선언을 할 수 있습니다.
```css
font-family: dotum;
```

많이 사용하는 폰트로는 돋움, 굴림, 나눔고딕을 많이 사용합니다.

하지만 나눔고딕의 경우 운영체제에서 기존 제공하는 폰트가 아니라서
외부 웹폰트를 통하여 적용하여야 합니다.

영문 폰트는
verdana, tahoma, arial, 등이 많이 사용이 됩니다.

### font-size
글씨의 크기를 조정할 수 있습니다.

```
font-size:12px;
```

`데스크탑`용 웹사이트는 11px, 12px을 많이 사용을 하였으나,
`모바일`등 웹 `점근성`을 위해서 최근에는 14px을 많이 사용하는 추세 입니다.

* em
* pt
* px
* %

4가지의 단위를 많이 사용합니다.

### font-weight
폰트의 굵기를 설정합니다.

```css
font-weight: bold;
```

* bold
* normal

퐅트를 굵게 표시하는 요소들
th, strong, b, h1~h6
는 굵은 폰트로 처리를 합니다.
<= 이러한 요소들을 강제로 weight를 변경할 수 있습니다.


### text-align
`텍스트` 또는 `inline` 요소, `inline-block` 요소를 x축 기반으로 중앙 정렬을 할 수 있습니다.

`블럭` 요소는 가운데 정렬을 할 수 없습니다.

* left
* right
* center
* justify

### vertial-align
인라인, 텍스트 세로 정렬이 가능합니다.

* middle
* top
* bottom

#### 테이블 적용
테이블 td에서 텍스트가 적용될때 vertial-align 을 적용할 수 있습니다.
테이블은 기본값은 middle 입니다.


### color
색상을 변경합니다.

#### 색상값


## clear
float 속성의 영향을 해제 합니다.

> 예제코드 : clear01.html

이전에 float 설정한 li외에 이후의 div 요소에도 float 속성이 적용된 것을 볼 수 있습니다.

float은 지정한 속성외에 다음 요소에도 영향이 미치게 됩니다.
이를 해결을 하기 위해서는 clear 속성을 주어야 합니다.

```css
div {
    clear:both;
}
```

> 예제코드 : clear02.html

div는 float 속성이 해제되어 다음줄에 위치한 것을 볼 수 있습니다.

레이아웃 배치시 float 속성의 영향으로 위치가 틀어지는 경우가 발생합니다.


float 속성이 적용되면, 높이가 0이 되어집니다.


### 가상 선택자를 통한 clear 속성
float 속성을 해제하기 위해서 가상선택자를 이용합니다.

> 예제코드 : clear04.html

```css
선택자:after {
    content:"";
}
```

가상선택자 after는 요소의 뒤에 추가되는 내용 또는 속성을 말합니다.

content
요소뒤에 추가 내용을 넣어 줍니다. content는 inline 요소와 비슷합니다.
content는 가상의 span 과 같은 요소가 추가되는 것과 같습니다.

인라인 요소는 `clear:both`가 적용되지 않습니다. 따라서, content 를 블럭 요소로 변환을 해주어야 합니다.


```css
선택자:after {
    content:"";
    display:block;
    clear:both;
}
```

clear 클래스를 미리 만들어 놓고, 다중클래스 선택자를 이용하여 사용을 하면 편리 합니다.

```css
.clear:after {
    content:"";
    display:block;
    clear:both;
}
```

## 배경(background)

### 배경이미지

```css
background-image:url(이미지);
```


```css
background-repeat:no-repeat;
```

* repeat : 반복허용
* repeat-x : 가로만 반복허용
* repeat-y
* no-repeat

### 배경색
```css
background-color: 색;
```

### 배경위치 변경
```css
background-position:위치
```

* right
* top
* left
* bottom
* center

background-position: rigth top
background-position: rigth bottom
background-position: center top

정가운데 위치
background-position: center

숫자값으로 지정

```css
background-position: 10px 10px
```
죄측 상단을 기준으로 떨어진 x, y 값에 배치를 합니다.

`%`를 통하여 지정할 수 있습니다.
```css
background-position: 10% 10%
```

한번에 정의하기

`background` 속성명 뒤에 여러 값을 순차적으로 나열을 하면 됩니다.

```css
div {
    background: url(img.png) no-repeat 20px center #ccc;
}
```

## 텍스트 스타일

### 줄간격
`line-height` 속성은 여러 텍스트의 줄간격을 지정합니다.

줄간격은 텍스트의 중심선을 기준으로 간격을 처리합니다.

### 들여쓰기
기본값은 0 입니다.

text-indent:10px

### 자간
letter-spacing:0;
기본값은 0 입니다.

### 꾸밈
text-decoration

* overline
* none
* line-through

밑줄이 있는 a 링크의 밑줄을 삭제 할때 자주 사용을 합니다.


## display 속성
요소가 보여지는 속성을 변경합니다.

* block : 블럭요소로 변경합니다.
* inline : inline 요소로 변경합니다.
* inline-block : 블럭과 인라인을 모두 적용합니다. 한줄표시와 여백설정이 가능합니다.
* none : 화면에서 표시를 제외합니다. 화면 낭독기에서 읽지 않습니다.

ex) span 테그는 인라인 속성을 가지고 있기 대문에, width와 height가 적용되지 않습니다.

> 예제코드 : display0.html

이를 변경하기 위해서는 display 속성을 block으로 변경해 주어야 합니다.

> 예제코드 : display1.html

### inline 요소로 변경하기
div와 같이 블록 요소를 display:inline 으로 변경할 수 있습니다.

> 예제코드 : display2.html


### inline-block
`인라인` 속성과 `블럭` 속성 두가지를 가지고 있습니다.


### none
화면에서 제거를 합니다.



## overflow
정해진 영역에 초과하는 데이터가 있을 경우 처리하는 방법입니다.

### visible
기본값 입니다.

```css
overflow:visible;
```

요소의 크기가 넘어가도 허용하여 출력합니다.
예제코드 : overflow0.html

### hidden
넘아 가는 부분을 표시 하지 않습니다.

```css
overflow:hidden;
```

예제코드 : overflow1.html

### auto
초과되는 내용이 있을 경우 스크롤을 생성합니다.


```css
overflow:auto;
```

예제코드 : overflow3.html

이전에는 overflow auto와 같은 결과물을 생성하기 위해서
iframe을 많이 사용을 하였습니다.

오버플로우 auto값을 적용하기 위해서는 width 또는 height 가 `반드시 존재`햐야 합니다.


오버플로우 스크롤은 기본적으로 `키보드 컨트롤(page up/down)`이 불가능합니다.
키보드 컨트롤을 가능하게 하기 위해서는 tabindex 속성을 이용하여 처리 합니다.

```html
<div tabindex="0">
내용....
</div>
```

tabindex는 `tab`키 입력시 선택되는 순서 입니다. 탭 키를 입력하면 포커스가 이동하여 선택 진입이 되기 때문에 키보드 컨트롤이 가능하게 됩니다.
단, 크롬은 지원하지 않고 ie만 지원을 합니다.


## CSS 선택자
요소를 선택하기 위한 선택자에 대해서 알아 봅니다.

### 자손 선택자
요소와 요소 사이를 스페이스 공백으로 구분하여 선택을 합니다.

```
요소1 요소2 {

}
```

자손은 모든 `요소1`에 속한 모든 `요소2`를 선택합니다.


### 자손선택 스패이스 공백

```
요소 클래스 {

}
```

요소 안에 있는 클래스 이름을 가지는 요소를 선택합니다.



### 요소와 클래스명이 두개가 일치하는 선택


```
요소.클래스 {

}
```

예)
```html
<div class="aaa">

</div>
```

```
요소#아이디 {

}
```

### 쉼펴(,)
쉼표는 and 성격의 요소를 선택합니다.
두개 이상의 요소를 동시에 선택할 수 있습니다.

```
div, p {

}
```
div 와 p 요소를 모두 선택합니다.


### 선택응용1

```
요소1.클래스 요소2#아이디 {

}
```


```html
<div class="div">
    <p id="name"></p>
</div>
```


### 형제 선택자

요소 + 요소


```html
<style>
    div + div {
        color:red;
    }
</style>

<div>첫번째</div>
<div>두번째</div>
```

두번째 div 형태 요소만 선택이 됩니다.


### 자식
자식은 `>`로 표시를 합니다.

선택하자과 하는 첫번째 깊이의 요소만을 선택합니다.

```
<style>
div > span {
    color:red
}
</style>
```


### 속성 선택
특정 속성을 가지는 요소를 선택합니다.

```css
input[type="text"] {
    border:1px solid red;
}
```


name 속성값이 있는 경우 선택
```css
input[name] {

}
```

### 가상선택자

마우스의 움직임을 처리합니다.

* :hover
요소 위에 마우스가 위치했을 때 반응동작을 지정합니다.

```css
a:hover {

}
```

* :active
요소를 마우스 클릭으로 누르고 있는 경우

```css
a:active {

}
```

* :focus
초점이 잡혀 있을 경우를 말합니다. 키보드의 텝키를 이용하여 
포커스를 지정 또는 이동할 수 있습니다.

```css
a:focus {

}
```

포커스는 마크업한 순서대로 이동을 하게 됩니다.



### 자식 선택자

첫번째 자식 요소만을 선택합니다.

```
요소1 요소2:fitst-child {

}
```

요소와 자식의 순서가 일치를 하여야 합니다.
만일 첫번째 자식이 선택한 요소2가 아닐 경우 선택되지 않습니다.


