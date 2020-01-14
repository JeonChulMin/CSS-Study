# CSS Backgrounds

- CSS Background properties는 elements의 배경에 효과를 정의할 때 사용한다.



## CSS background-color

- background-color property는 한 element(요소)의 배경색을 지정한다.

```css
body {
	background-color: gray;
}
```

- CSS에서 color는 아래와 같은 방법으로 사용된다.
  - a valid color name (ex) blue, red, ... )
  - a HEX value (ex) #fff000 )
  - an RGB value (ex) rgb(255, 255, 255))



## CSS background-image

- background-image property는 한 element의 배경에 이미지를 사용할 경우 사용한다.
- By default, the image is repeated so it covers the entire element.

```css
body {
	background-image: url("input url");
}
```



## CSS background-repeat

- 기본적으로 background-image property는 수직적, 수평적 모두 반복시킬 수 있다.
- 일부 이미지들은 의도하지 않게 가로, 세로로 이미지가 반복되어지는 것을 볼 수 있다.

- 만약 이미지가 수평적으로 반복된다면 `background-repeat: repeat-x;` 속성을 주면 된다. 그러면 배경에 한 이미지가 반복되지 않고 나타난다.

| 속성      | 설명                             |
| --------- | -------------------------------- |
| repeat    | 가로, 세로 방향으로 반복         |
| repeat-x  | 가로 방향으로 반복               |
| repeat-y  | 세로 방향으로 반복               |
| no-repeat | 반복하지 않는다.                 |
| initial   | 기본값으로 설정                  |
| inherit   | 부모 요소의 속성값을 상속받는다. |



## CSS background-position

- background-position property는 배경 이미지의 위치를 지정할 때 사용된다.

```css
body {
	background-image: url("input url");
	background-repeat: no-repeat;
	background-position: right top;
}
```

| 속성                 | 설명                             |
| -------------------- | -------------------------------- |
| x-position y-postion | 가로 위치와 세로 위치를 정한다.  |
| initial              | 기본값으로 설정.                 |
| inherit              | 부모 요소의 속성값을 상속받는다. |

- 가로 위치 값 : left, center, right, 백분율, 길이
- 세로 위치 값 : top, center, bottom, 백분율, 길이



## CSS background-attachment

- background-attachment property는 배경 이미지가 페이지 스크롤시 고정할 지 안할 지 지정할 수 있다.

```css
body {
	background-image: url("input url");
	background-repeat: no-repeat;
	background-position: right top;
    background-attachment: fixed;
}
```

- fixed : 스크롤시에도 항상 고정된 위치에 위치해서 스크롤해도 따라온다.
- scroll : 스크롤시 따라오지 않는다.



## CSS background - Shorthand property

- 코드를 짧게 하기 위해서 모든 background 속성들은 하나의 속성에 정의할 수 있다.
- 이를 Shorthand property라고 불린다.
- background 속성이 모두 정의하면된다.

```css
body {
  background: #ff0000 url("input url") no-repeat right top;
}
```

- shorthand 속성을 사용하는 경우 입력가능한 속성들은 아래와 같은 순서대로 기입하면 된다.

1. background-color
2. background-image
3. background-repeat
4. background-attachment
5. background-position

- 이 중 하나라도 누락되어도 괜찮다. 자동으로 그 다음 속성으로 적용된다.