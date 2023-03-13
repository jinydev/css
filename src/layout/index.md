---
layout: home
---

# 레이아웃 스타일
CSS가 강력한 이유 중 하나가 웹사이트를 제작할 때 텍스트나 이미지, 표 등 웹 문서 안의 요소를 자유자재로 배치할수 있다는 것입니다. 레이아웃을 구현하기 위한 다양한 기술에 대해서 알아 보도록 합니다.


## 박스 모델
css의 박스 모델을 사용하면 텍스트 단락에서 테두리와 내용 사이에 적절하게 골간을 두어 읽기 
쉽게 만들 수 있고, 이미지에 다양한 색상의 테두리를 추가할 수도 있습니다. 

* [박스모델](/layout/box)

## 박스모델 속성
* [패딩영역](/layout/box/padding)
* [마진영역](/layout/box/margin)
* [테두리 영역](/layout/box/border)
* [그림자 영역](/layout/box/shadow)


## Display 속성
Display 속성은 HTML 요소를 어떻게 처리를 할 것인지에 대해서 지정을 하는 방법입니다.

* [디스플레이 속성이란?](/layout/display)


## Float
* [float 응용](/layout/float)


## position

* [position 학습하기](/layout/position)





### visibility 속성 - 요소를 보이게 하거나 보이지 않게 하기

요소를 화면에 보이게 하거나 보이지 않게

```css
visibility:속성 값;
```

visibility를 hidden으로 하면 화면에서 감춘 요소들은 눈 
에 보이진 않지만, 실제로는 공간을 차지하고 있습니다.


* visible : 요소를 화면에 표시합니다. 기본 값입니다.
* hidden : 요소가 화면에서 감춰집니다 하지만 크기는 그대로 유지하기 때문에 배치에 영향을 줍니다.
* collapse : 표의 행이나 열. 행 그룹, 열 그룹 등에서 지정하면 서로 겹치도록 조절합니다.
* inherit : 부모 요소의 visibility 속성을 상속합니다






## 다단으로  편집하기
CSS3은 column과 관련된 여러 속성이 있습니다.
> 다단과 관련된 속성은 브라우저 제조업체 접두사를 붙여 사용해야 합니다.

### column-width - 단의 너비 지정하기
한 화면을 여러 개의 단(column)으로 구성할 때，단의 너비를 고정해 놓고 화면을 분할할 수 있습니다

```css
column-width: 속성 값;
```

### column-count 속성 - 단의 개수 지정하기
다단 화면을 만들 때 단의 개수를 먼저 정해놓고 화면을 분할할 수도 있습니다. 
> 화면이 커질수록 단의 너비가 넓어집니다.

```css
column-count: 속성 값;
```

### column-gap 속성 - 단과 단 사이 여백 지정하기
단 사이의 여백을 지정하는 속성입니다.

```css
column-gap:속성 값;
```

### column-rule 속성 - 구분선의 색상，스타일，너비 지정하기

### column-span 속성 - 여러 단을 하나로 합치기
단을 합쳐서 내용을 표시해야 할 경우

```css
column_span: 속성 값;
```






