---
layout: post
title:  "text-align 속성"
categories: css
---

## 개요
`text-align` 속성은 텍스트의 정렬 방향을 의미합니다.

- `left`: 왼쪽 정렬
- `right`: 오른쪽 정렬
- `center`: 중앙 정렬
- `justify`: 양쪽 정렬 (자동 줄바꿈시 오른쪽 경계선 부분 정리)

## 사용법
```css
#box1 { text-align: right; }
#box2 { text-align: left; }
#box3 { text-align: center; }
```


## 예제
```html
<html>
<head>
<style>
	#box1 { text-align: right; }
	#box2 { text-align: left; }
	#box3 { text-align: center; }
</style>
</head>
<body>
	<div id="box1">오른쪽 정렬</div>
	<div id="box2">왼쪽 정렬</div>
	<div id="box3">중앙 정렬</div>
</body>
</html>
```