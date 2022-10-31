# 9강. URL

<br>
<br>

## 9. URL의 이해

<br>

- 서버를 생성, 버튼을 눌렀을 때 달라지는 페이지들은 다 각각의 정적인 html 페이지들을 불러오는 것
    - 이렇게 할 경우 페이지가 달라질 때마다 정적인 html을 다 가지고 있어야한다.
    - 보통의 사이트들은 사이트 내에 어떤 부분만 데이터가 변함
        - t 값만 변경되는 경우를 예시로 보여줌
        - node 앱이 클라이언트 앱브라우저에게 서로 다른 페이지를 보내는 것

<br>
<br>
    

        >http://opentutorials.org:3000/main?id=HTML&page=12

<br>

- http  : protocol
    - 웹 브라우저와 웹 서버가 데이터를 주고 받으기위해 만든 통신규칙 (사용자가 통신할 때 어떤 방식으로 통신하는가)
    - hyper text transper
- opentutorials.org
    - host(domain name) 인터넷에 접속되어있는 각각의 컴퓨터
    - org : 특정한 인터넷에 연결되어있는 컴퓨터를 가르키는 주소
- 3000 : 포트번호
    - 한대의 컴퓨터안에 여러개의 서버가 있을 경우 클라이언트가 접속시 어떤서버와 연결할지 애매하기 때문에 숫자를 지정해서 해당 숫자의 서버와 연결하기로 함을 명시한 것
    - 80 : 웹서버는 80번포트를 쓰는게 약속되어있음. http를 통해 접속 = 웹서버로 접속한 것
        - 디폴트가 80이다 생략해도 됨
- main : path
    - 어떤 디렉토리의 어떤 파일인지 가르킴
- id=HTML&page=12 : query string
    - 이 수업의 주인공, 페이지의 값을 변경 시 웹서버에 데이터를 전달해서 원하는 페이지를 불러옴
    - 시작은 ? , 값과 값은 & 로 연결, 이름과 값은 =로 구분

<br>
<br>

## 10. URL을 통해서 입력된 값 사용하기

<br>

- id 값이 무엇이냐에 따라 페이지를 다르게 보여주는 방법

<br>

```jsx
var http = require('http');
var fs = require('fs');
// url 모듈을 사용할거다 require : 요구한다
var url = require('url');

var app = http.createServer(function(request,response){
// id 값은 request.url로 들어간다.
// 해당 id 값을 추출해내면 id에 따라 다른 화면 출력이 가능해진다
var _url = request.url;
var queryData = new URL('http://localhost:3000' + _url).searchParams;
console.log(queryData.get('id'));
if(_url == '/'){
url = '/index.html';
}
if(_url == '/favicon.ico'){
response.writeHead(404);
response.end();
return;
}
response.writeHead(200);
//console.log(__dirname + url);
//사용자가 접속한 url에 따라서 파일들을 읽어주는 곳
response.end(queryData.id);

});
app.listen(3000);
```