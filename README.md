
# **오픈소스SW개발론**

## Introduction
오픈소스SW개발론 강의 내용

-------------
### Week1-1 강의 개요 (강의계획서)
* 깃 실습을 위한 **노트북** 필수!!
* 플립러닝
* 퀴즈로 출석체크
* _Haskell_ 다룰 예정

-------------
### Week1-2 오픈소스소프트웨어 개요
* GitHub이 매년 발표하는 전 세계 오픈소스 개발 동향 보고서
  * [OCTOVERSE](https://octoverse.github.com/)(클릭 시 이동)
* github
  * src : Git 구조·버전 관리·코드 협업
  * community : Issue·PR·커뮤니티 가이드라인
  * license : 오픈소스 라이선스 종류와 의미
* OSS : 소프트웨어 저작권 소유자가 모든 사람에게 소스코드를 게시, 사용, 복사, 수정 및 배포할 권리를 부여한 소프트웨어
  * Free Software
    * ‘공짜’(free of charge)가 아니라 **이용자의 자유**를 의미함.
    * 사용자가 프로그램을 **자유롭게 실행, 수정, 복제, 배포**할 수 있어야 함.
  * Open Source Software
    * **소스 코드 접근성과 협업 개발**을 중점으로 함.
    * 누구나 소스 코드를 열람·수정·배포할 수 있지만, ‘자유’보다는 **개발 품질과 효율성**에 초점을 둠.
* OSS License : 오픈소스 소프트웨어의 사용, 복제, 수정, 배포 권한의 범위를 지정
* 오픈소스 라이선스 종류
  * **GPL (GNU General Public License)**
    * 가장 대표적인 강한 카피레프트 라이선스.
    * 소스 코드 공개 의무가 있으며, 수정·배포 시에도 동일한 라이선스(GPL)로 공개해야 함.
    * 상업적 이용은 가능하지만, 배포 시 소스 공개 필수.

  * **LGPL (Lesser General Public License)**
    * GPL의 완화된 버전.
    * 라이브러리 형태로 사용 시, 해당 라이브러리를 링크하는 프로그램은 오픈소스일 필요 없음.
    * 단, LGPL 코드 자체를 수정하면 수정된 부분은 공개해야 함.

  * **MIT License**
    * 매우 자유로운 허용적(permissive) 라이선스.
    * 상업적 이용, 수정, 재배포 모두 자유로움.
    * 단, 원 저작권자 표시와 라이선스 사본 포함 필수.

  * **BSD License**
    * MIT와 유사한 자유로운 허용적 라이선스.
    * 배포 시 저작권 표시와 면책 조항만 유지하면 됨.
    * 변형 버전도 자유롭게 상용 제품에 포함 가능.

  * **Apache License 2.0**
    * 특허(특허권) 관련 조항이 포함된 허용적 라이선스.
    * 기업에서 선호함.
    * 수정·배포 시 변경 내용 명시 필요, 저작권 및 NOTICE 파일 유지.

  * **MPL (Mozilla Public License)**
    * 파일 단위의 카피레프트 라이선스.
    * 수정된 파일만 공개하면 되고, 프로젝트 전체 공개 의무는 없음.
    * 오픈소스와 상용 코드 혼합이 비교적 쉬움.


-------------
### Week2-1 버전 관리 개요
### Week2-1 버전 관리 개요

* **VCS (Version Control System) 소프트웨어**  
  * **CVS (Concurrent Versions System)**: 초기 버전 관리 시스템으로, 텍스트 파일 중심의 소스 코드 관리.  
  * **SVN (Subversion)**: CVS의 단점을 개선한 중앙집중형 버전 관리 시스템. 디렉토리 구조, 브랜치 관리 개선.  
  * **Mercurial**: 분산형 버전 관리 시스템(DVCS). Git과 유사하지만 사용법이 단순하고 직관적.  
  * **Darcs**: 패치 기반 분산형 버전 관리 시스템. 변경 사항 중심 관리.  
  * **Git**: 가장 널리 사용되는 분산형 버전 관리 시스템. 빠른 속도와 강력한 브랜치 기능 제공.  

* **Distributed Version Control System (DVCS)**  
  * **Workspace (작업 영역)**: 개발자가 실제로 파일을 수정하는 영역.  
  * **Index (스테이징 영역)**: 커밋할 파일을 임시로 저장하는 영역. Git에서는 `git add`로 파일을 Index에 올림.  
  * **Local Repository (로컬 저장소)**: 개발자의 로컬 PC에 존재하는 Git 저장소. 커밋과 히스토리 관리 가능.  
  * **Remote Repository (원격 저장소)**: 협업을 위해 중앙 서버나 클라우드에 존재하는 저장소. Push/Pull로 동기화.


-------------
### Week2-2 Git
* Git == History _관리하는_ **도구**
* Git 필수 명령어
  * add : 커밋할 목록에 추가
  * commit : 커밋 (히스토리의 한 단위) 만들기
  * push : 현재까지 역사 (commits) Github에 밀어넣기
* **Git 상태 확인 명령어**  
  * **git show**: 최근 커밋의 상세 정보(변경된 내용, 커밋 메시지 등) 확인.  
  * **git log**: 커밋 히스토리를 시간 순서대로 확인.  
  * **git shortlog**: 커밋 히스토리를 작성자별 요약 형태로 확인.  
  * **git diff**: 수정되었지만 커밋되지 않은 변경 사항 확인.  
  * **git status**: 현재 작업 디렉토리와 스테이징 영역 상태 확인.


![Image](https://cheris8.github.io/assets/images/ETC/GIT/git_structure.png)

-------------
### Week2-3 Github, fork, pull request
* fork 하기
  1. **GitHub 접속**  
    - 브라우저에서 GitHub에 접속 후 로그인합니다.

  2. **Fork 하고 싶은 Repository 이동**  

  3. **Fork 버튼 클릭**  
    - 우측 상단에 있는 **Fork** 버튼을 클릭합니다.

  4. **Fork 위치 선택**  
    - 개인 계정 또는 소속 조직 계정을 선택하여 Fork를 생성합니다.

  5. **Fork 완료 확인**  
    - 선택한 계정에 동일한 Repository가 복사되어 생성됩니다.

  6. **Fork한 Repository Clone (선택 사항)**  
    ```bash
    git clone <Fork된 Repository URL>
    cd <Repository 이름>

* pull-request 하기
  1. 나의 프로필에서 fork해서 만들어진 프로젝트 페이지로 이동 -> Push했던 브랜치를 확인하기 위해서 Branch 탭 클릭 Pull-request하려는 브랜치에서 New pull-request 버튼을 클릭
  2. github 들어가서 fork한 저장소에서 pull-request 버튼 누르기

[My Github Blog](https://github.com/spring-is-me)

-------------------
### Week2-4 Git: Advanced topics

* **브랜치 관리(Branching)**
  - 새로운 기능 개발, 버그 수정용 브랜치 생성 및 관리
  - `git branch`, `git checkout`, `git switch`, `git merge`, `git rebase` 사용법
  - 브랜치 전략: Git Flow, GitHub Flow 등

* **Rebasing과 병합(Merge vs Rebase)**
  - `git rebase`: 커밋 히스토리 정리
  - `git merge`: 브랜치 통합
  - 충돌(Conflict) 해결 방법

-------------
### Week3     Markdown
> 경량화 마크업 언어로, 일반 텍스트 편집기를 사용해 서식 있는 문서를 작성할 수 있음  
* John Gruber와 Aaron Swartz (2004) 개발  
* GitHub README 파일 등에서 널리 사용됨  
* 일반 텍스트를 구조적으로 올바른 HTML로 변환 가능  
* **제목, 목록, 링크, 이미지, 코드 블록, 표, 인용문** 등 지원  
* 간단한 문법으로 원문 그대로 읽어도 이해 가능  
* GitHub, GitLab, Bitbucket, Jekyll 블로그 등 다양한 플랫폼에서 호환  

