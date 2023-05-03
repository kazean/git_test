# 처음 배우는 Git & Github 
## 0. Intro
1. 버전관리가 무엇인지
2. 버전관리가 무엇인지 들어보기만 했다
3. Git 기본 기능을 써봤다(commit, push, pull, merge, branch)
4. Git 동자 원리를 알고 있다(로컬 저장소, 스테이지, diff)
5. Git 심화 기능을 써봤다(rebase, cherry-pick, reset, revert, git-flow)
- GitHub을 써봤다: fork, pull equest, code review

## Ch01-01. 버전관리가 뭔가요
> 따로 조금씩 작업하다가 내가 원할 때 코드를 합칠 수 있는 방법
- Git
> 분산 버전 관리 시스템이다
- 버전 관리란 무엇인가?: 저장본
- 다수의 사람이 버전 관리를 해야 한다면
- 버전 관리 시스템: Git
> 원하는 시점마다 버전을 만들고, 이들 간에 자유롭게 이동할 수 있다.
- Git을 쓰러면 무엇이 필요한가요?: 개인 저장소, Cloud
- Git을 사용하는 두 가지 방법: CLI(Command Line Interface), GUI(Graphic User Interface)
- GitHub에 코드를 올리는 과정
```
1. 프로젝트 폴더에 '여기에 Git을 쓸꺼다!' 라고 명명: git init
2. 변경한 파일중 올리길 원하는 것만 선택: git add
3. 선택한 파일들을 한 덩어리로 만들고 설명 적어주기: git commit -m "message"
6. Github에 저장소 만들기
7. 내 컴퓨터에 프로젝트 폴더에 Github 저장소 주소 알려주기: git remote add origin <addr>
8. 내 컴퓨터에 만들었던 덩어리 Github에 올리기: git push
```

## Ch01-02. Git & Github 환경 설정하기
- Git, Git Bash 설치(CLI 환경 구축)
1. git 설치확인: git
2. git 설치

## Ch01-03. Github, VSCode 설치


## Ch02-01. Git 초기화와 로컬 저장소
git init
1. 원하는 폴더에 git 초기화를 하면 그대부터 가능: git init
2. git 초기화를 하면 .git이라는 숨겨진 폴더가 만들어진다: 로컬 저장소
3. 로컬 저장소에 내가 만든 버전 정보, 원격 저장소 주소 등이 저장된다.
4. 원격 저장소에서 내 컴퓨터로 코드를 받아오면 로컬 저장소가 자동으로 생긴다.
5. 한 폴더에 하나의 로컬 저장소만 유지해야 한다.
- 로컬 저장소 생성 실습
```
1. 내 컴퓨터에 boxiting-cat 폴더 생성
2. Git Bash로 만든 폴더에 들어가기
3. git init으로 로컬 저장소 생성
```

## Ch02-02. 첫번째 버전 만들기
- 덩어리가 뭐예요?: 커밋(Commit) = 하나의 버전
- 커밋으로 만들길 원하는 파일만 선택: 애드(add)
- 버전 생성 실습
```
1. README.md, index.html 파일 생성
2. 원하는 파일만 선택하기: git add README.md
3. 메세지를 달아 커밋으로 만들기: git commit -m "message"
4. 생성한 커밋 보기: git log
```
## Ch02-03. 만든 버전 GitHub에 올리기
git remote add, git push
- 원격 저장소에 GitHub에서 만들고 커밋 푸시하기: 푸시(push)
```
1. GitHub에 로그인해서 Boxiting 저장소 생성
2. 내 컴퓨터에 boxiting-cat 폴더에 Github 저장소 주소 알려주기: git remote add origin https://github.com/kazean/boxiting.git
3. 만든 커밋 푸시하기: git push origin main
4. GitHub 사이트에 올라간 커밋 확인
```

## Ch02-04. 다른 사람이 만든 저장소 받아오기
- 원격 저장소를 내 컴퓨터에 받아오기: 클론(Clone)
> 클론(Clone)을 하면 원격 저장소의 코드를 내 컴퓨터에 받아올 수 있습니다.  
로컬 저장소(.git 폴더)도 자동으로 생깁니다.
- 원격 저장소의 데이터 가져오기: 풀(pull)
> 문어도 물론 커밋을 만들어서 원격 저장소로 Push를 할 수 있습니다.  
(원격 저장소에 푸시 권한이 있는 경우)
- GitHub 저장소에 내 컴퓨터에 받아오기: 클론(Clone)
```
1. 내 컴퓨터에 boxiting-oct 
2. clone: git clone https://github.com/kazean/boxiting.git .
```
- 원격 저장소의 데이터 가져오기: 풀(pull)
> git pull origin main


## Ch03-01. 소스트리로 GUI로 Git 다지기
1. 커밋 객체에는 무엇이 저장되나요?
2. 두 사람이 병렬로 커밋을 만들고 싶으면 어떡하나요?
3. 두 사람이 만든 버전을 합칠 수 있나요?
4. 남이 만든 오픈소스에는 어떠헤 기여할 수 있나요?
- CH.3 에서 배울 내용
1. Git GUI인 소스트리로 로컬 저장소 추가하기
2. 애드(Add)와 커밋(Commit)이 무엇인지 스테이지 개념과 함께 이해
3. 브랜치(Branch)로 평행세계 나누기
4. 머지(Merge)로 두 브랜치 합치기
5. 두 브랜치가 충돌(Conflict) 났을때 해결하기
6. 예의바른 병합 요청(Pull request) 보내기
7. 남의 저장소 통째로 복제하기: 포크(Fork)
- Git을 사용하는 두 가지 방법, 이번엔 GUI

## Ch03-02. 그림으로 배우는 Add와 Commit
- Git에서 커밋이란?
> 1. 변경 사항의 모음(x), 최종 코드모음  
2. 다만 기존 커밋과 비교해서 변경된 파일이 아니면 '변경되지 않았다'고만 저장해서 용량이 무겁지 않다
>> !SVN은 이전 커밋과의 변경사항만 저장, 한 버전을 보려면 맨 처음 커밋부터 계산해야한다.(속도 느림)  
Git은 바로 이전 커밋만 보면된다(속도 빠름)
0. 맨 처음 로컬 저장소를 만들었을 때
- 로컬 저장소(.git)
> 스테이지  
README.md, app.js: 추적 안됨
1. 두 파일 스테이지에 올리기
> add / README.md, app.js: 스테이지됨
2. 스테이지 사진 찍어 남기기
> commit / README.md, app.js: 수정 없음
3. 커밋을 원격 저장소에 올리기: 푸시
4. app.js 수정, app.css 추가
> app.js: 수정함, app.css: 추적 안됨
4. app.js 수정, app.css 올리기(commit)
> README.md: 수정없음, app.js, app.css: 스테이징
5. 스테이지 사진 찍어 남기기: 커밋
> .: 수정없음
6. 커밋을 원격 저장소에 올리기
- 요약
1. Git으로 추적하는 파일의 4가지 상태
> `untracked, tracked(수정없음/수정함/스테이지됨)`
2. 작업공간(Working directory)에 있는 수정함/추적안됨 파일을 스테이지로 올려 스테이징됨 으로 변경한다.
3. 커밋을 하면 수정없을 상태로 돌아가서 다시 파일을 수정할 수 있다.

## Ch03-03. GUI로 add, commit, push, pull 하기
1. [boxiting-cat] 파일 수정 후 add, commit, push하기
2. [boxiting-oct] pull

## Ch03-04. 평행세계 나누기 - 브랜치(branch)
- 한 줄로 커밋을 쌓으면 둘이 겹치지 않나요?
> cat: 고양1-고양2-고양3-고양4  
oct: 고양1-고양2-고양3-문어A
- 여러 줄로 커밋을 쌓는다?
> `똑같은 코드를 동시에 고칠 가능성 > 여러 브랜치, 추후 결합`
- 브랜치(Branch - 가지) 개념
> git push origin main  
master 브랜치에 커밋을 푸시해라, HEAD: 내가 지금 작업하는 로컬 브랜치를 가리킴
- 브랜치 만들기
> `git branch cat  `
cat 브랜치를 현재 시점에 만들어라
- 만든 브랜치로 이동하기
> `git checkout cat`, HEAD가 옮겨짐
- cat 브랜치에 커밋을 추가하면?
> main 브랜치는 과거를 가르키고, cat은 현재 상태
- main로 이동하고, oct 브랜치 만들고, 커밋
- 브랜치 생성 실습
```
1. [boxiting-cat 저장소] main에서 feat/main-page 브랜치 생성
2. 커밋추가
3. [boxiting-oct 저장소] pull 받기
4. main에서 feat/comment 브랜치 생성
5. 커밋추가
```

## Ch03-05. 두 버전 합치기 - 머지(merge)
- feat 브랜치에서 작업이 끝났어요! 이제 main에 합치고 싶어요
> `main 브랜치의 최신 커밋(base) oct 브랜치의 최신 커밋(compare)를 합치려고 한다`
1. 먼저 base가 될 main 브랜치로 이동
2. compare 브랜치인 oct를 나와 합치고 싶다고 명령
> `git merge oct`
3. 합쳐진 결과는 문어A 커밋

# Ch003-06. 합치다 충돌이 났어요 - 컨프릭트(Conflict)
- 두 문어 그립의 합집합을 구하기
> 1. 빨리 감기 됨(Fast-forward)  
2. 머지 커밋 생김(Merge commit)  
3. 충돌남(Conflict)
- Caase 1: 빨리 감기 된 머지
> main에 oct브랜치 합침
- Case 2-a: 새로운 커밋 만들어지는 머지
> main에 cat 브랜치 합침
- Case 2-b: 만약에 충돌이 났다면
> main에 cat을 합침(conflict)
- 컨플릭트 해결
> 머지할 때 두 버전이 같은 곳을 수정했다면 이를 수동으로 고쳐줘야 한다
```
<<<< HEAD
2. 스파링 좋아요 (base)
====
2. 스파링 싫어요
>>>> cat 브랜치
```
> 
```
2. 싫은데 좋아요
```
- 머지, 컨플릭트 해결 실습
```
1. [boxiting-oct] feat/comment로 이동 후 '스파링 좋아요' 수정
2. main에 feat/comment 수정본 머지 (머지 커밋 생성 확인)
3. [boxiting-cat] feat/main-page로 이동 후 '스파링 싫어요' 수정
4. main에 feat/main-page 수정본 머지(컨플릭트)
5. 컨플릭트 해결
```

## Ch03-07. 저장소 통째로 복제하기 - 포크(fork)
- 푸시 권한이 없는데 어떻게 기여하지?
> Collaborators, 커밋 전에 반드시 컬래버레이터 등록을 부탁해야 할까요?
- 포크(fork): 저장소를 통째로 복제
> 1. 고양&문어의 Boxiting 저장소를 통째로 너구리의 계정에 복제해와서  
2. 그 저장소(내꺼)에 자유롭게 커밋, 푸시를 하고  
3. 내 저장소의 브랜치와 고양&문어 저장소의 브랜치를 머지해달라고 요청
- 포크(fork): 저장소를 통째로 복제
- 브랜치 vs 포크
> 두 가지 모두 코드를 협업하기 위해 분기점을 나누는 방식이지만 특성이 다르므로 내 프로젝트에 맞게 사용
- 포크 실습
```
1. GitHub에 새로운 계정 만들기(너구리 포크 실습용)
2. Boxiting 저장소 포크
3. 포크한 저장소 크론
4. 소스트리에 새 계정 추가 및 디폴트 계정으로 설정
5. 좋아요 기능 만들고 커밋, 푸시
6. GitHub에 커밋 확인
```

## Ch03-08 내 코드를 머지해주면 안되겠니 - 풀 리쿼스트
- 이 커밋이랑 저 커밋으 합치는걸 허락해줘!: 풀 리퀘스트
1. 머지하고 싶은 두 브랜치를 선택하고
2. 어떤 변경을 했는지 제목과 내용에 쓰면 됩니다.
3. 단일 저장소에서 보낼 수도 있고, 이렇게 포크한 저장소에도 보낼 수 있습니다.
- 언제쓰냐
1. 직접 머지하는건 피하고 모든 머지를 풀 리퀘스트를 통해서 하세요
2. 동료가 내 풀 리퀘스트(PR)을 보고 코드를 리뷰할 수 있습니다.
3. 동료의 PR에 수정이 필요하면 댓글을 달아 change request를 보낼 수 있습니다.
4. 오픈소스에 PR을 보낼때는 '기여 안내문서(contribution guideline)'을 반드시 참고해야 합니다.
- 풀 리퀘스트 실습
1. 너구리가 포크한 저장소에서 고양이&문어 저장소로 풀 리퀘스트 보내기
> racoon: new pull request, compare/base 명시(racoon/master > cat/master)  
create pull request, Able to merge(conflict가 나지 않는다는 것을 명시)
2. 고양이 아이디로 로그인해서 풀 리퀘스트 수락 후 머지하기
> Pull request > Files changed > Review changes > Comment/Approve/Request changes > Merge pull request

## Ch03-09 다지기
- git 추가기능
1. rebase: 묵은 커밋을 새 커밋처럼 조작하고 싶어요
2. ammend: 커밋에 살짝 추가
3. cherry-pick: 저 커밋 하나만 떼서 지금 브랜치에 붙이고 싶어요
4. reset: 옛날 커밋으로 시간을 돌리고 싶어요
5. reverse: 이 커밋의 변경사항을 되돌리고 싶어요
6. stach: 변경사항을 잠시 킵해두고 싶어요. 아직 커밋은 안 만들래요