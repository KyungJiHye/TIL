# 1-4. 수업 소개 목적 설치방법 목표

<br>
<br>
## 1. 수업 소개

<br>

- html 이 생기고 하나하나 코드를 쳐야하는데 불만이 생긴 개발자 들

  → 구글에서 v8 을 오픈소스로 공개

  → 이미 웹 개발자가 익숙했던 js 로 자동으로 html 작성하게 만들어주는 node.js 만듬

<br>
<br>

## 2. 수업의 목적

<br>

1. 생산성 
   - 현재 html 실습에서 진행한 파일은 목록 포함 4개의 링크를 가지고 있음 <br>
      (페이지가 1억개라고 가정) <br>
      순서가 없는 목록으로 바꿔달라고 요청할 경우 태그를 html 에 변경하러 가야함 <br>
      연결되어있는 html 모두를 변경해야하는 번거로움을 개선

<br>    

2.  사용자의 의견? 반영이 빠름
    - 읽기, 쓰기, 변경, 삭제 모두 웹을 통해 할 수 있음
    - 이로 인해 인터넷이 폭발적으로 성장

<br>
<br>

# 3. 설치 및 실행

<br>

1. Node.js runtime 프로그램 설치
    - javaScript 를 통해 Node.js Application 생성 

<br>

2. 설치 후 cmd 실행
    - node -v 입력하여 잘 설치됐는지 버전 확인
    - node 입력 시 javascript 언어로 cmd 창 조정가능
        - ex. console.log(1+1);
    - 나갈때는 컨트롤 c 두번 누르기

<br>

3. 사용할 폴더 만들기
    - 폴더 내 js 파일 생성 
      - 터미널 내 파일 생성 명령어 `vi 파일명` or 에디터로 폴더 내 파일 생성
    - cmd에서 생성한 js파일 있는곳으로 이동
      - `cd 파일or폴더 경로` 
    - dir 입력 : 현재 위치한 폴더의 존재하고 있는 목록 확인가능 
      - 파일이 위치한 dir 내에서 `node js 파일이름.js` 치면 해당 파일 실행 됨 

<br>
        
4. Linux & Codeanywhere
    - codeanywhere : 크로스 플랫폼, 클라우드 통합 개발 환경, 무료
        - 회원가입 - 컨테이너 생성(nodejs) - IDE 열기
        - 기본 창
            
            To access your web application make sure your application server is running and listening on 0.0.0.0 address on port 3000 and use the following link:
            
            > https://nodejs-white-jackal-k92270217324986.codeanyapp.com
            > 
        - 해당 부분이 외부에서 내 페이지에 접속할 때 입력하는 주소임
        - 나중에 다시 열고싶으면 커넥트되어있는 파일 우클릭 - info 클릭 시 확인 가능하다고 하는데 난 생활코딩님이랑 같은 화면이 안보임 뭔가 이상해…
        
        - 암튼 그냥 workspace에서 node.js 파일 만들어서 우클릭하니까 터미널 어쩌고 보여서 그거 키고 동영상 대로 하니까 되긴된다 그냥 ui가 바꼈나봄
            
            → 동영상에서는 node helloworld.js 라고 하면 실행됐지만 
            
            고사이에 명령어가 바껴서 .load helloworld.js 해야 실행 됐다. .help 채고

<br>
<br>           
        

# 4. 수업 목표

1. node.js로 만든 웹애플리케이션을 만든다. 
2. node.js 각각의 스텝마다 기능을 실행
3. 실행하기 위한 조작장치는 js 언어임 > 해당 문법 적당히 알려줌
4. 해당 문법을 통해 node.js 의 기능을 적당히 배울거임
5. 위를 반복