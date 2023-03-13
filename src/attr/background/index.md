---
layout: home
---

# 배경 속성
태그의 배경 이미지 또는 색상을 지정하는 스타일 속성입니다.


## background-image 속성
background-image 속성은 배경에 넣을 그림을 지정하는 스타일 속성입니다.

## background-size 속성
그림 크기를 조절할 때는 background-size 속성을 사용합니다.

> background-size 스타일 속성은 CSS3에서 추가된 속성이므로 인터넷 익스플로러 8 이하에서는 시용 할 수 없습니다.

* contain
* cover


## background-repeat 속성


## background-attachment 속성
배경 이미지를 어떠한 방식으로 화면에 붙일 것인지를 지정하는 
스타일 속성입니다.


## background-position 속성

* background-position:  키워드;
* background-position: X축크기;
* background-position: X축크기 Y축크기;





## 배경(background)

### 배경이미지

```css
background-image:url(이미지);
```


```css
background-repeat:no-repeat;
```

* repeat : 반복허용
* repeat-x : 가로만 반복허용
* repeat-y
* no-repeat

### 배경색
```css
background-color: 색;
```

### 배경위치 변경
```css
background-position:위치
```

* right
* top
* left
* bottom
* center

background-position: rigth top
background-position: rigth bottom
background-position: center top

정가운데 위치
background-position: center

숫자값으로 지정

```css
background-position: 10px 10px
```
죄측 상단을 기준으로 떨어진 x, y 값에 배치를 합니다.

`%`를 통하여 지정할 수 있습니다.
```css
background-position: 10% 10%
```

한번에 정의하기

`background` 속성명 뒤에 여러 값을 순차적으로 나열을 하면 됩니다.

```css
div {
    background: url(img.png) no-repeat 20px center #ccc;
}
```







