# HM Backend Server

23.11.28 사이트 만들기 시작

---

> 오랜만에 pull 받거나 뭔가 꼬여서 안된다 그러면 아래처럼 다시 해야함(순서 다시 수정)

> 깃에서 새로 받아서 다시 할때는 poetry.lock, pyproject.toml 삭제 후(db.sqlite3 있으면 이것도 삭제)

> > poetry init -> enter x4 -> 라이센스는 MIT -> enter -> no x2 -> 마지막은 yes

> > > (가상환경에 들어가서 장고 시작) -> poetry shell

> > > (** 처음 설치할때는 **) -> django-admin startproject config . -> (runserver 하고 -> db생성 -> 마이그레이션 -> suer 생성 순으로 해야함)

> > > > (장고 설치) -> poetry add django

> > > > > (image를 가져오기 위해서 pillow 설치) -> poetry add pillow

> > > > > > (장고 레스트 프레임워크 사용) -> poetry add djangorestframework

> > > > > > > (토큰 사용) -> poetry add pyjwt

> > > > > > > > (.env 파일 읽는거 도와주기 위해) -> poetry add django-environ

> > > > > > > > > (서버에서 fetch 가능 하도록 하기 위해) -> poetry add django-cors-headers

> > > > > > > > > > (requests 설치) -> poetry add requests

> > > > > > > > > > > (에러가 나고 admin 페이지에 접속 안될텐데 마이그레이션\_db의 state 변경 해야해서 그럼) -> control + c 로 서버 끄고 -> python manage.py migrate -> (만약 안된다면 마이그레이션, 디비 다 삭제하고) -> python manage.py makemigrations -> python manage.py migrate

> > > > > > > > > > > > (admin 페이지 로그인 하려면 슈퍼 유저 만들어야함) -> python manage.py createsuperuser -> user name, email 그냥 엔터x2 -> 비밀번호는 그냥 123456 -> y

> > > > > > > > > > > > > 이 순서로 해야 정상 작동함(물론 기존 파일과 다른점 있는지는 확인 해야함) / 데이터 베이스는 깃에 없으니 다시 슈퍼유저 만들어야 하는거고!

> > > > > > > > > > > > > > (서버 시작 - poetry shell 로 가상환경에서 시작해야함) -> python manage.py runserver

---
