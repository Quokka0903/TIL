# TIL

## Be전공 Python_6

<details>
<summary>1st Day - off</summary>
<div markdown="1">

- 신입개발자의 역량

1. 코테통과 (알고리즘)
2. CS
3. 영어
4. 잔디가 빽빽(꾸준한 학습 증명) → 가장 중요

------

#### Git (분산 버전 관리 프로그램) / Github (Git 기반 저장소 서비스) -  소잘능개의 기본
	- 중앙 집중식 버전 관리(SVN, 서버컴퓨터 한대. 매니지먼트쪽 강점.)의 단점 보완.
	- 레거시 프로젝트(와 그 히스토리)의 안정적인 보관을 위해서는 분산 버전 관리가 유리하다.
	- 법인이 쓰기에는 Github이 더 비싸고, 소스코드가 서버로 들어가기 때문에 보안 이슈가 있음.

- CLI (Command Line Interface) & Markdown
	- GUI - 그래픽으로 상호작용. 쉽지만 성능이 더 소모됨.
	- CLI - 명령어를 통해 상호작용. 서버/개발 시스템이 이러한 조작환경제공.
	- Git Bash
		- Git은 Linux로 되어있기 때문에, 윈도우에서 Linux를 사용하기 위해 Git Bash로 수행.
		- 절대경로: 모든 경로 / 상대경로: 현재디렉토리 기준 상대적 위치

- Markdown → 텍스트기반 가벼운 markup언어
	- 문서 구조화와 내용을 쉽고 빠르게 작성코자. (특히 웹 환경)
	- 선택한 언어의 Highlight Syntax 적용.
	- README.md
		- 파일을 통해서 오픈 소스의 공식 문서 작성. 잔디심을때마다!
			- 프로젝트에 대한 설명
			- 가장 먼저 보는 문서
			- 일반적으로 SW와 함께 배포
			- 형식은 따로 없으나 일반적으로 Markdown 활용
		- 개인 프로젝트의 소개 문서 작성
		- 매일 학습한 내용 정리
		- MarkDown 활용한 블로그 운영

#### Repository
- 특정 디렉토리 버전관리하는 저장소
1) git init 명령어로 로컬 저장소 생성 → 기본 필수요소(초기값)을 세팅해줌.
2) .git 디렉토리에 버전 관리에 필요한 것이 들어있음
3) git config —global → 이메일과 유저네임 설정.
4) README.md
- Working Directory(작업하는 실제 디렉토리 — untracked)
 → <git add 파일명 or git add . (현재디렉토리 전체)> →
- Staging Area(커밋으로 남기고 싶은 파일이 있는 곳 — staged)
 → <git commit -m “메세지”> →
- Repository(커밋이 저장되는곳 — committed) → <git push> →
- vscode에서 Git Graph 설치해볼 것!

#### ??Staging Area는 왜 있지??
- Working Directory 자체의 모습이 아니라 수정사항(변화된 내용)만 반영되기 위해서!
- 상용(퍼블리싱)할 내용들만 골라 commit해야 하니깐~

#### Github Repo Settings에서 default Branch를 master로 바꿔야 하는 이유?
- main으로 바뀐 이유가 있다.
 [깃허브, 개발용어 '마스터'→메인으로 바꾼다](https://zdnet.co.kr/view/?no=20200921101131)
- 그런데 기존 기업들은 모두 master로 쓰기 때문에 main으로 저장하자~

#### 로컬과 깃헙 레포 연결하기
- git remote add origin 링크 → 연결.
	- 링크의 별명을 origin으로 설정하는 것.
- git push -u origin master → 깃푸쉬.
	- origin → 별명
	- master → local branch 이름

#### git clone, git pull
- clone == 해당 url을 다운로드 받는 것.
- pull == remote에서 local로 업데이트 하는 것.
	- vscode에서 수정 옵션 선택 가능

</div>
</details>

<details>
<summary>2st Day - off</summary>
<div markdown="1">

### git collaborator 초대

[https://eunoia3jy.tistory.com/118](https://eunoia3jy.tistory.com/118)

### git branch 활용

[https://git-scm.com/book/ko/v2/Git-브랜치-브랜치란-무엇인가](https://git-scm.com/book/ko/v2/Git-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EB%B8%8C%EB%9E%9C%EC%B9%98%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)

1. 브렌치 생성 후 이동

```bash
git checkout -b (브렌치)

git switch -c (브렌치)
```

[https://git-scm.com/book/ko/v2/Git-브랜치-브랜치와-Merge-의-기초](https://git-scm.com/book/ko/v2/Git-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EB%B8%8C%EB%9E%9C%EC%B9%98%EC%99%80-Merge-%EC%9D%98-%EA%B8%B0%EC%B4%88)

1. 병합 (마스터 브렌치와 입력 브렌치의 병합)

```bash
git merge (브렌치)
```

1. 변화 확인하기

```bash
git log --oneline --graph
```

## 챗봇 프로그래밍

### 4차 산업 혁명과 소프트웨어

- 4차산업 - 소프트웨어 중심의 기술, 산업, 사회 패턴과 절차의 급격한 변화
- 빅데이터, 인공지능, 로봇공학, 사물인터넷, 무인운송, 3D프린터, 나노기술
- 오픈소스 라이브러리를 잘 활용하자! 디자인과 기능을 구상하여 조립하는 것이 중요.
    - 에러를 무서워말자!

### Request module 설치

```bash
pip install request
pip install beautifulsoup4
pip install lxml
```
</div>
</details>
