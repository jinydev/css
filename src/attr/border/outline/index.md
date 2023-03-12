---
layout: home
title: "CSS3의 outline - Learn html5"
keyword: "css, css3, html5"
description: "css3의 outline 속성에 대해서 학습합니다. 요소의 포커스에 대한 외각선 모양을 변경할 수 있습니다."
breadcrumb:
- css
- outline
---

> CSS3
# outline

포커스 초첨이 있는 요소일 경우, 외각선을 설정할 수 있습니다.

기본값은 연한 파랑색으로 표시가 됩니다.

```css
.link1:focus {
    outline: 1px solid brown;
}
```

초점 외에도 강제 설정시 일반상태에서도 outline을 출력할 수도 있습니다.


### outline vs border

outline은 border는 유사합니다. 아웃라인은 외각선 밖에 위치합니다.
만일, outline과 border를 2개 설정하여 중첩된 선을 만들 수 있습니다.

```css
a {
    outline: 1px solid brown;
    border: 1px solid blue;
}
```

> 예제코드: ./sample/outline2.html


> 참조: 아웃라인은 외곽선과 달리 상/하/좌/우 개별로 선택하여 지정을 할 수 없습니다.


## outline-offset
아웃라인과 외각선간의 간격은 없습니다. 중간에 간격을 두기 위해서는
`outline-offset` 속성을 주어야 합니다.

```css
outline-offset: 10px;
```

> 예제파일: ./sample/outline3.html

### outline은 주의 요소에 영향을 반영하지 않음
예제파일을 확인해 보면 아웃라인의 좌측 상단이 잘려져 보인는 것을 
볼 수 있습니다.  

outline은 주변 요소에 영향을 미치지 않습니다.













