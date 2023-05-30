# 목차

1. 깃과 깃허브란
1. 깃에 깃허브 인증정보 등록
1. 변경사항 기록
1. 깃허브에서 변경사항 받아오기
1. branch, merge
1. git flow
1. github 유용한 기능  

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

### 5.1 branch

1. 브랜치 생성 : cmd(로컬저장소) > `git branch [새로운 브랜치명]`
2. 브랜치 전환 : cmd(로컬저장소) > `git switch [전환할 브랜치명]`
3. 브랜치에서 작업(add, commit)

* 브랜치 목록 확인 : `git branch`

### 5.2 merge

1. 기존 브랜치로 전환 : `git switch master`
2. 브랜치 병합 : `git merge [병합할 브랜치]`

* 브랜치 삭제 : `git branch -d [삭제할 브랜치명]`

### 5.3 merge 이후

* merge 이후에도 브랜치는 사라지지 않음
* 기록용으로 남겨 놓기도 함
* 삭제하지 않으면 동명의 브랜치를 못 만듦
* 오래된 브랜치는 정리하는게 좋음

---

</details>


<details>
<summary><h1>6주차 - git flow</h1></summary>

> 협업을 위한 git branch 전략

### git flow에서 사용되는 브랜치(예시)
* Main (또는 Master): 제품의 실제 릴리스를 관리하는 메인 브랜치. 안정적이고 배포 가능한 상태의 코드만을 포함.
* Develop: 개발 중인 코드를 관리하는 브랜치. 새로운 기능 개발이나 버그 수정과 같은 작업을 수행하는 개발자들이 여기에서 작업을 진행.
* Feature: 새로운 기능을 개발하기 위해 사용되는 브랜치. 각각의 기능은 개별적인 브랜치로 생성되며, 개발이 완료되면 Develop 브랜치로 병합.
* Release: 제품의 배포를 준비하는 브랜치. 개발이 완료되고 테스트가 완료된 코드를 이 브랜치에 병합하여 배포를 준비.
* Hotfix: 긴급하게 수정이 필요한 버그를 처리하기 위한 브랜치. Main 브랜치에서 발생한 버그를 수정한 후, Develop 브랜치와 Main 브랜치로 병합하여 배포.

### 배민 git flow
[git flow 배민](https://techblog.woowahan.com/2553/)

---

</details>



<details>
<summary><h1>7주차 - github 유용한 기능</h1></summary>

### 7.1 markdown

* 마크다운(.md 또는 .markdown)이란 마크업 언어
* 깃허브에서 프로젝트를 설명하는데 사용

### 7.2 github page

* github에서 웹 사이트를 호스팅해주는 서비스
* 블로그를 올릴 수 있음(jekyll 지원)

### 7.3 .gitignore

* 무시할 파일을 지정하는 파일

---

</details>