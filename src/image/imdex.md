---
layout: home
---

# 이미지 속성

## 스프라이트 이미지
스프라이트 이미지는 여러 이미지를 한장의 이미지 파일로 묽어 놓은 것을 말합니다.

작은 이미지들을 한장의 이미지로 묽어 놓는 이유는 서버에 이미지를 요청하는 `시간`을 줄이기 위해서 입니다.
스프라이트 이미지는 background-position 속성을 같이 사용 합니다.

```css
background: url('스프라이트.jpg');
background-position: -62 0px;
```