---
layout: home
title: "html5"
keyword: "html5"
description: "html을 학습합니다."
---

# id속성
---
id를 이용하여 요소를 선택합니다.
id는 태그에 지정을 할 수 있는 속성입니다.
아이디를 이용하여 요소를 선택할 수 있습니다.

<br>

## id 속성 부여
html 테그안에 id 속성을 부여합니다.

```html
<h1 id="heading">Hello world</h1>
```
<br>

### 유일성
---
아이디는 하나의 문서에 중복되지 않도록 사용하는 것이 중요합니다.

## css 선택
---
테그의 속성으로 선택된 아이디를 선택할 수 있습니다.
아이디를 선택할때에는 `#`기호를 사용합니다.

```css
#heading {
    color:red;
}
```