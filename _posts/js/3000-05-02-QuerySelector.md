---
layout: post
title:  "QuerySelector"
categories: js
---

## 개요
JavaScript에서 **제어 대상**(문서 객체)를 찾기 위해서 몇 가지 함수를 제공합니다.  
적절한 제어 대상을 정하고 함수 호출을 하면 객체를 반환하게 되는데, 이 객체의 속성과 메소드를 통해 자바스크립트에서 문서를 동적으로 처리할 수 있습니다.

| 함수 이름                    						   | 요약                 | 반환값       | IE 지원  |
|--------------------------------------------------------|--------------------|------------|----------|
| [`getElementById`](#getelementbyid)                  | `id` 속성으로 검색     | 객체(한개)   | IE 7+   |
| [`getElementsByClassName`](#getelementsbyclassname) | `class` 속성으로 검색  | 배열(여러개) | IE 9+   |
| [`getElementsByTagName`](#getelementsbytagname)     | 태그 이름으로 검색      | 배열(여러개) | IE 7+   |
| `querySelector`              							| jQuery-유사 셀렉터     | 객체(한개)  | IE 8+   |
| `querySelectorAll`         						  | jQuery-유사 셀렉터     | 배열(여러개) | IE 8+   |


위 함수들은 글로벌 함수가 아닌 `객체 모델`에서 사용할 수 있는 함수입니다.  
즉, `getElementById` 함수로 이미 찾은 객체 내부에서 다시 `getElementsByClassName` 함수를 사용하는 식이죠.

문서 전체에서 객체를 찾을 시에는 `document` 전역 변수를 사용합니다.

querySelector 함수와 querySelectorAll 함수는 [jQuery 강의](/js-course/jQuery)를 참고 바랍니다.


### 사용법
```javascript
var mytext1 = document.getElementById('mytext1');
var containers = document.getElementsByClassName('container');
var images = document.getElementsByTagName('img');
var mytext1_1 = document.querySelector('#mytext1');
var containers = document.querySelector('.container');
```



## getElementById
### 예제

```html
<input id="mytext1" type="text">

<script type="text/javascript">
	var myText1 = document.getElementById('mytext1');
	myText1.value = Math.random();
</script>
```


## getElementsByClassName
### 예제

```html
<input class="rand-text" type="text">
<input class="rand-text" type="text">
<input class="rand-text" type="text">

<script type="text/javascript">
	var randTexts = document.getElementsByClassName('rand-text');

	for (var i = 0; i < randTexts.length; i++)
		randTexts[i].value = Math.random();

</script>
```

## getElementsByTagName
### 예제

```html
<select id="my-selector">
	<option></option>
	<option></option>
	<option></option>
</select>

<script type="text/javascript">
	var mySelector = document.getElementById('my-selector');
	var mOptions = mySelector.getElementsByTagName('option');

	for (var i = 0; i < mOptions.length; i++)
		mOptions[i].innerHTML = Math.round(Math.random() * 10000);

</script>
```
