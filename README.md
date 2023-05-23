# 스터디 목차

1. 스터디 소개 / 깃이 무엇인지(깃과 깃허브 차이)
1. 깃 설치 및 깃허브와 연동
1. 깃허브에 변경사항 올리기(commit, push)
1. 받아오기(pull)
1. branch 및 merge
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
<summary><h1>2주차 - 깃과 깃허브 연동</h1></summary>

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

### 3.1 원격저장소 등록

1. 원격저장소 만들기 : 깃허브 사이트 우측 상단 '+' 버튼을 눌러 'New Repository'를 클릭
1. 로컬저장소 만들기 : 작업 공간 안에 cmd(로컬저장소) > `git init`
1. 로컬과 원격 연결 : cmd(로컬저장소) > `git remote add origin 원격저장소주소`

### 3.2 변경 사항 올리기

1. cmd(로컬저장소) > `git add .` : Staging Area에 변경사항을 추가
1. cmd(로컬저장소) > `git commit -m "커밋메시지"` : Staging Area에 있는 변경사항을 로컬저장소에 기록
1. cmd(로컬저장소) > `git push origin main` : 원격저장소에 변경사항을 기록

---

</details>

<details>
<summary><h1>4주차 - 깃허브에서 변경사항 받아오기</h1></summary>

1. 만약 원격 저장소에서 변경이 생긴다면
2. 

</details>