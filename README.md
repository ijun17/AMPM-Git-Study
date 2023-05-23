# 스터디 목차

1. 깃 & 깃허브
1. 깃에 깃허브 인증정보 등록
1. 변경사항 기록(add, commit, push)
1. 깃허브에서 변경사항 받아오기(pull)
1. branch & merge
1. 마크다운이란
1. github-page이란
1. .gitignore이란

---
<details>
<summary><h1>1주차 - 깃과 깃허브란</h1></summary>

### 1.1 Git & Github

> Git - 컴퓨터 **파일**의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 **분산 버전 관리 시스템**이다. 소프트웨어 개발에서 소스 코드 관리에 주로 사용된다. 

> Github - 깃허브는 깃 저장소 호스팅을 지원하는 **웹 서비스**이다.

### 1.2 Github를 사용하는 이유

1. 백업 용이성
2. 버전 관리
3. 협업 용이성
4. 오픈 소스 개발과 공유

---

</details>

<details>
<summary><h1>2주차 - 깃에 깃허브 인증정보 등록</h1></summary>

로컬에서 깃을 통해 깃허브에 변경사항을 올리기 위해선 깃에 깃허브 인증정보가 있어야함

### 2.1 용어

* 로컬 저장소(local repository) : 깃으로 관리되는 자신의 컴퓨터에 있는 저장소
* 원격 저장소(remote repository) : 깃허브로 관리되는 인터넷 세상에 있는 저장소

### 2.2 깃허브 인증정보 등록

cmd 또는 터미널을 켜서 다음을 입력(쌍따옴표도 입력해야함)

1. cmd > `git config --global user.name "이름"` : 깃허브 이름 등록
1. cmd > `git config --global user.email "이메일"` : 깃허브 이메일 등록
1. cmd > `git config --global user.password "비밀번호"` : 비밀번호 등록
1. cmd > `git config --list` : 이름,이메일,비밀번호 잘 입력되었는지 확인

---

</details>

<details>
<summary><h1>3주차 - 변경사항 기록</h1></summary>

### 3.1 로컬저장소-원격저장소 연결 

1. 원격저장소 만들기 : 깃허브 사이트 우측 상단 '+' 버튼을 눌러 'New Repository'를 클릭
1. 로컬저장소 만들기 : 작업 공간 안에 cmd(로컬저장소) > `git init`
1. 로컬에 원격저장소 등록 : cmd(로컬저장소) > `git remote add origin 원격저장소주소`

### 3.2 변경 사항 올리기

1. cmd(로컬저장소) > `git add .` : Staging Area에 변경사항을 추가
1. cmd(로컬저장소) > `git commit -m "커밋메시지"` : Staging Area에 있는 변경사항을 로컬저장소에 기록
1. cmd(로컬저장소) > `git push origin master` : 원격저장소에 변경사항을 기록

---

</details>

<details>
<summary><h1>4주차 - 깃허브에서 변경사항 받아오기</h1></summary>

원격저장소에 변경이 생길 경우

**fetch** : 변경사항 로컬저장소에 반영
* cmd(로컬저장소) > `git fetch origin`
* 작업 공간을 수정하려면 cmd(로컬저장소) > `git merge origin/main`

**pull** : fetch + merge
* cmd(로컬저장소) > `git pull origin master`

</details>

<details>
<summary><h1>5주차 - branch, merge</h1></summary>

여러 명이 동시에 개발을 진행할 때, 각자 복사본을 생성하여 작업을 진행하고, 작업이 완료되면 원본과 병합한다.

여기서 복사본을 `branch`라고 한다.

### 4.1 branch

1. 브랜치 생성 : cmd(로컬저장소) > `git branch [새로운 브랜치명]`
2. 브랜치 전환 : cmd(로컬저장소) > `git switch [전환할 브랜치명]`
3. 브랜치에서 작업(add, commit)

* 브랜치 목록 확인 : `git branch`

### 4.2 merge

1. 기존 브랜치로 전환 : `git switch master`
2. 브랜치 병합 : `git merge [병합할 브랜치]`

* 브랜치 삭제 : `git branch -d [삭제할 브랜치명]`

### 4.3 merge 이후

* merge 이후에도 브랜치는 사라지지 않음
* 기록용으로 남겨 놓기도 함
* 삭제하지 않으면 동명의 브랜치를 못 만듦
* 오래된 브랜치는 정리하는게 좋음

</details>