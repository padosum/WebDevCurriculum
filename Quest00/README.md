# Quest 00. 형상관리 시스템

## Introduction
* git은 2021년 현재 개발 생태계에서 가장 각광받고 있는 버전 관리 시스템입니다. 이번 퀘스트를 통해 git의 기초적인 사용법을 알아볼 예정입니다.

## Topics
* git
  * `git clone`, `git add`, `git commit`, `git push`, `git pull`, `git branch`, `git stash` 명령
  * `.git` 폴더
* GitHub

## Resources
* [Resources to learn Git](https://try.github.io)
* [Learn Git Branching](https://learngitbranching.js.org/?locale=ko)
* [Inside Git: .Git directory](https://githowto.com/git_internals_git_directory)

## Checklist
* **형상관리 시스템은 왜 나오게 되었을까요?**
  * 개발에 있어 편리함과 안정성을 높이기 위해 나오게 되었습니다. 소프트웨어 개발 프로젝트를 진행하면 여러 개발자들이 한 프로젝트를 함께 작업해야 하는 경우가 있을 때, 서로 수정한 코드가 무엇인지 알 수 없어 겹치는 코드를 작성하거나, 한 사람이 작업한 코드를 다른 사람이 없앨 수도 있습니다. 형상관리 시스템을 통해 소스코드를 해당 문제로부터 안전하게 관리할 수 있게되었고, 프로젝트 개발 과정에서 코드가 버전별로 관리가 되어 버그가 생겼을 때 개발 과정을 추적하거나 이전 버전으로 되돌릴 수 있게 되었습니다.
* **git은 어떤 형상관리 시스템이고 어떤 특징을 가지고 있을까요? 분산형 형상관리 시스템이란 무엇일까요?**
  * git은 분산형 방식입니다. 분산형 형상관리 시스템은 다른 방식인 중앙집중형 방식과 다르게 작업한 것을 다른 작업자와 함께 공유하는 중앙 서버로 바로 올리는 것이 아니라, 분산된 각각의 로컬에서 작업을 진행하고 서버로 올리고자 하는 내용을 로컬 저장소에 올려 이력을 관리할 수 있습니다. 그 후 최종적으로 중앙 서버에 업로드를 합니다. 
  * **git은 어떻게 개발되게 되었을까요? git이 분산형 시스템을 채택한 이유는 무엇일까요?**
    * git은 리누스 토발스가 리눅스 커널 개발 협업을 위해 다른 커널 개발자들과 함께 처음 개발하게 되었습니다. 분산형 시스템을 채택한 이유는 분산형 시스템의 장점 때문이라고 생각합니다. 분산형 시스템은 원격 저장소와 로컬 저장소가 완전히 분리되어, 동시에 여러 사용자들이 변경 작업을 수행할 수 있습니다. 큰 프로젝트에서도 다른 사용자와 충돌 없이 로컬 저장소에서 작업을 하거나 다른 사용자의 저장소와 브랜치 병합을 통해 협업할 수 있는 장점이 있습니다.
* **git과 GitHub은 어떻게 다를까요?**
  * git은 형상관리를 위한 소프트웨어이고, GitHub는 git 저장소, 즉 git으로 관리하는 프로젝트의 호스팅을 지원하는 서비스입니다.  
* **git의 clone/add/commit/push/pull/branch/stash 명령은 무엇이며 어떨 때 이용하나요? 그리고 어떻게 사용하나요?**
  * 우선 git으로 형상관리를 하는 작업 디렉토리 내 모든 파일은 다음 4가지 상태를 갖습니다.    
    * Untracked: 저장소에 이력을 추가하지 않은 파일 
    * Unmodified
    * Modified: 마지막 버전에서 변경된 파일
    * Staged: 새로운 버전에 반영될 준비가 된 파일
  * clone
    * `git clone <url>`
    * 원격 저장소 내용을 현재 디렉토리로 복사합니다.
  * add
    * `git add <file>` 
    * 명령에 Modified 상태인 파일을 전달하면 Staged 상태로 변경됩니다. (staging area로 옮겨짐) 
  * commit
    * `git commit -m "commit message`
    * 이력의 마지막 버전에 Staged 상태인 파일들을 반영해 새로운 버전을 생성합니다. commit message를 통해 어떤 작업을 했는지 확인합니다. 새로운 버전이 생성되면 파일들은 다시 Unmodified 상태로 돌아갑니다.
  * push  
    * 원격 저장소로 로컬 저장소의 변경 사항을 반영합니다.
  * pull
    * 원격 저장소의 데이터를 내 로컬 저장소로 가져와 병합합니다.
  * branch
    * `git branch <브랜치명>`: branch를 생성합니다.
    * `git branch`: 현재 branch 목록을 조회합니다. 
  * stash
    * `git stash`: 수정한 내용을 임시로 저장합니다.
    * `git stash pop`을 이용해 `stash`로 임시 저장한 내용을 다시 복구합니다. 
* **git의 Object, Commit, Head, Branch, Tag는 어떤 개념일까요? git 시스템은 프로젝트의 히스토리를 어떻게 저장할까요?**
  * [https://padosum.dev/How-Does-Git-Work](https://padosum.dev/How-Does-Git-Work)
* **리모트 git 저장소에 원하지 않는 파일이 올라갔을 때 이를 되돌리려면 어떻게 해야 할까요?**
  * `git reset`이나 `git revert` 명령을 사용합니다. 
    * `git reset`은 되돌린 버전 이후 버전이 모두 사라지고, `git revert`는 되돌린 버전 이후 버전은 유지되고 `revert` 되었다는 사실을 담은 commit이 새로 추가됩니다.  

## Quest
* [x] GitHub에 가입한 뒤, [이 커리큘럼의 GitHub 저장소](https://github.com/KnowRe-Dev/WebDevCurriculum)의 우상단의 Fork 버튼을 눌러 자신의 저장소에 복사해 둡니다.
* [x] Windows의 경우 같이 설치된 git shell을, MacOSX의 경우 터미널을 실행시켜 커맨드라인에 들어간 뒤, 명령어를 이용하여 복사한 저장소를 clone합니다.  
* [x] 앞으로의 git 작업은 되도록 커맨드라인을 통해 하는 것을 권장합니다.  
* [x] 이 문서가 있는 폴더 바로 밑에 있는 sandbox 폴더에 파일을 추가한 후 커밋해 보기도 하고, 파일을 삭제해 보기도 하고, 수정해 보기도 하면서 각각의 단계에서 커밋했을 때 어떤 것들이 저장되는지를 확인합니다.
* [x] `clone`/`add`/`commit`/`push`/`pull`/`branch`/`stash` 명령을 충분히 익혔다고 생각되면, 자신의 저장소에 이력을 push합니다.

## Advanced
* Mercurial은 어떤 형상관리 시스템일까요? 어떤 장점이 있을까요?
  * 분산형 형상관리 시스템입니다. 배우고 사용하기 쉬운 장점이 있다.
* 실리콘밸리의 테크 대기업들은 어떤 형상관리 시스템을 쓰고 있을까요?
  * Git
    * Google
    * Facebook
    * Microsoft
    * Twitter
    * LinkedIn
    * Netflix
  * Mercurial
    * Facebook
    * Mozilla
