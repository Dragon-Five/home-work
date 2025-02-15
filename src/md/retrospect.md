# 1,2주차 회고

## Git 및 VS Code 설치

### 1. Git 설치

### 1.1. Git 다운로드

- **웹사이트**: [Git 공식 웹사이트](https://git-scm.com/)
- 최신 버전의 Git을 다운로드하려면, 본인의 운영체제에 맞는 설치 파일을 다운로드한다. 설치 파일이 `Windows`, `macOS` 있다.

### 1.2. 설치 과정

- **Windows**:
  - 설치 파일을 실행하고, 옵션 선택 화면에서는 모든 항목을 Check 후 Next를 선택한다.
  - Git에서 사용할 Default Editor를 앞으로 쓸 Visual Studio Code로 지정해주고 Git의 기본 브랜치를 master에서 main으로 변경해준다 변경이유는 master라는 용어가 역사적으로 노예제와 연관이있어서 부적절하다는 의견이 있어 바뀌게 되었다.
  - `Git Bash`와 `Git GUI`가 함께 설치됩니다. `Git Bash`를 사용하면 명령어 입력이 간편해진다.
- **macOS**:
  - macOS에서는 Homebrew를 이용해 설치하거나, Git 웹사이트에서 `.dmg` 파일을 다운로드하여 설치할 수 있다.

### 1.3. 설치 확인

git --version, git -v도 가능

---

### 2. **Git Bash** 에서 `tree` 명령어 사용

- Git Bash에서 `tree` 명령어라는 디렉토리 구조를 트리 형태로 시각적으로 보여주는 명령어 `Window`에는 기본적으로 설치가 되어있으나 Git Bash는 안되어있어 따로 설치해준다.
- Git Bash 실행후 tree 명령어 입력 그럼 자동설치를 진행한다.

### 2.1. 단축키 복사/붙여넣기 사용하기

- 화면 왼쪽 상단 우클릭하여 `Options` 항목으로 이동 후 `Keys` 선택한다.
- Ctrl + Shift + letter shortcuts 항목을 선택한 후 저장(save)한다.
- 복사 `Ctrl + Shift + C` / 붙여넣기 `Ctrl + Shift + V` 윈도우랑 다르게 `Shift`를 추가하여 복사 붙여넣기 기능이 가능하다.

---

### 3.NVM, Node 설치

- **웹사이트**: [설치 웹사이트] `https://github.com/coreybutler/nvm-windows/releases`
  - 스크롤을 내려 `Assets`부분의 `nvm-setup.exe` 파일을 다운로드한다.

### 3.1 설치과정

- 다운로드한 파일을 실행시켜 설치해준다.
- 설치 확인을 위해 Git Bash를 실행하여 명령창에 `nvm -v`를 입력하여 nvm 버전이 출력되는지 확인!
- Git Bash 명령창에 `nvm install lts`를 입력하여 Node 설치.

### 3.2 버전확인

- Git Bash 명령창에 `nvm on`을 입력하여 nvm으로 설치한 Node를 활성화 시킨다.
- 명령창에 `nvm list` 입력하면 설치된 Node 버전 목록을 확인할수 있다.
- 명령창에 `node -v`를 입력하면 설치한 버전을 확인할수 있다.

---

### 4.Cli (Command Line Interface)

### 4.1 CLI란?

- 사용자가 텍스트 명령어를 입력하여 컴퓨터와 상호작용하는 인터페이스. 그래픽 사용자 인터페이스(GUI)와 달리, CLI는 텍스트 기반으로 명령어를 입력하고 결과를 텍스트로 출력하는 방식.
- 시스템을 제어하거나 소프트웨어를 실행하는 데 유용

### 4.2 CLI 장점

- **빠른 작업 처리** : 텍스트 명령어로 빠르게 작업가능
- **스크립트 작성 가능** : 반복적인 작업을 자동화할 수 있는 스크립트를 작성할 수 있음
- **리소스 절약** : GUI보다 시스템 자원을 덜 사용
- **정밀한 제어** : 시스템을 더 세밀하게 제어할 수 있는 명령어와 옵션 제공

### 4.3 CLI 주요 명령어

1. **ls** (List Segments) 현재 디렉토리의 파일 목록을 출력한다

- `ls ~/Frontend/assets` : `Frontend/assets` 폴더의 하위 폴더 목록을 출력
- `ls -l ~/Frontend/assets` : 폴더 목록을 출력할 때 사용 권한, 소유자, 그룹, 크기, 날짜 등 상세 정보를 함께 표시
- `ls -a ~/Frontend/assets` : 폴더 목록을 출력할 때 숨겨진 항목을 포함하여 모든 내용을 출력
- `ls -al ~/Frontend/assets` : 폴더 목록을 출력할 때 숨겨진 항목을 포함하여 사용 권한, 소유자, 그룹, 크기, 날짜 등 상세 정보를 함께 표시

2. **cd** (change Directory) 디렉토리 변경 명령어

- `cd .` - 현재 디렉토리 (생략 가능)
- `cd ..` - 상위 경로로 한 단계 이동
- `cd ../..` - 상위 경로로 두 단계 이동
- `cd ~/Desktop` - 데스크탑 디렉토리로 바로 이동

3. **pwd** (print working directory) 현재 작업중인 폴더 확인

- 내가 작업중인 폴더를 확인하는 방법 `(자주 써야한다 내위치를 파악하기 위해)`

4. **mkdir** (Make Directory) 폴더 생성

- mkdir Five: 현재 폴더에 Five폴더를 생성

5. **touch** 빈 파일 생성

- touch 입력후 한칸 띄우고 만들고 싶은 이름 그리고 확장명을 써준다
- `touch hi.html` 명령어 사용시 내용이 비어있는 html 파일이 생성된다.

6. **echo** 간단한 내용을 포함한 파일 생성

- 예시로 echo 입력후 내용입력! >(사용시 텍스트를 추가해주는 기능) index.js
- 출력값은 내용입력! 이 텍스트가 index.js에 생성된다.

7. **cat** (Concatenate) 파일 내용 확인

- `cat js/index.js` : `index.js`파일의 내용을 화면에 출력
- `cat index.js app.js` : `index.js`파일과 `app.js`파일 내용을 모두 화면에 출력

8. **rm** (Remove ) 파일 비어있지않은 디렉토리 삭제

- `rm {제거할 파일/디렉토리 이름}`
- `rm index.html` = `index.html`파일 삭제
- `rm -r js` = js폴더 내부 하위 디렉토리까지 모두 삭제
- `$ rm -rf assets` = `assets`폴더 안의 하위 디렉토리까지 모두 삭제하되, 경고를 나타내지 않음 `f`(force)포스 강제실행 모드다 모든 상황을 무시한다.

9. **rmdir** (Remove Directory) `mkdir` 과 반대로 폴더를 제거하는 명령어

- `rmdir` = Remove Directory
- `rmdir {제거할 디렉토리 이름}`
- `$rmdir js`: `js` 폴더 삭제

10. **mv** (Move) 파일 디렉토리 이동 및 이름 변경 가능하며 이미 존재하는 파일/디렉토리의 경우 이름 변경 가능!

- `mv index.html views/index.html` = `index.html` 파일을 `views`폴더로 이동
- `mv js/index.js js/app.js` = `js` 폴더에 있는 `index.js` 파일명을 `app.js`로 변경

11. **cp** (Copy) 파일 디렉토리 복사

- `cp` = Copy
- `cp index.html main.html`:`index.html`파일을 동일한 폴더에 복사한 후 파일명을 `main.html` 로 변경
- `cp index.html views/main.html` :`index.html`파일을 `views` 폴더에 복사한 후 파일명을  `main.html` 로 변경

---

### 5.Git CLI

### 5.1 Git CLI 준비하기

- Git CLI를 사용하기 위해서는 Visual Studio Code에서 기본 쉘을 `zsh` 또는 `bash`로 설정하는 것이 필요합니다.
- Windows 사용자의 경우, Visual Studio Code에서 Git Bash를 기본 쉘로 설정해야 Git CLI를 사용할 수 있습니다. 아래는 이를 설정하는 방법.
- Visual Studio Code를 실행.
- 상단 메뉴에서 **View** → **Command Palette**를 클릭.
- **Select Default Profile**을 선택.
- 표시되는 옵션 목록에서 `Git Bash`를 선택.

### 5.2 Git 환경설정

- Git 사용자 ID 설정 git config --global user.name `"Dragon-Five"`
- Git config --global user.email `https://github.com/Dragon-Five`
- Git 기본 편집기 설정 git config --global core.editor `"code --wait"`
- Windows와 macOS의 줄바꿈(CRLF) 설정 git config --global core.autocrlf `true`, 줄바꿈 관련 경고 메시지만 숨기기 git config --global advice.ignoreCrLfWarning `true`
- 설정 확인 git config --list

### 5.3 Git 명령어

1. **git status** = 현재 상태 확인

- 변경된 파일명이 빨간색으로 보일 경우 Working Directory 상태
- 변경된 파일명이 초록색으로 보일 경우 Staging Area 상태
- nothing to commit, working tree clean의 경우 변경 내용이 없음을 나타냄

2. **git init** = 저장소 생성

- 현재 디렉토리를 Git 저장소로 생성
- .git 폴더(숨김 폴더)가 생성됨 (숨긴 폴더를 보려면 ls -a 사용하면 보인다)

3. **git add** = 파일의 변경 사항을 index(Staging Area)에 추가

- 특정 파일을 Staging Area에 추가하기
- 변경 내용이 있는 모든 파일을 Staging Area에 추가하기 `git add *`, `git add .`

4. **git restore** = 작업 내용 취소

- Working Directory에 변경 내용을 취소할 경우(Tracked File) `git restore <file>`
- Staging Area에 변경 내용을 Working Directory로 되돌릴 경우 `git restore --staged <file>`

5. **git commit** = 파일의 변경 사항에 대한 이력 생성

- 커밋 하기 `git commit -m "커밋 메시지"`
- 마지막 커밋 메시지 수정 `git commit --amend`
- VS Code에 COMMIT_EDITMSG 창에 수정할 커밋 메시지 입력 후 창 닫기
- commit은 정말 확정되었을때 보내자.. (마지막 커밋 메세지 수정을 놓친다면 뼈아플지도..)

6. **git rebase** git rebase -i <hash> = 특정 커밋 수정

- -i 몇번째 1~3 중 이동후 텍스트 폴더가 열리는데 pick -> reword로 수정한 후 커밋 메시지 수정 reword <hash> "수정할 커밋 메시지" 해준다.

7. **git log** = 커밋 이력 확인

- Log를 한줄, 그래프 형태로 보기 `git log --oneline`, `git log --oneline --graph`
- Log가 많을 경우 모두 출력하고자 할 때 `git config --global core.pager cat`

8. **git checkout HEAD~** = 과거 커밋 이력 확인

- 이전 2개의 커밋으로 이동 `git checkout HEAD~2`
- 특정 커밋으로 이동 `git checkout <hash>`
- 마지막 커밋으로 복귀 `git checkout main`

9. **git reset HEAD~** = 이전 상태로 복원(이력 제거)

- 이전 2개의 커밋으로 돌아가기 (--mixed : default)
- 커밋 기록은 삭제되지만 Working Directory에 변경 사항은 남김 `git reset HEAD~2`
- 커밋 기록은 삭제되지만 Working Directory와 Staging Area에 변경 사항은 남김 `git reset --soft HEAD~2`
- HEAD~2 커밋으로 복원되며 이후에 변경된 커밋 기록은 모두 삭제 `git reset --hard HEAD~2`
- 만약 돌아간 곳이 이미 커밋한상태라면 안된다

10. **git remote** = 리모트(Remote) 브랜치

- 리모트 브랜치 조회 `git remote -v`
- 리모트 브랜치 추가 `git remote add origin`, `https://github.com/ID/REPOSITORY`
- 리모트 브랜치 삭제 `git remote remove origin`, `git remote rm origin`

11. **git push** = 로컬의 변경 이력을 리모트로 전송

- 로컬의 main 브랜치의 변경 이력을 리모트 main 브랜치로 보내기 `git push origin main`

12. **git pull** = 리모트의 내용을 로컬에 반영 (fetch + merge) merge는 병합을 뜻한다.

- 리모트 main 브랜치의 변경 이력을 로컬 main 브랜치로 가져오기 `git pull origin main`

13. **git merge** = 브랜치 병합하기

- develop 브랜치를 main 브랜치에 병합 `git merge develop`
- 충돌(conflict) 시 mergetool을 활용해 해결
- config 설정에 mergetool 추가
  1. git config --global -e
  2. [merge]
  3. tool = vscode
  4. [mergetool "vscode"]
  5. cmd = code --wait $MERGED
