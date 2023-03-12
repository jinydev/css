---
layout: home
title: "CSS - Learn html5"
keyword: "css, css3, html5"
description: "hcss3에 대해서 학습합니다."
breadcrumb:
- css
- background
---

> CSS3
# 백그라운드 사이즈 지정
CSS3에서는 백그라운의 사이즈를 지정할 수 있습니다.

기존 css2에서는 배경 이미지가 삽입이 될때, 배경크기를 맞추기 위해서는 별도의 이미지 가공작업이 필요 했습니다.

하지만, CSS3에서는 배경이미지의 사이즈를 변경하여 별도의 작업을 하지 않고도 적용을 할 수 있게 됩니다.

## background-size
이미지의 사이즈를 직접 지정합니다.
`px` 또는 `%`로 입력이 가능합니다.


### 가로 사이즈 기준으로 변경하기
```css
background-size: 100px;
```

한개의 값을 지정할때는 가로 기준으로 변경합니다.
높이는 이미지 비율에 따라 적용합니다.

### 가로, 세로 사이즈 지정하기

```css
background-size: 100px 200px;
```

### 세로 사이즈 지정하기
가로 사이즈를 auto로 지정하고, 세로값을 지정하면 됩니다.
```css
background-size: auto 200px;
```

<br>

### cover
이미지의 비율을 `유지`하면서 요소에 꽉차게 배치를 합니다.

```css
background-size: cover;
```

> 요소에 이미지를 꽉차게 적용하고자 할때에는 가로, 세로를 모두 100%로 입력합니다.

<br>

### contain
이미지 비율을 유지하면서, 한쪽 기준으로 전체가 보이도록 처리를 합니다.

```css
background-size: contain;
```

가로가 긴경우에는 가로 기준으로 배치를 합니다. 높이가 큰경우에는 높이를 기준으로 배치를 합니다.

cover와 다르게 비율이 맞지 않는 부분은 `빈영역`으로 표시가 됩니다.


## 주의
background-size의 속성은 기존 background 속성에 적용을 할 수 없습니다.
별도로 분리된 속성으로 처리를 해야 합니다.


```css
background: url(img.png) no-repeat;
background-size: contain;
```

### 배경이 여러개일 경우

```css
background: 이미지1, 이미지2, 이미지3;
background-size: 설정1, 설정2, 설정3;
```

위와 같이 지정을 할 수 있습니다.


