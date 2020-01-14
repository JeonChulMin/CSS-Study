# CSS Borders

- border properties는 element border의 style, width, color를 지정할 수 있다.



## CSS Border Style

```css
p {
	border-style: dotted;
}
```

| value  | 설명                                                         |
| ------ | ------------------------------------------------------------ |
| dotted | `.` (점) 선 경계선                                           |
| dashed | `-` 선 경계선                                                |
| solid  | 굵은 경계선                                                  |
| double | 줄이 2개인 경계선                                            |
| groove | Defines a 3D grooved border. The effect depends on the border-color value |
| ridge  | Defines a 3D ridged border. The effect depends on the border-color value |
| inset  | Defines a 3D inset border. The effect depends on the border-color value |
| outset | Defines a 3D outset border. The effect depends on the border-color value |
| none   | 경계선을 없게함                                              |
| hidden | 경계선을 숨김                                                |

- border-style property는 하나에서 4개의 vaule까지 가질 수 있다.
- (top border, right border, bottom border, left bordet)





## CSS Border Width

- border-width property는 위, 아래, 왼쪽, 오른쪽 경계선의 width(폭)를 정의한다. (경계선의 두께라고 생각하면 될 것 같다.)

- width는 구체적인 size로 설정(px, em, cm, em, pt, in, ..)되거나 또는 미리 정의되어 있는 3개의 값(thin, medium, thick)으로 설정된다
- border-width 속성은 1~4개의 value를 가질 수 있다.
- (top border, right border, bottom border, left border)





## CSS Border Color

- border-color property는 네 개의 경계선의 색을 설정할 때 사용된다.
- border-color property는 1 ~ 4 개의  value를 가질 수 있다.
- (top border, right border, bottom border, left border)





## CSS Border - Individual Sides

- 경계선의 네 부분 각자 설정할 수도 있다.

```css
p {
  border-top-style: dotted;
  border-right-style: solid;
  border-bottom-style: dotted;
  border-left-style: solid;
}
```

```css
p {
  border-style: dotted solid;
}
```

- 위 아래 같은 의미이다.

### 1) border-style 속성이 4가지 value를 가질 때

- border-style: dotted solid double dashed;
- top / right / bottom / left

### 2) border-style 속성이 3가지 value를 가질 때

- border-style: dotted solid double;
- top / right & left / bottom 

### 3) border-style 속성이 2가지 value를 가질 때

- border-style: dotted solid;
- top & bottom / right & left

### 4) border-style 속성이 1가지 value를 가질 때

- border-style: dotted;
- all four borders



## CSS Border - Shorthand Property

- border property는  shorthand property 이다.

1. border-width
2. border-style(required)
3. border-color

```css
p {
  border: 5px solid red;
}
```

- 또한 한 쪽 경계선에만 설정할 수 있다.

```css
p {
  border-left: 6px solid red;
  background-color: lightgrey;
}
```





## CSS Rounded Borders

- border-radius property는 요소의 경계선을 둥글게하고 싶을 때 사용한다.

```css
p {
  border: 2px solid red;
  border-radius: 5px;
}
```

- 값이 클수록 모서리 부분이 둥글게 된다.