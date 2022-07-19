# TIL

## Be전공 Python_6

<details>
<summary>(220714)  1st Day - off</summary>
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
<summary>(220715)  2nd Day - off</summary>
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

### .gitignore 활용

[gitignore.io](https://www.toptal.com/developers/gitignore/)

1. 왜 쓰는가?

```
보안상으로 위험성이 있는 파일프로젝트와 
관계없는 파일용량이 너무 커서 제외해야되는 파일등등
git add 에 포함시키기 싫은 경우가 있다.

물론 이 경우 git rm 를 통해 일부 파일만 제외시키면 되지만, 
모든 커밋에 그런 행동을 하는 것은 번거롭다.

따라서 우리는.gitignore 이라는 디렉토리를 만들어 무시할 파일을 넣어 줄 수 있다.
```

2. ***반드시!!*** Repository 만들자마자 생성해야함.
    1. 한 번 git이 관리하기 시작한 파일은 추가적인 ignore가 안된다.
</div>
</details>


<details>
<summary>(220716)  3rd Day - weekend</summary>
<div markdown="1">


arr = [ ] → arr 배열 선언

len(arr) → arr 배열의 원소 갯수

리스트.remove(a) → 배열에서 a 제거

“이름 : {1}, 나이 {0}세”. format(20, “홍길동) → ‘이름 : 홍길동, 나이 20세’

{숫자 : 문자열 표시 유형}

chr(num) → 아스키코드 num에 해당하는 문자

ord(char) → 문자 char에 해당하는 아스키코드

`for i in range (1, 201, 1) :` → 1 이상 201 미만의 i에 대한 반복문. i는 1씩 증가한다.

```python
dogs = {1: "골든리트리버". 2: "진돗개", 3: "보더콜리"} //사전형 객체

for key in dogs: //사전 객체 dogs를 사용하므로 항목의 키 정보 1, 2, 3이 차례로 대입
	print("{0} : {1}".format(key, dogs[key]))
```

[https://blockdmask.tistory.com/458](https://blockdmask.tistory.com/458) → 문자열

줄바꿈 없이 출력하기

```python
print("AngelPlayer", end='\n') //기본 형식.

for i in range(1, 51) :
    print("{0}".format(i * 2), end=' ')
```

파이썬에서의 삼항 연산자

```python
[true_value] if [condition] else [false_value]
```

	
</div>
</details>


<details>
<summary>(220717)  4th Day - weekend</summary>
<div markdown="1">

### join 사용방법

```python
구분자.join(문자열리스트)

str_list = ["동해물과","백두산이","마르고","닳도록"]
>>> str = " ".join(str_list)
>>> print(str)
# 동해물과 백두산이 마르고 닳도록 출력됨
```

구분자(separator)가 앞에 오고 문자열이 뒤에 오는 구조라서 좀 헷갈릴 수 있다.

### 문자열 나누기- split() 함수

이 함수는 파라미터로 구분자를 주면

해당 구분자를 기준으로 문자열을 잘라 리스트 형식으로 반환합니다.

만약 파라미터에 아무것도 주지 않으면 공백을 기준으로 문자를 나눕니다.

```python
>>> str = "Hi my name is gyu"
>>> splitted_str = str.split()
>>> print(splitted_str)

['Hi', 'my', 'name', 'is', 'gyu']
```

[[파이썬 / Python] map(int, input().split())에 대해](https://ccamppak.tistory.com/38)

### 진수 변환

```python
10진수에서 2진수로 변환함수: bin() # 접두어 0b 붙음
10진수에서 8진수로 변환함수: oct() # 접두어 0o 붙음
10진수에서 16진수로 변환함수: hex() # 접두어 0x 붙음
```

### 문자열 설정

[Python의 문자열에서 부분 문자열 추출](https://www.delftstack.com/ko/howto/python/extract-substring-from-a-string-in-python/)

[파이썬에서 문자열의 부분 문자열을 얻는 방법](https://www.delftstack.com/ko/howto/python/how-to-get-a-substring-of-a-string-in-python/)

### 공백 제거

**3가지 방법**은 아래와 같습니다.

1. **replace() 사용 - 모든 공백 제거**
2. **strip(), lstrip(), rstrip() 사용 - 양쪽, 왼쪽, 오른쪽 공백 제거**
3. **re.sub() 사용 - 정규표현식 사용으로 원하는대로 공백 제거**

### map 함수

```python
list(map(함수, 리스트))# 리스트에서 원소를 하나씩 꺼내 함수를 돌려 다시 리스트로 저장
```

[[python] 파이썬 map 함수 사용법과 예제](https://blockdmask.tistory.com/531)

### 딕셔너리

[Python 딕셔너리](https://zetawiki.com/wiki/Python_%EB%94%95%EC%85%94%EB%84%88%EB%A6%AC)

## **reduce()**

```python
reduce(함수, 시퀀스)
```

#시퀀스(문자열, 리스트, 튜플)의 원소들을 순차적으로 함수에 적용

```python
>>>from functools import reduce   # 파이썬 3에서는 써주셔야 해요  
>>> reduce(lambda x, y: x + y, [0, 1, 2, 3, 4])
10
```

먼저 0과 1을 더하고, 그 결과에 2를 더하고, ….

## **filter()**

```python
filter(함수, 리스트)
```

리스트에 들어있는 원소들을 함수에 적용시켜서 

결과가 참인 값들로 새로운 리스트를 만들어줌. 

```python
>>> list(filter(lambda x: x < 5, range(10)))
[0, 1, 2, 3, 4]
```

### 절대값 함수

```python
abs(x) # x의 절대값
```


</div>
</details>


<details>
<summary>(220718)  5th Day - online </summary>
<div markdown="1">

### 컨테이너

- 여러 개의 데이터를 담을 수 있는 객체.
- 순서가 있는 데이터와 순서가 없는 데이터로 나뉨.
        
    - 리스트 (리스트명 = [요소1, 요소2, … ]
        - 여러 값을 ‘순서가 있는’구조로 저장하고 싶을 때 사용
        - 생성된 이후 변경이 가능
    - 튜플
        - 여러 값을 ‘순서가 있는’구조로 저장하고 싶을 때 사용
        - 생성된 이후 변경이 불가.
        - 단일 항목 튜플은 값 뒤에 쉼표! ex) tuple_a = (1,)
        - 복수 항목 튜플도 넣는 것을 권장
    - 레인지
        - 숫자의 시퀀스를 나타냄
        - 주로 반복문과 사용됨 (for i in range(N))
    - 슬라이싱
        
        [[Tip] Python Array[::] 사용법](https://blog.wonkyunglee.io/3)
        
        - 시퀀스를 특정 단위로 슬라이싱
        - 인덱스와 콜론을 사용하여 특정 부분만 잘라냄
        - 
    - 셋
        - 중복되는 요소 없고 순서 상관 없는 묶음
            - 중복되면 하나만 저장
            - 순서가 없어서 인덱스 접근 불가
    - 딕셔너리
        - 키-값 쌍으로 이루어진 자료형 (3.7이후 orderd)
        - key는 변경 불가능 데이터만 가능.
        - 키의 값(values)는 형태 상관 없음.
        - dict()

### 형변환

- 파이썬에서 데이터 형태는 서로 변환 가능
- 암시적/명시적 변환.

### find 함수

```python
문자열.find(찾을 문자, 시작 index, 끝 index)
```

[[python] 파이썬 find 함수에 대해서](https://blockdmask.tistory.com/569)

[[Python - Tip] 파이썬 출력 메시지 글꼴 설정 - 글자색/배경색/굴게/기울임/밑줄](https://dsegfault.tistory.com/15)

</div>
</details>


<details>
<summary>(220719)  6th Day - offline </summary>
<div markdown="1">

### Dictionary 관련 함수

[[파이썬(Python)] 딕셔너리(Dictionary) 관련 함수 정리! [.keys() / .values() / .items() / .get() / .clear(), in]](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=sw4r&logNo=221504133335)

### append 살펴보기

[파이썬 append( ), extend( ), insert( ) 함수 차이 / 요소추가함수 비교 (Python)](https://ooyoung.tistory.com/117)

### Set 살펴보기

[점프 투 파이썬](https://wikidocs.net/16044)

### replace 함수

```python
변수.replace(변경하고 싶은 문자, 변경할 문자, [변경할 횟수])
```

[파이썬 replace( ) 문자열을 변경하는 함수 (Python)](https://ooyoung.tistory.com/77)

### re.sub

```python
re.sub(패턴, 바꿀 문자열, 문자열, 바꿀 횟수)
```

[[python] re.sub 정규표현식을 통한 문자열 치환 (특수문자 제거)](https://clolee.tistory.com/17)

### Try (예외처리)

[[Python] 예외처리 (try, except, finally, else)](https://yganalyst.github.io/pythonic/memo_16_except/)

</div>
</details>

<details>
<summary>(220719)  7th Day - online </summary>
<div markdown="1">


</div>
</details>
