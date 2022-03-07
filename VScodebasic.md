## VScode를 사용해 Github 관리하기

### git bash, typora, vscode 설치

설치의 경우 구글링을 통해 쉽게 할 수 있음

### github

- github 을 통해 원격저장소 설정

  ```bash
  sangbeom@DESKTOP-77PB0UP MINGW64 ~/TIL (master)
  $ git init
  Initialized empty Git repository in C:/Users/sangbeom/TIL/.git/
  ```

- git remote

​	로컬저장소에 원격저장소를 `등록, 조회, 삭제` 할 수 있는 명령어

1. 원격 저장소 등록 및 확인

2. `git remote add <이름> <주소>` 형식으로 작성

   ```bash
   [등록]
   git 명령어를 작성할건데, remote(원격 저장소)에 add(추가) 한다. origin 이라는 이름으로 내 github 주소를 입력한다.
   
   $git remote add origin https://github.com/dr0beom/TIL.git
   
   [확인]
   $git remote -v 
   origin https://github.com/dr0beom/TIL.git (fetch)
   origin https://github.com/dr0beom/TIL.git (push)
   
   [삭제]
   git 명령어를 작성할건데, remote와의 연결을 re(remove)할거고, 그 remote의 이름은 origin 이다.
   $git remote rm origin
   ```

   원격 저장소에 업로드

​	실습때 작성한 TIL파일을 Github 원격 저장소에 업로드

 * 파일을 업로드하는게 아니라 커밋을 업로드하는 것!

```bash
현재 상태 확인

$git status

워킹디렉토리의 파일은 Tracked / Untracked 로 나눠지며, 새로 만드는 파일은 git에서 추적하지 않기 때문에 Untracked 상태이다.

$git add

Untracked 파일을 git에서 추적하는 명령어 + 수정된 파일을 stage 상태로 바꿔주는 명령어

add된 Tracked 파일은 Unmodified, Modified, Staged의  3개의 상태로 나눠진다.
modified는 수정된 파일이 Tracked 상태이지만, Staged된 상태가 아니기에 git add 명령을 실행해야함을 나타낸다.

```
  $git add 의 경우 staging area에 모아놓는 역할일 뿐, commit을 하기 전까지는 Git directory에 영향을 미치지 않는다.

```bash
$git commit -m "message"
를 통해 staging area에 있는 것들을 commit할 수 있다.

실수로 message 입력없이 git commit 만 한 경우, esc를 누른후 :wq enter을 하면 빠져나올 수 있다.

$git log
를 통해 commit log를 확인할 수 있으며, q 로 빠져나올 수 있다.
```

 - $git push 를 통해 commit 된 파일을 github에 반영
```bash
$git push
```

## 기타 정보

```bash
[이름바꾸기]
탐색기의 이름을 우클릭한 후 변경이 가능하지만, git status를 해보면 deleted로 파일이 뜨는 것을 볼 수 있다. 이 경우 

$git rm "파일이름"
을 실행하여 삭제해준다면 git status 결과 renamed 되었음을 확인할 수 있다.
```