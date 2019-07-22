---
layout: post
title:  "background 속성"
categories: css
---

## 개요
`background` 속성은 태그의 배경을 지정하는 속성으로, [font 속성](/css-course/font-속성)과 비슷하게 세부적인 속성들을 한번에 쓸 수 있는 속성입니다.

아래의 세부적인 속성을 가집니다.

| [background-color](#background-color)      | 배경 색            |
| [background-image](#background-image)      | 배경 이미지         |
| [background-repeat](#background-repeat)    | 배경 이미지 반복 여부 |
| [background-position](#background-position)| 배경 이미지 위치     |


## background-color
배경색을 의미하며, 값은 [color 속성](/css-course/color-속성)의 포맷을 사용합니다.
> 태그의 크기가 없을 경우 배경색은 표기되지 않습니다.

### 예제
```html
<style>
	#box1-1{ background-color: green; }
	#box1-2{ background-color: #FF00CC; width: 200px }
</style>
<div id="box1-1">상자상자상자1</div>
<div id="box1-2">상자상자2<br>상자상자</div>
```



## background-image
배경 이미지를 설정하며, 주로 이미지 경로를 지정하는 방식으로 사용합니다.  
경로는 `background-image: url("이미지 경로")` 처럼 작성합니다.

특별한 점은 컨테이너의 크기와 상관없이 삽입된 `background-image`의 크기는 컨테이너에 맞춰 늘어나거나 줄어들지 않고 그대로 표시되며,  
이미지 보다 컨테이너가 더 크다면 이미지는 반복되어 표시되게 됩니다.


### 예제
```html
<style>
	#box2-1 {
		width: 100px;
		height: 100px;
		background-image: url("/images/attach/earth.jpg");
	}
	#box2-2{
		width: 300px;
		height: 150px;
		margin-top: 30px;
		background-image: url("/images/attach/earth.jpg");
	}
</style>
<div id="box2-1"></div>
<div id="box2-2"></div>
```

## background-repeat
`background-image`로 컨테이너보다 작은 이미지를 적용하면 이미지가 반복되어 출력됩니다.  
이때 `background-repeat` 속성을 사용하면 반복여부를 지정 할 수 있습니다.

### 예제
```html
<style>
	.abox{
		width: 500px;
		height: 100px;
		margin-bottom: 15px;
		background-image: url("/images/attach/android.jpg");
		border: 1px solid #AAA;
	}
	#box3-1{ background-repeat: no-repeat }
	#box3-2{ background-repeat: repeat }
	#box3-2{ background-repeat: repeat-x }
	#box3-3{ background-repeat: repeat-y }
</style>

<div id="box3-1" class="abox"></div>
<div id="box3-2" class="abox"></div>
<div id="box3-3" class="abox"></div>
<div id="box3-4" class="abox"></div>
```


## background-position
일반적으로 `background-image` 는 왼쪽 위부터 이미지를 출력합니다.  
`background-position` 속성을 사용하면 이미지의 좌표를 수정 할 수 있게 됩니다.

[margin, padding 속성](/css-course/margin-padding-속성)에서 지정했던 것과 비슷하게 띄어쓰기를 기준으로 x좌표, y좌표를 지정합니다.  
픽셀 뿐만 아니라 `left`, `top`, `center`, `bottom`, `right` 등의 상수도 쓸 수 있습니다.

### 예제
```html
<style>
	.abox{
		width: 500px;
		height: 100px;
		margin-bottom: 15px;
		background-image: url("/images/attach/android.jpg");
		border: 1px solid #AAA;
	}
	#box4-1{ background-position:center center; background-repeat: no-repeat }
	#box4-2{ background-position:30px right; background-repeat: repeat }
	#box4-3{ background-position:-100px -60px; background-repeat: repeat-x }
	#box4-4{ background-position:40px -90px; background-repeat: repeat-y }
</style>

<div id="box4-1" class="abox"></div>
<div id="box4-2" class="abox"></div>
<div id="box4-3" class="abox"></div>
<div id="box4-4" class="abox"></div>
```




## background

### 사용법
```css
#box{ background: #09C url('image.png') no-repeat 10px center; }
```


### 예제
```html
<html>
<head>
	<style>
		#box5{
			width: 300px;
			height: 100px;
			background: yellow url('/images/attach/google.png') no-repeat center center;
		}
	</style>
</head>
<body>
	<div id="box5"></div>
</body>
</html>
```