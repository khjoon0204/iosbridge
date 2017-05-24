# iosbridge

아이폰 - 웹 bridge javascript module  
[WebViewJavascriptBridge](https://github.com/marcuswestin/WebViewJavascriptBridge) 이용
<br />
<br />

## 필요한 것들

[jQuery](https://jquery.com/)

<br />
<br />

## 설치

```javascript
...
<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
<script src="iosbridge.js"></script>
...
```
<br />
<br />


## 사용법

```javascript

// 아이폰에서 메세지 받을때
$(iosbridge).on('ready', function(){

  iosbridge.recv(NAME, function(DATA, responseCallback){
		alert('WEB: received data = ' + data);
		
	});

});

//아이폰으로 메세지 보낼때
iosbridge.send(NAME, DATA, function(name, data, response){
  alert('WEB: send callback data = ' + data);
});

```

NAME(string): 웹과 아이폰 연결 키

DATA(string, array, json...): 키값 value
> EX) ['a', 'b', 'c'], ["k1":"v1", "k2":"v2"] 







