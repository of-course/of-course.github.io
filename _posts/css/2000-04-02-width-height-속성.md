---
layout: post
title:  "width,height 속성"
categories: css
---

## 개요
`width`와 `height` 속성은 각각 **가로 길이**, **세로 길이**를 의미합니다.

값을 정의 할때는 "**100px**" 처럼 숫자 뒤에 단위를 표시하여 적습니다.  
(px는 픽셀 이라는 의미의며 '50%' 처럼 '%' 단위를 사용 할 수도 있음)

`<span> 태그`등 `inline` 요소는 적용 되지 않는데, 이는 [display 속성](/css-course/display-속성)에서 다시한번 다룹니다.

## 사용법
```css
#box{ width: 100px; height: 60px }
```

## 예제
```html
<html>
<body>
	<div style="width: 150px; height: 80px; background-color: #d2f4ff; border: 2px solid #09c;">
		150x80
	</div>
	<div style="width: 60px; height: 200px; background-color: #fde6ff; border: 2px solid #90C;">
		60x200
	</div>
</body>
</html>
```
