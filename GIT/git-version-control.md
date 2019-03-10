# git-version-control


## 버전컨트롤

*RCS - Revision control software*
패치셋을 보관한다.

*CVCS - centralized version control systems*
싱글서버에서 모든 버전의 파일들을 보관한다. 서버가 오프라인이거나 네트워크에 접속할 수 없는 상황에서는 사용할 수 없다.

*DVCS - distributed version control systems*
Git과 같이 분산 버전 컨트롤 시스템. 각각의 사용자가 로컬 저장소를 가지게 되어 네트워크 없이 사용가능하고 각각의 사용자의 로컬 저장소는 리모트 저장소의 백업역할을 할 수 있다.
사용자는 파일의 히스토리까지 포함한 파일의 모든 정보를 함께 복사하게된다.(clone)



## git은 무엇인가
리눅스를 만든 Linus Torvalds에 의해 만들어졌다.
SHA-1 hash라고 불리우는 중복검사(checksum)을 사용한다.(checksum은 중복 검사의 한 형태로, 자료의 무결성을 보호하는 방법이다. )


## git command
* `git config --list` - 깃 설정을 볼 수 있다.
* `git config --global user.name "Dahye Oh"` - 전역으로 유저 이름을 설정
* `git config --global user.email` - 이메일 설정
* `git help <verb: config, commit, ...>` - 해당 명령어의 매뉴얼 볼 수 있다.
* `git diff <filename>` - check the differences between the working directory and the staging area
* `git log` - view commits
* `git show HEAD` - 가장 최신 커밋을 볼 수 있다.
	* commit on are currently on is known as the `HEAD` commit , 가장 최신 커밋을 HEAD 커밋이라고 한다.
* `git checkout HEAD <filename>` - 가장 최신 버전으로 복구
* `git checkout -- <file>` - to discard changes in working directory)
* `git reset HEAD <filename>` - unstage file from the staging ares,  언스테이징.
* `git reset <commit_SH>` - 커밋 해쉬 앞7자리를 입력해 그 커밋으로 맞춘다.(이후 커밋은 없어진다)
* `git branch <branchname>` - create branch
* `git branch` - list branches
* `git push -u origin <branch:master, feature,…>` - 리모트 브랜치로 올린다 (-u를 함으로써 나중에 연결된 상태를 기억하고 git push / git pull 만으로도 그 브랜치와 연결된다)
* `git merge <branchname>`
* `git branch —merged` - merge된 브랜치를 나타냄
* `git branch -d <branch name>` - 해당 브랜치 로컬에서 삭제
* `git push origin --delete <branch name>` - 해당 브랜치를 리모트에서 삭제
* `git branch -a` - 전체 로컬, 리모트 브랜치 보기
