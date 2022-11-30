## Github page Build

### 1. 로컬 저장소 생성 : 프로젝트에 이용할 로컬 저장소를 생성한다.

  사용할 디렉토리를 하나 선택한다.
<br/>
  경로 : "C:\Users\doche\Desktop\gitblog\blog"

  cmd에 다음과 같은 명령을 실행한다.
<br/>
  $ git init
<br/>
  명령을 실행하면 .git 하위폴더가 생성된다.

### 2. 리모트 저장소 생성
<br/>
  Github에서 새로운 Repository를 하나 생성한다. <br/>
  Repo 이름 : docherryra.github.io
<br/>
  로컬 커밋을 리모트 저장소에 올릴 수 있도록 다음과 같은 명령을 실행한다.<br/>
  $ git remote add origin <url>
  <br/>
  url 주소 : https://github.com/docherryra/docherryra.github.io
  <br/>
  $ git remote -v 명령을 실행하여 연결 상태를 확인한다.
  <br/>

### 3. 로컬 저장소 - 리모트 저장 동기화
<br/>
$ git add
<br/>
$ git commit
<br/>
$ git push
<br/>
위의 명령을 실행하여 로컬 커밋을 리모트 저장소에 업로드한다.

----------------------
## Blog Build

1. jekyll과 Ruby 설치 (RubyInstaller)

2. 로컬 저장소에 jekyll 설치
$ jekyll new . --force 명령 실행
$ bundle install 명령 실행

3. 서버 실행 테스트
$ bundle exec jekyll serve
명령 실행 후 localhost:4000 주소에 접속하여 사이트가 원활하게 구동되는지 확인한다.

4. 테마 적용
Lanyon 테마를 설치한 후 로컬 폴더에 덮어씌워 테마를 적용시킬 수 있다.

-------------------
## 추가 기능 구현

### 1. 댓글 기능 추가
 - disqus 회원가입 후 웹사이트 생성 (jekyll platform 등 설정)
 - _config.yml 파일에 다음과 같은 key-value 추가
[![1](https://user-images.githubusercontent.com/104899885/204676617-36225006-3d89-44cd-b6ed-521370909803.png)](https://docherryra.github.io/)
 - disqus 홈페이지에서 Universal Code 복사
 - post.html 파일에 적용 (아래 사진 참고)
[![2](https://user-images.githubusercontent.com/104899885/204676615-b0590928-afb3-41fb-9e95-4b261d270178.png)](https://docherryra.github.io/)
 - 댓글 기능을 추가하고 싶은 포스트의 파일에 'comments:true' 추가
[![3](https://user-images.githubusercontent.com/104899885/204676606-756d6cec-16c8-4a6a-9451-3ad99ab0aa5f.png)](https://docherryra.github.io/)

### 2. 파비콘 변경

[파비콘 참고 자료](https://min9nim.github.io/2018/03/add-favicon/)

-원하는 파비콘 이미지를 다운받는다.
-로컬 폴더에 assets 디렉토리를 생성한 후 파비콘 이미지를 업로드한다.
- _config.yml 파일을 수정 : **asset_url: /assets** 추가
- head.html 파일에 파비콘 설정을 추가한다.
[![4](https://user-images.githubusercontent.com/104899885/204677174-86db5971-9350-4f4c-89f1-0d3e3df2a17a.png)](https://docherryra.github.io/)

### 3. Google Analytics
[구글 애널리틱스 참고 자료](https://infiduk.github.io/2019/11/05/google-analytics.html)

구글 애널리틱스 빌드 과정은 아래 포스트에 기술하였다.
[구글 애널리틱스](https://docherryra.github.io/jekyll/update/2022/11/27/googleA.html)
