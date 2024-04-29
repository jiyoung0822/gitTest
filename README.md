# gitTest
git bash 사용법
---------

- git init 로컬 저장소 생성(.git 폴더 생성)
- git status 현재 상태 확인 (빨간색은 스테이지 올라가기 전)
- git log 커밋 로그 조회
- git show 커밋 상세 정보 확인

- git remote add origin [원격 저장소 주소] 원격 저장소 연결
- git remote -v 원격 저장소 확인
- git remote remove [origin] 원격 저장소 삭제
- git pull origin main --원격 저장소 파일 받기
- git fetch 원격 저장소 등록

- git branch -M main 로컬 브랜치 생성
- git branch -m [현재 브랜치 명] [바꾸고싶은 브랜치 명]
- git branch -d main 로컬 브랜치 삭제
- git branch -v 모든 브랜치 확인
- git checkout main HEAD가 가리키는 브랜치 바꾸기
- git switch 브랜치 변경

- git add [파일경로] 스테이지 영역에 추가
- git restore --staged [파일경로] unstaged
- git commit -m '커밋메시지'
- git push origin main 원격 저장소에 저장
- git push origin --delete [삭제 브랜치명] 원격저장소 브랜치 삭제

- git merge [sub-branch name] 합치고 싶은 브랜치에 가서 머지
- pull request 생성 메시지 작성하고 create pull request

- rm -rf .git git init 취소하기
- git reset --hard ORIG_HEAD git pull 되돌리기
- git reset HEAD [파일명] git add 취소하기
- git reset --hard @^ 커밋 취소하기
- git remote rm origin 원격 저장소 연결 해제

> git push/pull 할때 fatal: refusing to merge unrelated histories 문제
- git pull --allow-unrelated-histories origin main

> 로컬 저장소에 등록하기(처음 시작)
- git clone [저장소주소] 원격 저장소에서 자료를 받아올 떄
- git checkout [브랜치명] 브랜치 변경

> 깃 클론하더라도 이클립스에서 프로젝트를 임포트해서 사용해야 한다.
- Import - Projects form Git - Existing local repository - 등록된 브랜치를 받는다.

> git clone은 아래와 같은 과정이 함축되어 있다.
- git init //로컬 저장소 생성
- git remote // 원격 저장소 url 복사해서 생성한 로컬 저장소에 등록하기
- git fetch // 원격 저장소에 있는 모든 branch들 로컬 저장소에 등록하기
- git checkout // main/master branch로 전환하기

> 과거의 커밋과 현재 파일을 비교
- git log로 커밋 로그 및 아이디 확인
- git diff  [최신 커밋아이디 네자리][비교하고 싶은 과거 커밋아이디 네자리]

> 깃 충돌 발생시 과거 내역으로 되돌리기(주의: 로컬 코드는 사라진다)
- git reset --hard HEAD~3
