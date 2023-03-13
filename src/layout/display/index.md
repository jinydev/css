---
layout: home
---

# Display 속성
Display는 해당 요소가 화면에 어떻게 보여질 것인지 지정하는 속성입니다.

## 속성 적용 방법

```css
display: 속성 값;
```


### display 속성의 종류

* block : 블록 레벨 박스로 만듭니다. 
* inline : 인라인 레벨 박스로 만듭니다.
* inline-block : 블록 레벨 박스이지만 인라인 레벨 박스처럼 배치합니다 

* none : 박스를 만들지 않으며 시각적으로 표시하지 않습니다. 
* inherit : 상위 요소의 display 속성을 상속받습니다.

* table : 블록 레벨의 표로 만듭니다
* inline-table : 인라인 레벨의 표로 만듭니다 （HTML에서 table에 해당）. 
* table-row : 표의 행으로 만듭니다 （HTML에서 너에 해당）.
* table-row-group : 표의 본체 행 그룹으로 만듭니다 （HTML에서 tbody에 해당）.
* table-header-group : 헤더 행 그룹으로 만듭니다 （HTML에서 thead에 해당）.
* table-footer-group : 푸터 행 그룹으로 만듭니다 （HTML에서 tfoot에 해당）.
* table-column : 표의 열로 만듭니다 （HTML에서 col에 해당）.
* table-column-group : 표의 열 그룹으로 만듭니다 （HTML에서 colgroup에 해당）.

* table-cell : 표에서 하나의 셀로 만듭니다 （HTML에서 td나 th에 해당）. 
* table-caption : 표의 캡션을 만듭니다 （HTML에서 caption에 해당）.
* list-item : 목록의  항목을 표시할 수 있도록 기본적인 블록 박스와 표시자 박스를 만듭니다 
（HTML에서 li에 해당）.

> display 속성 을 익혀두면 레이아웃을 만들 때 편리합니다.


# CSS-Display

`display`은 HTML 요소를 어떻게 표시를 할 것인지를 결정하는 속성입니다.



HTML 요소마다 서로 다른 display 속성값을 가지고 있습니다. 대표적으로 `block` 와 `inline` 레벨 요소 입니다.



## 기본 4가지 요소



### none

HTML 요소를 화면에 보이지 않게 합니다. 

> `visibility`속성의 `hidden`값과의 차이점은 영역을 차지 하지 않는 다는 것입니다.



### block

박스 모델에서 가로 영역을 모두 사용하는 출력 형태 입니다. block 요소들이 배치가 되면 마치 줄바꿈이 된것 처럼 세로로 배치가 됩니다.



### inline

컨덴츠 영역만큼 차지하게 됩니다. 따라서, 블럭요소와 달리 요소들은 가로로 배치되어 출력하게 됩니다.

또한 width와 height 값을 지정하여 사용을 할 수 없습니다.



### inline-block

block 과 inline의 중간 형태의 요소 입니다. inline 처럼 컨덴츠의 크기 만큼 영역을 차지하고, 가로로 배치가 됩니다.

또한 block 요소처럼 width와 height 속성을 부여할 수 있습니다.
