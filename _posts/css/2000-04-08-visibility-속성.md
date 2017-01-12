---
layout: post
title:  "visibility 속성"
categories: css
---

## 개요
`visibility` 속성은 태그의 가시성을 결정합니다.

아래의 4가지 값을 가지며, 기본 값은 `inherit` 입니다.

- `visible`: 보임
- `hidden`: 숨김 (자신의 영역은 계속 차지)
- `collapse`: 겹치도록 지정(테이블의 행과 열 요소만 지정할 수 있으며, 그 외 요소의 지정하면 hidden으로 해석)
- `inherit`: 부모 요소의 값을 상속


## 사용법
```css
#box1 { visibility: hidden; }
```


## 예제
```html
<html>
<head>
<style>
	.box{
		width: 100px;
		height: 100px;
		background-color: #09C;
	}
	#box1{ visibility: hidden }
	#box2{ visibility: visible }
</style>
</head>
<body>
	<div id="box1" class="box"></div>
	<div id="box2" class="box"></div>
</body>
</html>
```