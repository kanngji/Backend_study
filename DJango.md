# migration 과 makemigtrations

: 테이블 및 필드의 생성, 삭제 , 변경 등과 같이 데이터베이스에 대한 변경 사항을 알려주는 것

클래스 모델을 만들고 makemigrations 명령어를 입력해서 데이터베이스 쪽에서 테이블을 생성할 수 있도록 migrate 하는 것

makemigrations: models.py에서 적용한 변경사항이나 추가된 혹은 삭제된 사항들을 감지하여 파일로 생성
migrate: 적용되지 않은 migrations들을(설정값들을) 적용시키는 역할
