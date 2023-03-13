---
layout: home
---

# 레이아웃

## float
float은 레이아웃을 설계할때 자주 사용이 됩니다.


## 정렬
레이아웃을 정렬합니다. 

* 중앙정렬
* 수평정렬



### float 속성 - 요소를 떠 있게 하기
float 속성은 웹 요소를문서 위에 떠 있게 하는 것입니다. 

float 속성은 문서의 레이아웃을 조절하려고 할 때 많이 사용됩니다.
> 요소가 떠 있으려면 위 
치가 고정되면 안 되기 때문에 position 속성에서 absolute를 사용해서는 안 됩니다.

```css
float:속성값;
```

### clear 속성 - float 속성 무효로 만들기
float 속성을 이용하여 웹 페이지 요소를 왼쪽이나 오른쪽에 배치하면 그 다음에 넣는 다른 요소들 
에도 똑같은 속성이 전달됩니다.

```css
clear: 속성 값;
```




* left : 왼쪽으로 떠 있지 않도록 합니다. 
* right : 오른쪽으로 떠 있지 않도록 합니다.
* both : 왼쪽이나 오른쪽 어디에도 떠 있지 않도록 합니다. 
* none : 왼쪽과 오른쪽 모두에 뜰 수 있습니다. 기본 값입니다

float:left를 이용하여 왼쪽으로 배치했다면 clear:left로 종료하고, 
float:right를 사용했다면 clear:right를 사용해 무효화시킴니다.


float 속성 값이 left인지 right인지에 상관없이 무조건 기본 
상태로 되돌리고 싶다면 `clear:both`라고 하면 됩니다.



## float 레이아웃 연습
float 기능을 활용한 다양한 레이아웃을 만들어 봅니다.

* [레아아웃1](/layout/float/ex/float1.htm)
* [레아아웃2](/layout/float/ex/float2.htm)
* [레아아웃3](/layout/float/ex/float3.htm)
* [레아아웃4](/layout/float/ex/float4.htm)
* [레아아웃5](/layout/float/ex/float5.htm)
* [레아아웃6](/layout/float/ex/float6.htm)
* [레아아웃7](/layout/float/ex/float7.htm)


