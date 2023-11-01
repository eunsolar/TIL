
# 멀티미디어실습

## 2023-11-01
### 브랜치 병합
명령어: git merge
- merge란 융합하단 뜻으로 다른 브랜치 두 개를 합치게 하는 명령어다.
- 11월 1일 실습에서는 merge를 사용하기 위해서는 하나의 브런치를 먼저 스위치 한 다음 머지를 시켰다.
- 변경한 내용이 달라도, 수정한 포인트가 겹치지 않다면 두 개의 파일은 머지가 가능하다.
- 브랜치 병합시 충돌이 일어나지 않게 하려면 두 브랜치에서 수정한 코드가 겹치지 않아야 한다


## 2023-10-18
### 저장소
-일반 폴더와 저장소의 차이는 '.git' 숨김폴더가 없냐 있냐이다.
  -일반 폴더는 '.git' 숨김폴더가 없음
  -저장소는 '.git' 숨김폴더가 있음
- '.git' 숨김폴더를 삭제하면 커밋 이력 등도 같이 삭제됨

### 브랜치
- 브랜치 <-- 커밋을 포인터
- 이슈를 만들고, 이슈에 해당하는 브랜치를 생성한다.
  -'git branch' <-- 만들어진 브랜치 확인
  - 'git branch 브랜치명' 새로운 브랜치 생성
-작업을 시작할 땐, 생성한 브랜치로 전환(switch)함
  -'git switch 브랜치명'
  -'git chackout 브랜치명'

### 회사에서 일할 때 프로세스

1. 내가 할 일에 대한 설명이 담긴 '이슈'를 만든다.
  -이슈 트래커
2. 이슈에 해당하는 '브랜치'를 만든다.
  -git branch 브랜치명
3. 2번에서 만든 브랜치로 전환한다.
  -git switch 브랜치명
4. 1번에서 만든 이슈에 해당하는 작업을 수행한다.
5. 커밋 만든다
  -add, commit
6. 원격 저장소(origin)에 내가 작업한 내용을 PUSH한다
  -git push -u origin 브랜치명
7. 원격 저장소에서 내가 작업한게 잘 보이는지 확인한다.
8. PULL REQUEST를 생성한다.
  - merge (병합하다)


## 2023-10-04
### 스테이징 영역
- IT 프로젝트는 여러 파일을 동시에 다루게된다.
- 일반 문서 수정과 같이 '저장' 버튼 클릭 만으로 한번에 수정한 파일들을 저장하게 하면, 불필요한 파일들이 커밋에 포함되는 일들이 발생한다.
 - 예시
  - '.vs' : visual studio로 프로젝트 열었을 때 자동 생성되는 폴더
- 그래서 staging area 라는 영역을 따로 두고, 커밋에 포함시킬 코드(파일)만 스테이징 영역에 추가하게 한 다음, 커밋을 만든다.
 - 스테이징 영역에 파일을 추가할 때 쓰는 명령어 : 'git add 파일명'
### gitignore파일
- 루트 경로에 있는 '.gitignore' 파일은 버전 관리 하지 않을 파일의 목록을 관리하는 용도로 쓰인다.
- 사용하는 운영체제, 에디터, 프로그래밍 언어, SDK, 라이브러리 등의 종류에 따라 사람이 의도하지 않는 파일이 생성되는데, 이런 파일들은 버전 관리 대상이 아니므로 gitignore 파일에서 관리한다.
- 예시 : https://github.com/lettier/3d-game-shaders-for-beginners/blob/master/.gitignore
- 처음 프로젝트 세팅하는 사람은 여러 툴을 사용해 자동으로 gitignore 파일에 들어갈 내용을 생성한다
- 웹사이트 : 
  - 구글에서 'gitignore generator' 로 검색
  - https://www.toptal.com/developers/gitignore
- VSCode 익스텐션 : 
  - gitignore by  CodeZombie

## 2023-09-27
- commit이란? 
  - git의 기본 단위로, 논리적 변경이 있을 때 만듦 (사진찍기와 유사)
- commit 메시지
  - 코드 변경분을 한 마디로 설명함
- 명령어
  - git commit -m "커밋 메세지 입력"
  - git commit --message "커밋 메세지 입력"
- 얼마나 커밋을 자주 만들어야 하나
  - 너무 작지도, 크지도 않게 함
    - 커밋 단위가 너무 작을경우, 불필요한 커밋들이 생성됨
    - 커밋 단위가 너무 클 경우, 오류 났을 때 빠른 대응이 힘듬
    - 예시: 30분 안에 리뷰 가능하도록 커밋 크기 조절

