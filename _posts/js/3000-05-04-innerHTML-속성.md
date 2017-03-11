---
layout: post
title:  "innerHTML 속성"
categories: js
---

## 개요
[QuerySelector](/js-course/QuerySelector)로 가져온 도큐먼트 오브젝트의 내용이나, 내부 HTML 코드를 JavaScript 코드에서 변경 할 수 있습니다.


## 예제
```html
<html>
<head>
	<script type= "text/javascript">
		function innerHTMLTest(){
			var randValNode = document.getElementById("rand-val");
			randValNode.innerHTML = "<b><font color='red'>"+Math.random()+"</font></b>";
		}
	</script>
</head>
<body>
	<div id="rand-val">Let's generate random Value</div>
	<button onclick="innerHTMLTest()">Generate</button>
</body>
</html>
```


## outerHTML
`innerHTML`과 비슷하지만, 선택된 노드를 포함하여 HTML를 수정합니다.



## innerText & outerText
`HTML` 코드가 그대로 입력되지 않으며, 텍스트로 입력됩니다.

### 예제
```html
<script type="text/javascript">
	function innerTextTest(target) {
		target.innerText = '<strong>click</strong>';
	}
</script>
<button onclick="innerTextTest(this)">Click This</button>
```


## 기타
`HTML`문자열을 그대로 삽입하는 방법 대신 `createElement` 등의 함수로 도큐먼트 객체를 만들고 `insertBefore` 등의 함수로 노드 객체 안에 다른 노드 객체를 삽입하며 `객체지향`처럼 사용하는 방법도 있습니다.