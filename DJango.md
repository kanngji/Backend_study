# migration 과 makemigtrations

: 테이블 및 필드의 생성, 삭제 , 변경 등과 같이 데이터베이스에 대한 변경 사항을 알려주는 것

클래스 모델을 만들고 makemigrations 명령어를 입력해서 데이터베이스 쪽에서 테이블을 생성할 수 있도록 migrate 하는 것

makemigrations: models.py에서 적용한 변경사항이나 추가된 혹은 삭제된 사항들을 감지하여 파일로 생성
migrate: 적용되지 않은 migrations들을(설정값들을) 적용시키는 역할

# CSRF

- Cross-site request forgery 공격의 약자로.
  사용자가 자기 의지와는 상관없이 공격자가 의도한 행위를 특정 웹사이트에 요청하게 하는 방식으로 수행하는 공격
  장고가 CSRF 토큰 값을 세션을 통해 발행하고 웹 페이지에서는 폼 전송시에 해당 토큰을 함께 전송하여 실제 웹 페이지에서 작성된 데이터가 전달되는지를 검증하는 기술이다.

# 한글입력이 가능한 데이터베이스 (MYSQL)

- 그냥 create database [이름]; 명령어로 데이터베이스를
  만들어서 한글데이터를 저장하려니 오류가 났다.
  https://yusang.tistory.com/49
