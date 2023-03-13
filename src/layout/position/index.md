---
layout: home
---

# 위치 속성
html 요소의 위치를 결정합니다. 

* [z-index](/layout/position/zindex)
* [overflow](/layout/position/overflow)

## 좌표 체계
HTML의 요소를 배치하는 위치는 크게 `절대위치`와 `상대위치`가 있습니다.

* 절대 위치 좌표: 요소의 X 좌표와 Y 조十포를 설정해 절다 워치를 지정합니다.
* 상태 위치 좌표 : 요소를 입력한 순서를 통해 상대적으로 워치를 지정합니다

대부분 요소를 배치할 때는 상대 위치 좌표를 사용해 페이지를 만듭니다. 하지만, 사이트를 제작하다 보면 특별한 위치에 요소를 배치하거나 고정해야 되는 경우도 발 생합니다. 이때, 위치 속성을 이용하여 요소를 배치할 수 있습니다.


## position 속성
태그의 위치 설정 방법을 변경 할 때는 `position` 속성을 사용합니다.

### static
기본적으로 위치의 속석은 `static`입니다. static 키워드를 적용하면 태그가 “위에서 아래로”와 '‘왼쪽에서 오른쪽으로” 순서에 맞게 배치
됩니다(direction 속성을사용해 "오른쪽에서 왼쪽”으로 변경할수 있습니다).

### relative
relative 키워드를 적용하면 static 키워드로 초기 위치가 지정된 상태에서 상하죄우로 이동할 수 있습니댜

### absolute
절대 위치 좌표를 사용할 때는 position 속성에 absolute 키워드를 지정합니다.
> fixed와의 차이점은 기준점으로 부터 절대 좌표가 결정됩니다.

### fixed
절대 위치 좌표를 사용할 때는 fixed 키워드를적용합니다.
> absolute와의 차이점은 화면을 기준으로 절대 위치 좌표를 설정합니다.




## position
요소의 위치를 이동합니다.

### static 
기본값으로 요소의 좌표를 이동할 수 없습니다.

```css
div {
    position: static;
}
```

객체의 위치를 초기화 할때 사용합니다.

### relative
요소를 상대적 위치로 이동을 합니다.

```css
div {
    position: relative;
}
```

> 예제코드: relative01.html
relative 속성이 부여되었다고 해서 현재의 위치에 아무런 변화가 없습니다.

### 위치이동
요소의 위치속성을 relative로 설정한 후에는 좌표의 이동이 같이 해주어야 합니다.
위치의 이동은 상하좌우 4방향으로 이동을 할 수 있습니다.
* top
* left
* right
* bottom

> 예제코드: relative02.html

`기존의 위치`로 부터 이동을 합니다.

> 위치이동은 상위 요소가 position 속성값이 없는 상태에서는
적용이 되지 않습니다.



### absolute
절대위치로 요소를 이동합니다.
만일, 절대위치를 적요한 요소의 상위요소가 relative가 되면,
relative 요소를 부모로 하여 기준좌표가 변경이 됩니다.

```css
div {
    position: absolute;
}
```

> 예제코드: absolute01.html

절대좌표가 적용되면, 요소는 레이어와 같이 중간에 뜬 상태가 됩니다.
따라서 위의 `~`과 아래 `~`이 같이 붙여져서 표현을 하게 되고.

위치를 이동할 수 있습니다.
기준점은 `브라우저`의 상단 좌측 입니다.


### fixed
요소를 브라우저의 특정위치에 고장하는 것을 말합니다.

relative와 absolute는 웹페이지를 기준으로 배치를 합니다.
반면에 fixed는 모니터의 브라우저 화면을 기준으로 고정배치를 합니다.





## 상호관계
relative와 absolute 와의 관계를 실습합니다.

> 예제코드: position41.html

absolute 속성을 이용하여 위츠를 이동해 봅니다.
> 예제코드: position42.html

브라우저의 기준으로 파란색 박스가 이동한 것을 볼 수 있습니다.

상위 div 요소에 relative 속성을 부여합니다.
> 예제코드: position43.html

바디 요소의 설정많큼 박스가 움직이게 됩니다.
상위 박스가 relative가 되면, 하위 absolute의 기준점은 상위 박스가 됩니다.

<br>




## 여러  요소를  원하는  형태로  배치하기
요소들을 원하는 형태로 배치하기 위해 가장 중요한 것이 포지셔닝(positioning) 개념


### position 속성 - 원하는 형태로 요소 배치하기
position 속성은 웹 문서 안의 요소들을 자유자재로 배치해 주는 속성

```css
position:속성 값;
```


* static : 요소를 문서의 흐름에 맞춰 배치합니다.
* relative : 이전 요소에 자연스럽게 연결해서 배치합니다.
* absolute : 원하는 위치를 지정하여 배치합니다
* fixed : 지정한 위치에 고정해서 배치합니다. 요소가 화면에서 잘릴 수도 있습니다


#### position：static 속성 - 문서의 흐름대로 배치하기

> position：static 속성을 사용할 경우 left나 top 속성을 사용해서 요소의 위치를 임의대로 지정할 수없습니다.

#### position：relative 속성 - 자연스럽게 배치하기
요소가 나타나야 하는 위치를 기준으로 상대적인 위치를 말합니다.
> left나 top 속성을이용해 요소의 위치를옮길 수도 있습니다.


#### position：absolute 속성 - 원하는 위치에 배치하기
문서 의 흐름과는 상관없이 left와 right, top, bottom 속성을 
이용해 원하는 위치에 요소를 배치할 수 있습니다.

#### position：fixed 속성 - 고정시키기
 position:fixed로 지정하면 일부 장치에서 요소가 지정한 위치에 고정되어 버립니다.

> 문서에서 요소의 위치는 position:absolute에서와 똑같이 계산









