### README.md
- 프로젝트에 대한 설명 문서

- Github 프젝에서 가장 먼저 보는 문서로 일반적으로 SW와 같이 배포함.
- 마크다운 형식 주로 사용


💡 **Repository**
- 특정 디렉토리를 버전 관리하는 저장소로 init 명령어로 로컬 저장소를 생성함.


- git init → initialized의 줄임말. git이 앞에 들어가면  git 명령어임
.git 디렉토리에 버전관리에 필요한 모든 것이 들어가 있음!
(숨김 파일)
- 특정 버전으로 파일을 남기는 것 → Commit 이라고 일컬음
**3가지 영역을 바탕으로 동작!**

![working directory : 작업 영역
staging area : 1차로 자료 올림
repository : commit 완료]![이미지](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7d2793c8-228c-4eb5-9ff4-6fe71060f2c6/2023-01-12-13-25-48-521.jpg)

working directory : 작업 영역
staging area : 1차로 자료 올림
repository : commit 완료

- 필수 GIT명령어

git add : working directory → staging 

git commit : staging→ repository

git status : 현재 상태 확인

`python

```jsx
SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/Python_pr
$ cd ..

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop
$ mkdir git_test  **# 경로 생성**
SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop
$ ls
 1학기/  '2반 신지원.md'   desktop.ini  'Eclipse IDE for Java Developers - 2022-09.lnk'*   git_test/   python_pr/   SPIKE-PRIME_Win10_2.0.9_Global.msi   Webex.lnk*                git_test/   python_pr/   SPIKE-PRIME_Win10_2.0.9_Global.msi   Webex.lnk*

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop
$ cd git_test **경로 변경**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test
$ git init **# git initialize**
Initialized empty Git repository in C:/Users/SSAFY/Desktop/git_test/.git/

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ ls -a **# 디렉토리 내 전체 파일 보기**
./  ../  .git/

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ touch README.md **#README 파일 생성**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status  
# 상태 보기 : 현재의 경우 commit 할 파일은 안올라왔으나 추가 가능한 파일이 있음을 알려줌
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git add README.md **#staging area로 파일 올림**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status **#상태 보니, 커밋 가능한 파일 알려줌**
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git commit -m "Add README.md"
Author identity unknown  **#git 저장한 사람의 이름과 이메일 작성**

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'SSAFY@DESKTOP-DOGVPUB.(none)')

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git config --global user.email "acd0825@naver.com"

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git config --global user.name "Jay"

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git commit -m "Add README.md"  **#git 커밋하고 설명글 작성**
[main (root-commit) 3ae580b] Add README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status
On branch main
nothing to commit, working tree clean
```

git에 올리기

```jsx
SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git remote add origin https://github.com/JayJayleee/git_test.git
**-> 원격으로 나의 주소에 git을 업데이트** 

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git remote -v
origin  https://github.com/JayJayleee/git_test.git (fetch)
origin  https://github.com/JayJayleee/git_test.git (push)
**-> 현재 git 에 저장된 저장소를 나타냄**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git push -u origin main
info: please complete authentication in your browser...
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 213 bytes | 213.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/JayJayleee/git_test.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
**-> git을 업로드 함**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git add README.md
**-> 스테이지에 git 추가**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
**$ git restore --staged  README.md  #스테이징 된 것을 다시 워킹 디렉토리로 내림**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git diff README.md
diff --git a/README.md b/README.md
index e69de29..a098547 100644
--- a/README.md
+++ b/README.md
@@ -0,0 +1,2 @@
+### 배드민턴 동아리 만들어서 운동해야지....
+## 집에 가고 싶다......
\ No newline at end of file

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
**$ git add README.md**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git push origin main
Everything up-to-date

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
**$ git commit -m "Edit README.md"  # 로컬 저장소에 기록 남김**
[main 2bedd6d] Edit README.md
 1 file changed, 2 insertions(+)

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
**$ git push origin main   # 허브에 업로드**
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 328 bytes | 109.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/JayJayleee/git_test.git
   3ae580b..2bedd6d  main -> main

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
**$ git log**
commit 2bedd6d6a9763588a4b4e60e7413b5ffa630918d (HEAD -> main, origin/main)
Author: Jay <acd0825@naver.com>
Date:   Thu Jan 12 14:29:37 2023 +0900

    Edit README.md

commit 3ae580b1697dd1340a26dc118af385f4f9b62392
Author: Jay <acd0825@naver.com>
Date:   Thu Jan 12 13:41:14 2023 +0900

    Add README.md
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/399c58b5-61b3-465e-8223-a2cd03646ecb/Untitled.png)

**업로드 과정**

```java
SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop
**$ rm -rf git_test  #파일 제거함**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop
**$ git clone https://github.com/JayJayleee/git_test.git
-> GIT 다시 복제** 
Cloning into 'git_test'...
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 9 (delta 0), reused 9 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.

```
`
- 이력이 필요 없을 경우에는 클론 대신 다운로드하여 최신 파일만 가져옴!