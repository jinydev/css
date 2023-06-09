---
layout: home
---

# 미디어 쿼리
접속하는 디바이스나 뷰포트에 따라 특정 CSS 스타일을 달리 사용하는 방법을 말합니다. 
즉, 뷰포트의 사이즈 별로 다른 CSS를 적용하는 방법입니다.  

미디어 쿼리(Media Queries)란 컴퓨터나 기기에게 니는 어떤 종류의 미디어니? 또는 '마디어의 화면크기는 어느정도나되니?'라고 미디어에게 질문하고 감지하여 웹시이트를 변경하는 기술입니다.


## 화면의 크기나 환경에 따라 웹사이트를 변경하는 기술,  미디어 쿼리 
이전의 미디어 타입은말 그대로 미디어의 종류만 감지하는 기능만을 가지고 있었습니다.

C:SS3 가등장하면서 이 미디어 타입이라는 기술은미디어 쿼리’라는 이름으로 바뀌었고기
기의 종류뿐만아니라해상도,   비트 수,   가로, 세로 여부동세밀한부분까지 감지할수 였는 기술이 탑
재되면서 반응형 웹의 시작과함께 웹 개발의 새로운 지평을영고 있다는찬시를-받고 있습니다.

### 미디어 쿼리로 브라우저 크기 감지 시 주의하기
미디어 쿼리를 이용해서 크기를 갑지할 때는 HTML 문서의 화면 크기를 기준으로 감지한다는 것


## 미디어쿼리 기본문법
`@media` 키워드를 이용하여 특정 미디어에서 어떤 CSS를 적용할 것인지를 지정합니다. 
이때 특정 구간을 `중단점(breakpoint)`라고 합니다.

미디어 쿼 리를 작성할 때는 기본적인 순서와규칙을 따리야 합니다.

```css
@media [only 또는 not] [미디어 유형] [and 또는 콤마] (조건문) {
    실행문
    }
```

> 미디어 쿼리 구문은 대,소문자를 구별하지 않습니다.


### 미다어 쿼리를 적용할 수 있는 기타 방식들
조건이 여러 개로 나눠지게 되면 그 만큼 CSS 파일의 
개수도 늘어나게 되어 CSS 파일을 여러 번 불러오IOt 하므로 웹사이트의 속도도 느려지기 때문입니다.

링크방식
```html
<link rel="stylesheet" media="all and (min -width:320px)" href= "style320px.css">
```

임포트방식
```css
@import url("style320px.css ") all and (m in -width :320px);
```

이 방식은 되도록 사용하지 않는 것이 좋습니다.


### 미디어쿼리사용시주의사항

* 띄어쓰기주의하기
* 접두사인 min/max 사용 시 작성 순서 주의하기

min을 시용할때는반드시 크기가작은순서대로작성해야하고, max를 시용할 때는반드시 크기가 큰 순서대로 작성 해야합니다.


## 미디어유형
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


## [only 또는 not]

#### only 키워드 
미디어 쿼리를 지원히는 브라우저에서만 미디어 쿼리를 해석하게 해주는 키워드입니다.
미디어쿼리를 지원하지 않는 웹 브라우저에서는 미디어 쿼리를 무시하고 실행하지 않습니다.

#### not
not 다음에 지정하는 미디어 유형을 제외합니다.



## and 또는 , 콤마
and 는 앞뒤 조건이 모두 사실일 때 뒤에 따라오는 것을 해석하라는 의미입니다. 

* and : 조건을 여러개 연결하여 추가합니다.

```css
@media A and B(실행문) 
@media A , B(실행문)
```


## 조건문

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


## 실행문
조건들이 모두 사실일 때 실행되는 실행문입니다.

