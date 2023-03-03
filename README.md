# 테스트용 데이터베이스

# 실행 방법
0. database 레포와 backend 레포를 클론 받는다.
1. database 레포에에서 run_db.sh 입력   
   (bash run_db.sh)   

2. 기다리면 창이 뜨는데 url에서 :8082 앞 부분을 localhost로 변경   
   ex) 변경 전: 10.19.XXX.XXX:8082/login.jsp?sessionid=???   
       변경 후: localhost:8082/login.jsp?sessionid=???   


3. 로그인 세팅
   드라이버 클래스: org.h2.Driver   
   JDBC URL: (최초 생성 시) jdbc:h2:/\~/test   
(이후) jdbc:h2:tcp://localhost/\~/test   
   사용자명: sa   
   비밀번호: X   
   

3-1. 최초 생성 시 ~/ 경로에 test.mv.db 가 생겼는지 확인

3-2. 생기지 않았다면 touch test.mv.db로 생성

4. 연결 버튼 클릭

6. 실행 중인 DB 를 끄지 않은 상태에서 다른 터미널에 vi run_server.sh 입력후, backend 경로 수정

6. run_server.sh 실행   
   (bash run_server.sh)   

7. 테스트 하면 됨.
