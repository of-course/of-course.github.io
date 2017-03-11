---
layout: post
title:  "EventListener"
categories: js
---

## 개요
`on 속성` 을 이용하여 이벤트를 등록시에는 이벤트 당 하나의 함수밖에 등록할 수 밖에 없습니다.  
`EventListener`를 이용하면 여러 이벤트를 등록할 수 있으며, 가장 권장되는 방식입니다.


- `addEventListener(eventType, listenerFunction)`
- `removeEventListener(eventType, listenerFunction)`
- `dispatchEventListener(event)`


## 사용법

```javascript
var myBtn = document.getElementById("my-btn");

// 클릭 이벤트 등록 (익명 함수)
myBtn.addEventListener("click", function (e) {
	alert("MyBtn Clicked");
});

function mbMouseOverHandler(e) {
	alert("MyByn MouseOvered");
	myBtn.removeEventListener("mouseover", mbMouseOverHandler); // 이벤트 삭제
}

// 마우스 오버 이벤트 등록
myBtn.addEventListener("mouseover", mbMouseOverHandler);
```




## Internet Explorer 예외처리
`addEventListener` 등의 함수는 IE9 이상부터 지원합니다.   
IE8은 `attachEvent` 함수가 존재하며, 그 이하 버전은 `onclick` 등의 속성을 사용해야합니다.

```javascript
function addEventListener(obj,evt,func){
	if ('addEventListener' in window)
		obj.addEventListener(evt,func, false);
	else if ('attachEvent' in window)
		obj.attachEvent('on'+evt,func);
    else
    	obj["on"+evt] = func;
}
```

위와 같은 함수로 대체할 수 있으나, IE 구버전 고려가 필요한 웹사이트라면 `jQuery`를 사용하는 것이 가장 편하며 안정적입니다.