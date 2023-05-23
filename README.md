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

# 1주차 - 깃과 깃허브란

### 1.1 [Git과 Github의 차이]

> Git - 컴퓨터 **파일**의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 **분산 버전 관리 시스템**이다. 소프트웨어 개발에서 소스 코드 관리에 주로 사용된다. 

> Github - 깃허브는 깃 저장소 호스팅을 지원하는 **웹 서비스**이다.

### 1.2 [Github를 사용하는 이유]

1. 백업 용이성: GitHub는 클라우드 기반의 원격 저장소로, 로컬 저장소와는 별도로 저장됩니다. 따라서 로컬 저장소와 함께 GitHub에 백업하면, 로컬 저장소가 손상되거나 유실되어도 GitHub에서 소스 코드를 복구할 수 있습니다.
2. 버전 관리: Git은 변경 사항을 버전별로 관리하므로, 이전 버전으로 롤백하거나 이전 버전과 비교해 변경 사항을 확인하는 것이 용이합니다. 이를 통해 소프트웨어 개발 과정에서 발생할 수 있는 문제를 빠르게 파악하고 수정할 수 있습니다.
3. 협업 용이성: Git과 GitHub를 이용하면 여러 개발자가 함께 작업하는 것이 용이해집니다. 각 개발자는 자신의 로컬 저장소에서 작업한 내용을 Push하여 공유하고, 다른 개발자의 변경 사항을 Pull하여 업데이트할 수 있습니다. 이를 통해 여러 개발자들이 함께 프로젝트를 개발할 수 있습니다.
4. 오픈 소스 개발과 공유: GitHub는 오픈 소스 개발을 지원하고, 오픈 소스 프로젝트를 공유하는 플랫폼으로서도 사용됩니다. 개발자는 GitHub에서 자신이 개발한 오픈 소스 프로젝트를 공유하여 다른 개발자들과 협업하고, 개선하는 것이 가능합니다.

---

</details>

# 2주차 - 깃과 깃허브 연동

### 2.1 \[용어]

* 로컬 저장소(local repository) : 깃으로 관리되는 자신의 컴퓨터에 있는 저장소
* 원격 저장소(remote repository) : 깃허브로 관리되는 인터넷 세상에 있는 저장소
* config : 깃의 설정으로 파일 형태로 저장됨. 깃허브 아이디와 비밀번호가 여기에 저장

### 2.2 [깃에 깃허브 계정정보 등록]

로컬 컴퓨터에 설치된 깃의 변경사항을 원격 저장소인 깃허브에 올리기 위해선 먼저 깃에 깃허브 계정정보를 등록해야 합니다. cmd 또는 터미널을 켜서 다음을 입력해주세요.(쌍따옴표도 입력해야함)

1. cmd > `git config --global user.name "이름"` : 깃허브 이름 등록
1. cmd > `git config --global user.email "이메일"` : 깃허브 이메일 등록
1. cmd > `git config --global user.password "비밀번호"` : 비밀번호 등록
1. cmd > `git config --list` : 이름,이메일,비밀번호 잘입력되었는지 확인

---

# 3주차 - 로컬 및 원격저장소에 변경사항 저장

### 3.1 [용어 및 상식]

* commit(커밋) : 버전을 구분하게하는 '변경사항'의 단위
* cmd 및 터미널에서 로컬 저장소(프로젝트 폴더)로 이동 : cmd > `cd 폴더경로`

### 3.2 [원격저장소(Remote Repository) 및 로컬저장소(Local Repository) 만들기]

1. 원격저장소 만들기 : 깃허브 사이트 우측 상단 '+' 버튼을 눌러 'New Repository'를 클릭
1. 로컬저장소 만들기 : 폴더를 만들고 그 안에 cmd(로컬저장소) > `git init`
1. 로컬과 원격 연결 : cmd(로컬저장소) > `git remote add origin 원격저장소주소`

### 3.3 [변경 사항 올리기]

1. cmd(로컬저장소) > `git add .` : 변경사항을 커밋(변경사항)에 추가
1. cmd(로컬저장소) > `git commit -m "커밋메시지"` : 로컬저장소에 커밋(변경사항)을 추가
1. cmd(로컬저장소) > `git push origin main` : 원격저장소에 커밋(변경사항)을 추가

---

# 4주차 - 깃허브에서 변경사항 받아오기