---
layout: post
title:  "border-radius 속성"
categories: css
---

## 개요
`border-radius` 속성은 요소의 테두리를 둥글게 만들어줍니다.
`px` 단위와 `%` 단위를 사용할 수 있으며, `border` 속성 없이도 사용할 수 있습니다.

총 4개의 모서리를 각각 다른 값으로도 줄 수 있습니다.
`margin` 및 `padding` 속성 처럼 4개의 값을 띄워쓰면 **왼쪽-위 부터 시계 방향**으로 각자 다른 값을 지정할 수 있습니다.


## 사용법
```css
#box{
	border-radius: 5px;
	border-radius: 1px 2px 3px 4px;
}
```


## 예제
```html
<html>
<head>
<style>
    .box{
        width: 150px;
        height: 80px;
		background-color: #039BE5;
		border: 2px solid #01579B;
		margin-bottom: 20px;
    }
	#box1{
		border-radius: 20px;
	}
	#box2{
		width: 80px;
		border-radius: 50%;
	}
	#box3{
		border-radius: 20px 0 10px 50px;
	}
</style>
</head>

<body>
	<div id="box1" class="box"></div>
	<div id="box2" class="box"></div>
	<div id="box3" class="box"></div>
</body>
</html>
```

