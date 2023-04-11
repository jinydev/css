---
layout: home
---

# 반응형 레이아웃
반응형 웹사이트는 `PC`와 `모바일` 양쪽에 최적화 하여 화면을 출력하기 위해서 적용되는 기술 입니다.


## 반응형 웹 기본 개념 이해하기
웹 사이트가 PC화면 뿐만 아니라 모바일, 태블리, 노트북등 여러 가지 디바이스의 `해상도`에 반응하여 각각에 맞는 화면을 보여주는 홈페이지 제작 기법입니다.

* [반응형 웹이란?](/response/res)
* 왜 반응형 웹으로 만들어야 하나



## 반응형 웹 기본 기술
반응형 웹을 만들기 위한 기본 기술에 대해서 알아 봅니다. 반응형은 다양한 사이즈의 화면을 가지는 기기에 잘 보이기 위하여 레이아웃과 컨덴츠를 가공하여 보여주는 기술입니다.

### [뷰포트](/response/viewport)
반응형 웹을 구현하기 위해서는, 먼저 사이트에 접속한 기기의 정보를 얻는 것입니다. 이를 위하여 뷰포트라는 기술을 이용하여 브라우저에게 접속기기의 정보를 전달하는 메타테그 입니다.

* 화면을 제어하는 기술 -  [뷰포트](/response/viewport)  



### [미디어쿼리](/response/media)
뷰포트를 통하여 얻은 화면의 크기에 따라서 CSS 코드를 다르게 변경하는 기술을 말합니다. 미디어쿼리는 접속된 기기의 종류와 화면 사이트에 따라서 동작을 합니다.

* 화면의 크기와 환경 감지 및 웹사이트를 변경하는 기술 - [미디어 쿼리](/response/media)  




## 반응형 미디어 쿼리
미디어쿼리를 이용하여 화면 사이즈에 맞는 반응형 CSS를 적용하는 코드를 실습해 봅니다.

* [반응형 레이아웃 실습](sample/res-layout-media.htm)

```css
/* 화면 너비가 1280px 이상인 경우: 고해상도 데스크탑 */
@media (max-width: 1280px){
    body {
        background: #880e4f;
    }
}

/* 화면 너비가 1024px 이상인 경우: 데스크탑 */
@media (max-width: 1024px){
    body {
        background: #4a148c;
    }
}

/* 화면 너비가 960px 이상인 경우: 노트북 */
@media (max-width: 960px){
    body {
        background: #311b92;
    }
}

/* 화면 너비가 768px 이상인 경우 : 타블렛 */
@media (max-width: 768px){
    body {
        background: #4a148c;
    }
}

/* 화면 너비가 0 ~ 576 : 모바일 */
@media (max-width: 576px){
    body {
        background: #004D40;
    }
}
```


## 반응형 레이아웃 연습
미디어쿼리를 이용하여 다양한 반응형 레이아웃을 만들어 봅니다.

* [반응형 레이아웃-01](sample/res1.htm)
* [반응형 레이아웃-02](sample/res2.htm)
* [반응형 레이아웃-03](sample/res3.htm)
* [반응형 레이아웃-04](sample/res4.htm)
* [반응형 레이아웃-05](sample/res5.htm)


## 가변 그리드
반응형에 맞는 가변적인 크기를 적용하기 위한 단위 변경에 대해서 알아 보도록 합니다.

* [퍼센트 단위](/response/fluid)
* [em 단위](/response/fluid)
* [rem 단위](/response/fluid)


## 화면 방향 전환
요즘 모바일기기들은 세로형 보기모드와 가로형 보기 모드를 지원합니다. CSS에서도 media를 감지하여 이를 구분한 CSS를 적용할 수 있습니다.

```css
@media screen and (orientation: portait) {

}

@media screen and (orientation: landscape) {

}
```



## 참고도서
* DoIt, 반응형 웹 만들기
* https://www.youtube.com/watch?v=52TT7SLexxE&list=PL4UVBBIc6giL7ygRa-P7UExEKqZgx4t9K