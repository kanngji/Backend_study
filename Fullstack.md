# 풀 스택 개발의 정의
- 풀 스택 개발은 프론트엔드(클라이언트) 및 백엔드(서버 측) 개발을 모두 포함하는 웹 애플리케이션 개발 과정

역할
- 사용자 인터페이서 설계 및 구현
- 클라이언트 측 로직 개발
- 서버 측 구성 요소 개발
- 데이터베이스 관리
- 배포 및 유지 보수

# Django Rest Framework, React, Next.js 스택
- Python과 Javascript의 강점을 활용하여 확장 가능하고 고성능의
웹 애플리케이션을 구축하려는 개발자에게 인기

-DJango 이유
1. 빠른 개발
2. 확장성
3. 보안성

Django의 아키텍쳐
MVT : Model-View-Template

-React이유
1. 성능 React는 가상 DOM을 사용하여 렌더링 성능을 최적화하며
비용이 많이 드는 DOM조작을 최소화 하여 대량의 데이터를 다룰 때에도 사용자
인터페이스가 반응적인 상태를 유지할 수 있다.
2. 재사용성 React는 재사용 가능한 모듈화된 구성 요소의 사용을 장려하여
이를 프로젝트 간이나 대규모 팀 내에서 쉽게 공유할 수 있도록 하여 개발을 간소화하고
중복 코드의 필요성을 줄인다.
3. 유연성 React는 다른 javascript 라이브러리나 프레임워크와 함께 사용할 수 있으며, 오ㅓㅏㄴ전히 
다시 작성할 필요 없이 기존 프로젝트에 통합할 수 있다.
4. 생태계 React는 활발하고 다양한 개발자 커뮤니티로 구성

# DJango 프로젝트와 앱 구조 이해하기
- DJango는 코드베이스를 유지 가능하고 확장 가능하게 유지하기 위해
'프로젝트'와 '앱'이라는 개념을 사용합니다.
DJango 프로젝트는 전체 웹 애플리케이션을 나타내며, 앱은 프로젝트 내에서 특정한 기능을 제공하는 모듈
각 Django 프로젝트는 여러개의 앱을 포함할 수 있으며, 각 앱은 다양한 프로젝트에 연결될 수 있어 구성 요소의 재사용성을 촉진함
관리작업을 위한 명령 줄 유틸리티인 manage.py
전체 DJango 프로젝트의 구성을 담고 있는 settings.py 파일, URL을 기반으로
웹 요청을 라우팅하는 urls.py 파일 그리고 WSGI- 나 ASGI- 호환 웹 서버가
프로젝트를 제공하는 데 사용하는 wsgi.py 또는 asgi.py 파일
반면, Django 앱은 프로젝트의 특정 기능을 캡슐화하는 독립된 모듈입니다.
이는 데이터베이스 스키마를 위한 models.py 파일 비즈니스 로직을 담당하는
views.py 그리고 단위 테스트를 위한 tests.py 파일로 구성됩니다
앱은 앱별 URL 라우팅을 위한 urls.py파일 Django 관리자 인터페이스를 구성하기 위한
admin.py 파일 Django 폼을 정의하기 위한 forms.py 와 같은 추가 파일을 포함할 수도 있습니다

# Django 모델 소개
- Django에서 모델은 django.db.models.Model 클래스를 상속하는 Python 클래스
모델의 각 속성은 데이터베이스 필드를 나타냅니다.
Django는 이 모델을 위해 데이터베이스 스키마와 관리자 사이트 인터페이스를 자동으로 생성합니다.

# 모델과 필드 정의
- 예시) 블로그 글을 위한 모델

from django.db import models

class BlogPost(models.Model):
    title = models.CharField(max_length=200)
    content = models.TextField()
    published_date = models.DateTimeField(auto_now_add=Ture)

BlogPost 는 모델이며 title, content , published_date 세가지 필드를 갖습니다

# 모델 간의 관계 생성
- 일대일 , 일대다 및 다대다 관계를 정의 할수 있습니다.
- 예시) 애플리케이션에서 각 사용자마다 고유한 사용자 프로필을 가지고 있따
[일대일]
from django.db import models
from django.contrib.auth.models import User

class UserProfile(models.Model):
    user = models.OneToOneField(User, on_delete=models.CASCADE)
    bio = models.TextField()

[일대다]
class Comment(models.Model):
    post = models.ForeignKey(BlogPost, on_delete=models.CASCADE)
    text = models.TextField()

[다대다]
class Tag(models.Model):
    name = models.CharField(max_length=30)
    posts = models.ManyToManyField(BlogPost)

# 모델 마이그렝션과 데이터베이스 스키마 관리
- 마이그레이션은 모델을 변경할 때 (필드 추가, 모델 삭제) 해당 변경 사항을
데이터베이스 스키마에 전파하는 Django의 방법
마이그레이션은 대부분 자동화되지만 언제 마이그레이션을 생성해야 하고
언제 실행해야 하는지 그리고 발생할 수 있는 일반적인 문제를 알아야함

# Google Icon
- link
<!-- Variable icon font -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" />

