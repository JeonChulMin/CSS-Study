# CSS Selectors

CSS selectors는 style을 주고자하는 HTML elements을 찾을 때 사용되어진다.

CSS selectors는 다섯 개의 카테고리로 나눌 수 있다.

### 1. Simple selectors (id, class, name)

### 2. Combinator selectors

- ex) div 태그 안의 p 태그에게 적용

```css
div p {
	background-color: yellow;
}
```

### 3. Pseudo-class selectors

- A pseudo-class is used to define a special state of an element.
- 요소의 특정 상태를 정의할 때 사용한다.
- 예를 들어 버튼 위에 마우스 커서를 올릴시에 색이 변한다거나, 입력창 클릭시 입력창 내부의 배경색이 바뀐다거나 등등을 말함.

### 4. Pseudo-elements selector

- A CSS pseudo-element is used to style specified parts of an element.
- 한 요소의 특정 부분의 스타일을 적용할 때 사용되어진다.
- 예를 들어 문장의 첫 문자 크기를 크게 하거나 특정 색을 적용할 경우

### 5. Attribute selectors

- HTML 안 설정된 attribute에 적용





# The CSS element Selector

```css
p {
	text-align: center;
	color: red;
}
```

- element selector는 HTML 요소 이름에 근거해서 사용한다.
- 모든 p 태그에 텍스트를 가운데 정렬하고 글자 색은 빨강으로 스타일을 적용하겠다는 의미이다.





# The CSS id Selector

- id selector는 HTML element 안에 id 속성을 부여해서 특정 element에 스타일을 부여하고 싶을 때 사용
- 한 element의 id는 unique 해야하고 id selector 또한 하나의 unique한 id를 사용해서 스타일을 부여한다.
- id selector는 `#id명` 형식으로 사용한다.
- 아래는 p 태그의 para1이라는 id 속성에 스타일을 부여, #para1으로 스타일 지정한 것을 볼 수 있음.

```html
<!DOCTYPE html>
<html>
<head>
<style>
#para1 {
  text-align: center;
  color: red;
}
</style>
</head>
<body>

<p id="para1">Hello World!</p>
<p>This paragraph is not affected by the style.</p>

</body>
</html>
```





# The CSS class Selector

- class selector는 HTML element 안 class attribute에 스타일을 부여, 보통 여러 태그들(공통된 스타일을 설정할 그룹이라고 생각하면 될거 같다.)에 적용할 때 주로 사용하는 것 같다.

- `.class명` 형식으로 사용, 주의할 점은 class명은 숫자로 시작할 수 없다.

- 아래는 HTML elements 안에 class 명이 center인 태그들에게 스타일을 부여.

```html
<!DOCTYPE html>
<html>
<head>
<style>
.center {
  text-align: center;
  color: red;
}
</style>
</head>
<body>

<h1 class="center">Red and center-aligned heading</h1>
<p class="center">Red and center-aligned paragraph.</p> 

</body>
</html>
```



- 아래와 같이 특정 태그 안 class에만 적용할 수도 있다.

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.center {
  text-align: center;
  color: red;
}
</style>
</head>
<body>

<h1 class="center">This heading will not be affected</h1>
<p class="center">This paragraph will be red and center-aligned.</p> 

</body>
</html>
```



- HTML element에 하나 이상의 class를 부여해서 사용할 수 있다.

```html
<!DOCTYPE html>
<html>
<head>
<style>
p.center {
  text-align: center;
  color: red;
}

p.large {
  font-size: 300%;
}
</style>
</head>
<body>

<h1 class="center">This heading will not be affected</h1>
<p class="center">This paragraph will be red and center-aligned.</p>
<p class="center large">This paragraph will be red, center-aligned, and in a large font-size.</p> 

</body>
</html>
```





# The CSS Grouping Selector

- grouping selector는 각각의 태그에 적용되는 스타일이 같을 경우 코드의 양을 최소화하기 위해 묶어서 사용할 수 있다.
- h1, h2, p 태그에 적용되는 스타일이 같으니 각 태그마다 코드를 만들 필요없이 묶어서 사용.

```css
h1, h2, p {
  text-align: center;
  color: red;
}
```



