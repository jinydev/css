---
layout: home
---

# 목록 스타일
목록은 다양한 요소들을 배치하는 용도로 자주 사용됩니다.

## list-style-type 속성 - 목록의 불릿과 번호 스타일 지정하기
list-style-type 속성은 순서 없는 목록의 불릿과 순서 목록의 번호 유형을 지정합니다.

```css
list-style-type:속성 값;
```

* disc
* circle
* square

* decimal : 1 로시작하는 십진수 (예: 1,2. 310. 11....)
* decimal-leading-zero : 0이앞에 붙는 십진수 (예: 01. 02, 03,10. 11....〉 
* lower-roman : 소문자 로마 숫자 (예: i, ii, iii, iv,...)
* upper-roman : 대문자로마숫자(예:  I. K. m, IV,...) 
* lower-greek : 소문자 그리스 문자
* lower-alpha 또는 lower-latin : 소문자 알파벳 (예: a. b, c. d, e....) 
* upper-alpha 또는 upper-latin : 대문자 알파벳 (예: A. B. C. D. E,...) 
* hebrew : 히브리 숫자
* armenian : 아르메니아 숫자
* georgian : 조지 왕조 시대의 숫자 (예: an, ban, gan,...) 
* cjk-ideographic : 단순한 표의 문자 (ideographic)
* hiragana : 히라가나 (0||: a. i,  u, e. o. ka. ki....)
* hiragana-iroha : 히라가나 번호 붙이기 (예: i, ro, han, ni, ho. he....) 
* katakana : 가타가나 (예: A. 1,  U. E, 0, KA, KI,...)
* katagana-iroha : 가타가나 번호 붙이기 (예: 1. RO, HAN. Nl. HO. HE....)



불릿을 감추고 싶다면 list-style-type 속성의 값을 `none` 으로 지정하면 됩니다.


### list-style-position 속성 - 목록에 들여쓰는 효과 내기

기본적으로 불릿이나 번호는 실제 내용 바깥쪽에 표시됩니다. 

하지만 이 속성을 이용하면 실제 내용이 시작되는 위치에 불릿이나 번호를 표시하기 때문 
에，결과 화면에는 불릿이나 번호가 좀더 안으로 들여써진 듯한 효과를 보입니다.

```css
list-style-position:속성 값;
```


* inside : 불릿이나 숫자를 안으로 들여씁니다.
* outside : 기본 값으로 불릿이나 숫자를 밖으로 내어씁니다


### list-style-image 속성 - 불릿 대신 이미지 넣기
직접 만든 이미지를 
불릿으로 넣고 그 옆에 텍스트를 입 력하는 방법

```css
list-style-image:url(이미지 파일 경로);
```

### list-style 속성 -  리스트 속성 한꺼번에 표시하기

 list-style-type과 list-style-position, list-style-image 속성을 한꺼번 
에 표시하는속성

