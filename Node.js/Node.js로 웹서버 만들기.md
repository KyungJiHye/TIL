# 5강 node.js 로 웹서버 만들기

<br>
<br>

- 웹브라우저에 주소 입력 → 요청 → 웹서버는 요청에 따른 정보를 웹 브라우저에 응답
    - 그 전에 공부한 건 Apache였음
- node.js  웹서버로의 기능 구현
- 하단 코드는 아직 뭔 말인지 모르겠지만 동일 유튜브 강의 내 html 과정에서 나온 결과물을 node로 실행 시킬 때 쓴 코드

<br>

```jsx
var http = require('http');
var fs = require('fs');
var app = http.createServer(function(request,response){
    var url = request.url;
    if(request.url == '/'){
      url = '/index.html';
    }
    if(request.url == '/favicon.ico'){
        response.writeHead(404);
        response.end();
        return;
    }
    response.writeHead(200);
		// __dirname : main.js 가 위치 하고 있는 디렉토리 위치 
    // url : 브라우저 내 해당 페이지의 url
		console.log(__dirname + url);
		// 프로그래밍 적으로 사용자에게 전송할 데이터를 생성한다
    response.end(fs.readFileSync(__dirname + url));
 
});
app.listen(3000);
```