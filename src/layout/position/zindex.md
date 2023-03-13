---
layout: home
---

# Z-index

## z-index 속성
요소들은 계층적으로 중첩이 되면서 배치가 됩니다.  
일반적으로 화면에서 x,y 평면을 기준으로 움직인다면, 요소는 z 축을 통하여 쌓이게 됩니다.
이러한 z축의 층간을 결정하는 요소 입니다.

## z-index
요소가 겹쳐져 있을때 화면에 보이는 순서를 변경할 수 있습니다.

예를 들어 여러개의 요소들이 절대값으로 인하여 동일한 위치에 있을경우
마지막에 있는 요소만 보이게 됩니다.

이를 순서를 변경하기 위해서는 z-index 옵션을 사용해 주어야 합니다.


```css
z-index:숫자;
```


### z-index 속성 - 요소 쌓는 순서 정하기
요소를 쌓는 Z축도 고 
려합니다.

```css
z_index: 숫자값;
```
> 웹 문서에 가장 먼저 삽입하는 요소가 z-index:1 