# How To Add CSS

- HTML에 CSS를 적용시키는 여러 가지 방법에 대해서 알아본다.





## Three Ways to Insert CSS

#### 1. External CSS

#### 2. Internal CSS

#### 3. Inline CSS





## 1. External CSS

- 외부 디자인이 설정된 CSS 파일로 웹 사이트 전체의 디자인을 변경하거나 설정할 수 있다.
- 각각의 HTML page는 외부 style sheet file(CSS파일)를 반드시 <link> element를 사용해서 head section에 포함시켜야 한다.

```html
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" type="text/css" href="external.css">
</head>
<body>

<h1>** H1 TAG **</h1>

</body>
</html>
```



- external style  sheet는 어떤 text editor로 쓰여도 상관없다, 다만 저장시 `.css` 확장자로 저장해야 한다.
- 외부 .css 파일은 HTML tag를 포함하지 않아야한다. (ex) <head>)

```css
body {
  background-color: black;
}

h2 {
  color: red;
  margin-left: 10px;
}
```





## 2. Internal CSS

- Internal style sheet는 한 HTML page에 unique style이 적용할 때 사용되어진다.

- Internal style은 HTML의 head 태그 안 style 태그 안에 정의하면 된다.

```html
<!DOCTYPE html>
<html>
<head>
<style>
body {
	background-color: black;
}

h2 {
  color: red;
  margin-left: 10px;
}
</style>
</head>
<body>

<h1>** H1 TAG **</h1>

</body>
</html>
```





## 3. Inline CSS

- 하나의 inline style은 single element에 unique한 style을 적용할 때 사용된다.

- inline style을 사용하기 위해서는 사용할 HTML 태그에 style attribute를 추가해서 사용하면 된다.
- style attribute는 모든 CSS 속성을 포함할 수 있다.

```html
<!DOCTYPE html>
<html>
<body>

<h1 style="color:blue;text-align:center;">h1 inline style</h1>

</body>
</html>
```





## Multiple Style Sheets

- 만약 몇몇의 properties가 각각 다른 style sheet들에 같은 selector가 정의되어 있을 때 가장 마지막에 선언된 style sheet를 적용시킨다.

- 예를 들어 external style sheet & internal style sheet를 동시에 적용시켰을 경우를 알아본다.

#### [external style sheet]

```css
h1 {
  color: black;
}
```

#### [internal style sheet]

```css
h1 {
  color: red;   
}
```

#### 1) internal style이 external style 후에 선언되었으므로 internal style인 red가 적용된다.

```html
<head>
<link rel="stylesheet" type="text/css" href="multiple.css">
<style>
h1 {
  color: red;
}
</style>
</head>
```



#### 3) external style이 internal style 후에 선언되었으므로 external style인 black가 적용된다.

```html
<head>
<style>
h1 {
  color: red;
}
</style>
<link rel="stylesheet" type="text/css" href="multiple.css">
</head>
```





## Cascading Order

- 하나의 HTML element에 하나이상의 style이 정의되면 어떤 style이 적용되어질까?
- 한 페이지의 모든 style들은 다음 규칙에 따라 새로운 "virtual" style sheet로 "cascade(종속)"됩니다.

 

1. inline style (inside an HTML element)
2. External and internal style sheets (in the head section)
3. Browser default













