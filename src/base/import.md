---
layout: home
---

# Import
작성된 CSS파일들 중에는 nested 하게 CSS 파일들을 결합하여 사용을 하는 것을 볼 수 있습니다.  

CSS 문법 중에서 `@import`는 외부의 다른 CSS파일을 읽어와 결합을 합니다. 작성규칙은 다음과 같습니다.

```css
@import url(스타일파일.css);
```

예를 들어 봅니다. 2개의 스타일시트 파일이 존재합니다. HTML은 여러개의 CSS 파일을 로드하여 사용을 할 수 있습니다.

```html
<head>
    <link rel="stylesheet" href="style1.css"/>
    <link rel="stylesheet" href="style2.css"/>
</head>
```

이렇게 HTML에서 여러개의 파일을 로드하는 것 대신에 스타일 구문에서 또 다른 스타일CSS 파일을 로드할 수 있습니다.

```html
<style>
    @import url(style1.css);
    @import url(style2.css);
</style>
```

## import와 media를 병행한 사용
`@media`는 클라이언트의 장비나 화면사이즈 조건이 일치하는 경우에 CSS 적용 범위를 분리 합니다. 이를 import 구문과 같이 사용을 할 수도 있습니다.

```html
<style>
    @import url(style1.css) screen;
    @import url(style2.css) print;
</style>
```

보여지는 클라이언트가 화면일 경우에는 `style1.css` 를 적용하고, 프린트 하는 경우에는 `style2.css` 를 적용하는 방법입니다. 

반응형 웹을 만들때에도 import 구분을 이용하여 CSS 파일을 분리하여 관리를 할 수 있습니다.


