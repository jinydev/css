---
layout: home
---

# 가상 요소 선택자
HTML 문서의 요소로는 존재하지 않지만, 마치 존재하는 것처럼 CSS 스타일로 요소를 생성하여 처리합니다.

## 가상요소란?

가상 요소(pseudo-element)는 해당 HTML 요소의 `특정 부분만을 선택`할 때 사용합니다.

```css
선택자::가상요소이름 {
    
}
```

## 문자 선택자
문자 가상 요소 선택자는 태그 내부 특정 조건의 문지를 선택히는 선택자입니다.

문자 선택자는 가상 요소 선택지로 `::` 기호를 시용하는 것이 표준이지만 `:` 기호를 시용해도 정상 작동합니다.

* 시작문자 선택
* 전후 문자 선택자
* 반응 문자 선택자

## 시작문자 선택
시작 문자 선택지는 태그 내부의 첫 번째 글자와 첫 번째 줄을 선택할 때 시용히는- 선택자입니다.

#### ::first-line
텍스트의 첫번째 라인만을 선택합니다. 이는 블록 레벨 요소에서만 사용이 가능합니다.

#### ::first-letter
텍스트의 첫 글자만을 선택합니다. 이는 블록 레벨 요소에서만 사용이 가능합니다.


## 전후 문자 선택자
전후 문자 선택지는 특정 태그의 전후에 위치하는 공간을 선택하는 선택자입니다.

전후 문자 선택자에는 content 속성을 사용할수 있습니다


#### ::before
특정 요소의 내용(content) 부분 바로 앞에 다른 요소를 삽입할 때 사용합니다.
> CSS2부터 정의되었습니다.


> 사용 예) 

> ```css
> .require::before {
>     content: '*';
>     margin-right: 2px;
>     color:red;
> }
> ```
>
> 

#### ::after
특정 요소의 내용(content) 부분 바로 뒤에 다른 요소를 삽입할 때 사용합니다.
> CSS2부터 정의되었습니다.


툴팁 만들기

```html
<style>
    [data-tooltip] {
        position:relative;
    } 
    
    [data-tooltip]:hover::after {
        content: attr(data-tooltip);
        position: absolute;
        top:0px;
        left:50px;
        background-color: black;
        color:white;
        width:150px;
    }
</style>

<div data-tooltip="클릭하세요" >
    보내기
</div>
```


## 반응 문자 선택자
반응 문자 선택자는 시용자가 문자와 반응해서 생기는 영역을 선택하는 선택자입니다.


#### ::selection
해당 요소에서 사용자가 선택한 부분만을 선택할 때 사용합니다.


