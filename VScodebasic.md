## 2일차 정리

- 오늘 배운 내용 정리 후, vscode 활용 github에 올리기

### git bash, typora, vscode 설치

데스크탑 -> 노트북으로 바꾸느라 처음부터 설치를 다시 진행했다. 초반 수업을 따라가는 것은 힘들었지만, 강의 막판에는 그래도 진도를 따라잡아 다행이었다.

- 설치의 경우 강사님의 notion을 참고하였다.
- [강사님NOTION](https://www.notion.so/hphk/push-rejected-1c3f94beddc24adfa6679636e5f79b6a) 을 눌러서 notion으로 이동.

### github

설치 한 뒤부터는 전날 수업 때 배운 내용을 토대로 금방 따라갈 수 있었다. 또한, github을 사용해본 경험이 있어 어느정도 수월했던 것 같다.

- github 을 통해 원격저장소 설정

  ```bash
  sangbeom@DESKTOP-77PB0UP MINGW64 ~/TIL (master)
  $ git init
  Initialized empty Git repository in C:/Users/sangbeom/TIL/.git/
  ```

- git remote

​	로컬저장소에 원격저장소를 `등록, 조회, 삭제` 할 수 있는 명령어

1. 원격 저장소 등록 및 확인

1. `git remote add <이름> <주소>` 형식으로 작성

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

2. 원격 저장소에 업로드

​	실습때 작성한 TIL파일을 Github 원격 저장소에 업로드

 * 파일을 업로드하는게 아니라 커밋을 업로드하는 것!

```bash
#현재 상태 확인

$git status

# 워킹디렉토리의 파일은 Tracked / Untracked 로 나눠지며, 새로 만드는 파일은 git에서 추적하지 않기 때문에 Untracked 상태이다.

$git add
# Untracked 파일을 git에서 추적하는 명령어 + 수정된 파일을 stage 상태로 바꿔주는 명령어

# add된 Tracked 파일은 Unmodified, Modified, Staged의  3개의 상태로 나눠진다.
# modified는 수정된 파일이 Tracked 상태이지만, Staged된 상태가 아니기에 git add 명령을 실행해야함을 나타낸다.

```


   