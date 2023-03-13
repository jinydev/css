---
layout: home
---

# Important

## CSS 적용 우선순위

`사용자 !important` > `제작자 important` > 제작자 > 사용자 > 브라우저 

순으로 우선순위가 반영됩니다.


### 절대 최고값, !important
위의 모든 우선순위를 무시하고 적용하는 초고 우선순위를 말합니다.
우선순위를 무시합니다.

```css
* {
    color:red !important;
}
div {
    color:blue;
}
```


`*` 보다 우선순위가 높은 div 테그의 스타일이 적용되어야 하나, `!important`로 인하여 우선순위가 낮은 `*` 선택자가 적용되는 것을 확인할 수 있습니다.

> `!important`는 세미콜론 안쪽에 넣어 줍니다.