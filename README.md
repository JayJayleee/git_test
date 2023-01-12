# 마크다운

- 텍스트 기반의 가벼운 마크업 언어
- 문서의 구조와 내용을 같이 쉽고 빠르게 적고자 탄생

# 개발자로 성장하기
- 대체 어디서부터 시작해서 어디까지 해야 할까?
- python과 Java를 배우면 개발자가 되는걸까?
제일 중요한건 **꾸준한 학습**을 할 수 있는 사람인지를 보여줘야 한다!

[Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fdbf0a52-ac1a-495b-8410-a18e64f7cdc8/Untitled.png)

- **마크다운 활용 가능 기호**
    
    #헤딩
    
    - 문서의 제목이나 소제목으로 사용함.
    - #의 개수에 따라 제목의 수준을 구별(h1~h6)
    - 문서 구조의 기본
    - 글자 크기를 키우기 위해서 사용금지! (제목으로 구별함)
    
    # * /1.2.3 리스트
    
    - 순서가 있는 리스트와 순서가 없는 리스트로 나뉨
    - 목록을 표시하기 위해 사용
    - 많이 사용하는 태그 중 하나
    
    # ```text``` / `text` 코드블럭
    
    ```jsx
    ```text```의 예시
    ```
    
    ``text`의 예시`
    
    - 일반 텍스트와 달리 코드를 꾸며서 출력함
    - 개발자가 마크다운을 사랑하는 이유 중 하나.
    - 사용하는 프로그램에 따라 특정 언어를 명시하면 구문 강조 지원
    
    [title]([https://www.example.com](https://www.example.com/)) 링크
    
    - 다른 페이지로 이동
    
    # ![string](img_url) 이미지
    
    - 이미지 삽입에 사용
    - 너비와 높이는 조절 할 수 없음
    
    # **BOLD**, *Italic*, ~line~ 라인 등
    

**링크 참고**

[Markdown Cheat Sheet | Markdown Guide](https://www.markdownguide.org/cheat-sheet)

README.md
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
repository : commit 완료](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7d2793c8-228c-4eb5-9ff4-6fe71060f2c6/2023-01-12-13-25-48-521.jpg)

working directory : 작업 영역
staging area : 1차로 자료 올림
repository : commit 완료

- 필수 GIT명령어

git add : working directory → staging 

git commit : staging→ repository

git status : 현재 상태 확인