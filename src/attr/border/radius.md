---
layout: home
title: "CSS - Learn html5"
keyword: "css, css3, html5"
description: "hcss3에 대해서 학습합니다."
breadcrumb:
- css
---

# CSS3 정리
CSS2에서 3로 넘어오면서 많은 기능이 추가되었습니다.

## border-radiis
테이블을 제외한 모든 요소에 적용을 할 수 있습니다.

모서리가 둥근 사각형을 제작할 수 있습니다.
이전에는 모서리가 둥근 형태일 경우 별도의 이미지로 만들어서 사용을 하는 경우가 흔하였습니다.
하지만 border-radius로 인하여 손쉽게 둥근 모서리를 생성할 수 있습니다.


### radius 전체 적용
사각형 전체 모서리에 곡률을 적용을 할때에는 한개의 값만 지정하면 됩니다.

```css
border-radius: 50px; 
```

> 예제파일: radius.html



### 곡율적용으로 원 만들기
곡율을 사이즈의 50% 이상값을 주게 되면 곡율로 인하여 원형 모향이 됩니다.

```css
border-radius: 50%; 
```

> 예제파일 : ./sample/radius2.html

사진에도 radius를 적용하여 둥근 모양을 만들 수 있습니다.
과거에는 포토샵으로 둥근 이미지와 투명배경 작업을 하여 사용을 하였지만,
최근에는 radius 를 적용하여 쉽게 원형 이미지를 만들어 낼 수 있습니다.


### 모서리 다르게 지정하기


```css
border-radius: 50px 25px; 
```


값을 지정하는 방법은 패딩값을 설정하는 규칙과 동일합니다.
패딩의 경우 첫번째 값이 `좌/우`에 적용되고, 두번째 값은 `상/하`에 적용됩니다.

radius의 경우에는 반시계 45도 회전하여 각각의 모서리에 적용이 되는 형태 입니다.

첫번째 값은 왼쪽상단/오른쪽하단에 적용됩니다.
두번째 값은 오른쪽 상단/ 왼쪽 하단에 적용합니다.


### 3개 적용


```css
border-radius: 50px 25px 10px; 
```

세번째 값은 오른쪽 하단에 적용이 됩니다.


### 4개 적용

```css
border-radius: 50px 25px 10px 3px; 
```

네번째 값은 왼쪽 하단에 적용이 됩니다.



## 특정 모서리만 지정하기
border-radius는 전체 모서리에 일괄적으로 곡율을 적용하는 속성입니다.

특정 모서리만 곡율을 적용할 수 있습니다.
이때는 모서리를 지정하는 속성을 선택합니다.

```css
border-bottom-left-radius: 50px;
```
> 예제코드 : ./sample/radius6.html


```css
border-bottom-right-radius: 50px;
```

```css
border-top-left-radius: 50px;
```

```css
border-top-right-radius: 50px;
```


## 곡율 적용하여 버튼 만들기

> 예제코드: ./sample/radius11.html



