---
layout: home
---

# 미디어쿼리와뷰포트

## 화면의 크기나 환경에 따라 웹사이트를 변경하는 기술,   미디어 쿼리 
이전의 미디어 타입은말 그대로 미디어의 종류만 감지하는 기능만을 가지고 있었습니다.

C:SS3 가등장하면서 이 미디어 타입이라는 기술은미디어 쿼리’라는 이름으로 바뀌었고기
기의 종류뿐만아니라해상도,   비트 수,   가로, 세로 여부동세밀한부분까지 감지할수 였는 기술이 탑
재되면서 반응형 웹의 시작과함께 웹 개발의 새로운 지평을영고 있다는찬시를-받고 있습니다.

### 미디어쿼리의 기본문법
미디어 쿼 리를 작성할 때는 기본적인 순서와규칙을 따리야 합니다.

```css
@media [only 또는 not] [미디어 유형] [and 또는 콤마] (조건문) {실행문}
```
> 미디어 쿼리 구문은 대 · 소문자를 구별하지 않습니다.


#### [only 또는 not]
only 키워드는 미디어 쿼리를지원히는브라우저에서만미디어 쿼리를해석하게 해주는키워드입니다.

#### 미디어유형
미디어별로 적용할 CSS를 따로 작성

* all : 모든장치
* print :  인쇄장치
* screen : 겅퓨터 화면 장치 또는 스바트 기기의 화면
* tv : 영상과 음성이 동시에 출력되는 징차
* projection :  프로젝터 징처
* handheld :  손에 듈고 다니논 소헝 장치
* speech :  음성출력장차
* aural :  음성 합성 장치(화면을 읽어 소리로 출력해 주는 상치)
* embossed :  점자 인쇄 장치(화민을 읽어 종이에 접자를 찍어내는 장치)
* tty : 디스플레이 가능이 제한된 장치
* braille : 섬자표시장치


### and 또는 , 콤마
and 는 앞뒤 조건이 모두 사실일 때 뒤에 따라오는 것을 해석하라는 의미입니다. 

```css
@media A and B(실행문) 
@media A , B(실행문)
```

### 조건문

* width
* height 
* device-width 
* device-height
* orientation
* aspect-ratio
* device-aspect-ratio 
* color
* color-index 
* monochrome 
* resolution 
* scan
* grid

### 실행문
조건들이 모두 사실일 때 실행되는 실행문입니다.

### 미다어 쿼리를 적용할 수 있는 기타 방식들
조건이 여러 개로 나눠지게 되면 그 만큼 CSS 파일의 
개수도 늘어나게 되어 CSS 파일을 여러 번 불러오IOt 하므로 웹사이트의 속도도 느려지기 때문입니다.

링크방식
```html
<link rel="stylesheet" med ia="all and (min -width:320px)" href= "style320px.css">
```

임포트방식
```css
@import url("style320px.css ") all and (m in -width :320px);
```

이 방식은 되도록 사용하지 않는 것이 좋습니다.


### 미디어쿼리사용시주의사항

* 띄어쓰기주의하기
* 접두사인 min/max 사용 시 작성 순서 주의하기
min을 시용할때는반드시 크기가작은순서대로작성해야하고, 
max를 시용할 때는반드시 크기가큰순서대로작성해야합니다.


### 미디어 쿼리로 브라우저 크기 감지 시 주의하기
미디어 쿼리를 이용해서 크기를
갑지할 때는 HTML 문서의 화면 크기를 기준으로 감지한
다는 것


## 화면의 보이는 영역을 다루는 기술, 뷰포트

데스크톱은사용자가설정한해상도가뷰포트 영역이 되고.
스마트 기기는 기본으로 설정되어 였는 값이 뷰포트 영역이 됩니다.


뷰포트 메타 태그를 이용해서 화면의 크기나배율을 조절해야합니다

```html
<meta name= "viewport" content="width =device-width , initial-scale=1, minimum-scale=1, 
maximum-scale=1, user-scalable=no">
```

뷰포트속성
* width : devi ce - width. 앙수
* height : devi ce height. ~상수


* initial-scale : 뷰포트의 초기 배율을 지성합니다
기본값은 1 입니다. 1 보다 작은 값을 사용하면 축소된 패이지를 표시
하고. 1 보다 큰 값을 사용하면 확대된 1I1IO IXI 를 표시합니다


* user-scalable
뷰포트의 확대/축소 여부를 지정합니다.


* minimum-scale
뷰포트의 최소 축소 비율을 지정합니다.

* maximum-scale
뷰포트의 최대 확대 비율을 지정합니다.







