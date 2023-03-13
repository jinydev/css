---
layout: home
---

# 테이블


## 표 관련  스타일
표와 관련된 여러 css에 대해 살펴보겠습니다.

### table-Layout 속성 - 콘텐츠에 맞게 셀 너비 지정하기
셀 너비를 변하게 할지 고정시킬지 여부 를 결정할수 있습니다.

```css
table-layout:속성 값;
```

* fixed : 셀 너비를 고정합니다. 즉 셀 안의 내용 양에 따라 셀의 너비가 달라지지 않습니다. 
* auto : 셀 안의 내용에 따라 셀의 너비가 달라집니다 기본 값입니다.
* inherit : 부모 요소의 table-layout 값을 상속합니다


### 셀 안의 수평 정렬과 수직 정렬

text - align 속성
텍스트의 가로 정렬 방법을 지정하는 것입니다.

```css
text-align:속성 값;
```

* left
* right
* center
* justify

vertical-align 속성
세로 정렬 방법을 지정하는 것입니다.

```css
vertical-align:속성 값;
```

* baseline
* top
* bottom
* middle


### border-style 속성 - 표 테두리 스타일 지정하기
border-style 속성으로 테두리 스타일을 지정할 수 있습니다

### border-collapse 속성 - 테두리 통합，분리하기
표의 바깥 테두리와셀의 각 테두리가 떨어져 있는 것을 떨 어진 채로 둘 것인지，두 테두리를하나로 합칠 것인지 결정할수 있습니다.

```css
border-collapse:속성 값;
```

* collapse : 테두리가 통합됩니다.
* separate : 테두리가 분리됩니다. 기본 값입니다.
* inherit : 부모 요소의 border-collapse 값을 상속합니다.


### border-spacing 속성 - 인접한 셀 테두리 사이 거리 지정하기
셀들을 분리했을 경우 인접한 셀 테 두리 사이의 거리를지정합니다.
> border-spacing 속성은 border-collapse:seperate를 사용하여 셀들을 분리했을 경우

```css
border-spacing:속성 값;
```

### empty-cells 속성 - 빈 셀의 표시 여부 지정하기
cmpty-cclls 속성을 사용해 내용이 없 
는 빈 셀들의 표시 여부를 지정합니다.

```css
empty-cells:속성 값;
```


* show : 빈 셀 주위에 테두리를 그려 빈 셀을 표시합니다. 기본 값입니다.
* hide : 빈셀주위에테두리를 그리지않습니다.
* inherit: 부모 요소의 값을 상속합니다

### caption-side 속성 - 캡션 위치 바꾸기

캡션의 위치를 옮길 수 있습니다.

```css
caption-side:속성 값;
```

* top : 캡션을 표의 윗부분에 표시합니다.
* bottom : 캡션을 표의 아랫부분에 표시합니다


