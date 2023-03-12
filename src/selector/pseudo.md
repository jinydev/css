---
layout: home
---

# 가상 클래스
가상 클래스는 슈도 클래스(pseudo class)라고 합니다.
HTML 문서에는 존재하지 않지만, css에서 가상으로 요소를 추가하여 처리하는 것을 말합니다.


## 가상 클래스의 활용
HTML 요소에 마우스를 호버 하거나 포커서등이 이동되었을 경우 디자인 상태가 변경되는 것을 볼 수 있습니다. 
이전에는 이러한 동작을 위해서 자바스크립트를 이용해야 했지만, 이제는 CSS 만으로도 간단한 동작들은 쉽게 구현을 할 수 있습니다.

이를 위해서 가상선택 요소의 기능이 도입되었습니다.


## 가상클래스(Pseudo class) 작성규칙

가상 클래스는 선택하고자 하는 HTML 요소의 특별한 상태(status)를 명시할때 사용합니다.
선택자 다음에 콜론(:)을 사용하고, 가상 클래스 이름을 부여합니다.

```css
선택자:가상클래스이름 {
    
}
```

## 위치별 가상 클래스

### :root 선택자
문서 안의 루트 요소에 스타일을 적용합니다.
HTML 문서에서는 루트 요소가 HTML이므로 `HTML` 요소에 스타일이 적용됩 니다. 즉뿌리가 되는부 
분은 <html> 태그입니다. 
> CSS3부터 정의되었습니다


## 구조 선택자
특정한 위치에 있는 태그를 선택하는 선택자입니다. 
> 구조 선택자는 CSS3부터 지원하는 선택자입니다. 


### :first-child, ：last - child 선택자
:first-child는 첫 번째 자식 요소에 적용할 스타일이고，:last-child는 마지막 자식 요소에 적용할 선택자입니다.

* 선택자:first-child
* 선택자:last-child

> CSS3에서 정의되었습니다.



### :nth - child(n)와:nth - last - child(n) 선택자
목이 몇 번째에 있는지 따져서 스타일을 적용할수 있습니다.

* 선택자:nth-child(수열)
* 선택자:nth-last-child(수열)

 이것은문서 구조로 표시했을 때 모두 같은 레벨에 있는 요소라는 의미입니다.
> CSS3에 정의되어 있습니다.


```css
li:nth-child(2n) {
  background-color: red;
}

li:nth-child(2n+1) {
  background-color: blue;
}
```

2n과 2n+1을 통하여 짝수와 홀수를 구분해서 적용을 할 수 있습니다.

* :nth-child = 형제 사이에서의 순서에 따라 요소를 선택합니다.
> 숫자를 지정하거나, even 또는 odd 를 선택합니다.


### :first -of-type, ：last - of—type 선택자
형 제 관계에 있는 요소 중에서 first - of - type은 첫 번째 요소에，last - of - type은 마지막 요소에 
스타일을 적용합니다.

* 선택자:first-of-type
* 선택자:last-of-type


### :nth-of-type(n),:nth 一 last -of-type(n) 선택자

* `:nth-of-type(n)`은 앞에서 세어서 n번째 요소입니다.
```css
선택자:nth-of-type(수열) {

}
```

* `:nth-last-of-type(n)`은끝에서부터 세어 n번째 나타나는요소에 스타일을적용합니다.
```css
선택자: nth-last-type(수열) {

}
```

### ：only-child, ：only-of-type 선택자
`:only-child`는 부모 요소 안의 자식 요소가 유일하게 하나일 때 스타일을 적용.
`:only-of-type`은 해당 요소가 유일한 요소일 때 스타일을 적용합니다.
> CSS3부터 정의되었습니다.








## 링크 선택자
링크 선택자는 href 속성을 가지고 있는 a 태그에 적용되는 선택자입니댜 

> 가상 클래스를 사용할때는 link-> visited -> hover -> active 순으로 선언하여 사용합니다.

a 링크는 이미 한 번 다녀온 렁크는 색이 변경되는 것을 볼 수 있습니다. 링크 선택자는 한 번 이상 다녀온 링크를 선택할 수 있는 선택자입니다.

### :link
하이퍼링크가 있을때 아직 방문하지 않은 링크에 스타일을 적용합니다.
* :link = 아직 방문하지 안은 요소를 나타냅니다.  href 속성을 가진 a, area, link 중 방문하지 않은 모든 요소를 선택합니다.

### :visited 선택자
한 번 이상 방문한 링크에 대한 스타일을 적용합니다.
* :visited = 사용자가 방문한 적이 있는 링크를 나타냅니다.


### :target 선택자


웹 문서에서 같은 사이트의 페이지나 다른 사이트의 페이지로 이동할 때 링크를 이용하고，
같은 문서 안에서 다른 위치로 이동할 때는 앵커(anchor)를 이용합니다.

앵커로 연결된 부분，즉 앵커의 목적지가 되는부분의 스타일을 지정할수 있습 
니다.




## 반응 선택자
html의 일부 요소들은 마우스를 올려 놓거나등의 할때 상황들이 존재합니다.

### :active 선택자
요소가 활성화 되었을 때의 스타일을 지정합니다.
* :active = 사용자가 활성화한 요소를 나타냅니다. (마우스로 클릭하고 있으때)

### :hover 선택자
마우스 포인터를 올려놓았을 때의 스타일을 지정합니다.
> CSS1 부터 정의되어 있습니다.

* :hover = 사용자의 마우스 포인터가 요소 위에 올라가 있으면 선택됩니다.

### ::selection 선택자
사용자가 마우스로 선택했을 때 커서가 드래그되어 선택되는 영역의 스타일을 지정할 수 있습니다. 
> CSS3부터 정의되었습니다.


## 상태 선택자
### :checked
상태의 스타일을 지정합니다.
> CSS3부터 정의되었습니다.

### :focus 선택자
요소에 초점이 맞춰졌을 때의 스타일을 지정합니다.
> CSS2에 정의되어 있습니다.

* :focus = 앵식의 입력칸 등 포커스를 받은 요소를 나타냅니다. 보통 사용자가 요소를 클릭 또는 탭하거나, 키보드 tab키로 선택했을 때 발동한다.


### :enabled
상태의 스타일을 지정합니다.
> CSS3부터 정의되었습니다.

### :disabled
상태의 스타일을 지정합니다.
> CSS3부터 정의되었습니다.



## 부정 선택자
부정 선택지는 지금까지 배운 선택자를 모두 반대로 적용할수 있게 만드는 선택자입니다.

### 선택자:not(선택자)
부정의 의미를 가지고 있습니다. 

```css
:not(hl) { 
    color:blue;  
}
```
위의 예제는 hl 요소가 아닌 모든 요소의 글자색을 파란색으로 지 정하는 스타일입 니다.

* :not = ~ not 안에 포한되 요소를 제외 시키겠다는 의미

```css
/* target 클래스만 적용을 제외한다. */
li:not(.target) {
    
}
```

