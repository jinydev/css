---
layout: home
title: "CSS - Learn html5"
keyword: "css, css3, html5"
description: "hcss3에 대해서 학습합니다."
breadcrumb:
- css
- background
- multi
---

# 멀티 백그라운드
---

css2에서는 하나의 요소에 한개의 배경만 설정이 가능하였습니다.

css3로 넘어오면서 하나의 요소에 여러개의 배경을 설정할 수 있게 되었습니다.

`쉼표`를 통하여 여러개의 배경 설정을 지정할 수 있습니다.

```css
background: 설정1, 설정2, 설정3;
```

> 예제코드 : ./sample/background11.html

```css
background-image: url(img1.png), url(img2.png), url(img3.png);
background-repeat: no-repeat, repeat-x, repeat-y;
background-position: top. left, bottom;
```

삽입되는 이미지와 추가 속성을 분리하여 1:1 대응을 합니다.





