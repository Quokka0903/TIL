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
<summary>(220720)  7th Day - online </summary>
<div markdown="1">

[Python Tutor code visualizer: Visualize code in Python, JavaScript, C, C++, and Java](https://pythontutor.com/visualize.html#mode=edit)

[(Python) 20 - 파이썬의 유용한 내장함수들](https://dogrushdev.tistory.com/134)

### 제어문(Control Statement)

- flowchart로 표현 가능한, 특정 상황에 따른 선택적 코드 실행
1. 조건문
    - if / elif / else 계속 연습하자

1. 반복문
    - for문
        - Dictionary 순회
            - .Keys() / .values() / .items() → 튜플 활용해서 순회 가능
            - ex)
            
            ```python
            for student, grade in grades.items()
            ```
            
        - enumerate 순회
            - 인덱스(순서)와 객체를 쌍으로 담은 열거형 반환
            
            ```python
            members = ['민수', '영희', '철수']
            
            for idx, number in enumerate(members) : 
                print(idx, number)
            
            # enumerate(members, start = n) -> n값부터 idx가 증가
            ```
            
        - List comprehension
            - 표현식과 제어문을 통해 특정값을 가진 리스트 생성
            
            ```python
            # code for 변수 in iterble if 조건식
            
            cubic_list = [number ** 3 for number in range(1, 4)]
            print (cubic_list)
            
            #[1, 8, 27)
            ```
            
        
        - Dictionary Comprehension
            
            ```python
            cubic_dict0 = {}
            for number in range(1, 4) : 
                cubic_dict0[number] = numer ** 3
            print(cubic_dict0)
            
            #{1: 1, 2: 8, 3: 27}
            
            cubic_dict1 = {number : number ** 3 for number in range(1, 4)}
            print (cubic_dict1)
            
            #{1: 1, 2: 8, 3: 27}
            ```
            

### 함수

- return은 한 함수에 두 개 불가. 여러 개를 반환하고 싶으면 리스트나 튜플 등의 컨테이너 활용

```python
def minus_and_product(x, y) :
    return x - y,  x * y

y = minus_and_product(4, 5)
print(y) # (-1, 20)
print(type(y)) # <class 'tuple'
```

- Input
    - Keyword Argument 다음에 Positional Argument 넣을 수 없다
    - Default Argument를 지정해서 정의된 것보다 더 적은 개수의 argument를 입력 가능
    - 정해지지 않은 여러개의 Arguments 처리는 Asterisk 혹은 언패킹 연산자라고 불리는 * 덕분.
    
    ```python
    print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
    ```
    
    - 가변인자 (*args)
        - 여러개의 Positional Argument를 하나의 필수 parameter로 받아서 사용
        - 몇 개를 받을 지 모를 때 사용.
        
        ```python
        def add(*args) : 
            for arg in args :
                print(arg)
        ```
        
    
    - 패킹 / 언패킹
        - 묶는게 패킹 푸는게 언패킹
        
        ```python
        numbers = (1, 2, 3, 4, 5) #패킹
        a, b, c, d, e = numbers #언패킹
        ```
        
        - 패킹 = 여러 개의 데이터를 묶어서 할당
        - 언패킹 = 시퀀스 속 요소를 여러 변수에 나누어 할당
            - 언패킹시 변수 개수와 할당 갯수가 동일해야 함.
            - 변수에 Asterisk를 붙이면 남은 요소를 담을 수 있음
            
            ```python
            numbers = (1, 2, 3, 4, 5)
            a, b, *rest = numbers
            print(a, b, rest) # 1 2 [3, 4, 5]
            
            a, *rest, e = numbers
            print(rest) # [2, 3, 4]
            ```
            
        
        - *는 시퀀스 언패킹 연산자라고 불리며, 말 그대로 시퀀스를 풀어 헤치는 연산자
            - 튜플이나 리스트 언패킹할 때 사용
            - * 활용해서 가변인자 만들 수 있음
            
            ```python
            def func(*args) :
            	print(args)
            	print(type(args))
            ```
            
            ```python
            def sum_all(*numbers):
            	result = 0
            	for number in numbers :
            				result += number
            	return result
            
            print(sum_all(1, 2, 3)) # 6
            print(sum_all(1, 2, 3, 4, 5, 6)) # 21
            ```
            
            ```python
            def print_family_name(father, mother, *pets): # 아빠 엄마는 필수. 반려동물은 추가적인 인자
            	print(f'아버지 : {father}')
            	print(f'어머니 : {mother}')
            	print('반려동물들')
            	for name in pets:
            			print(f'반려동물: {name}')
            
            ```
            
        
        - 가변 키워드 인자 (**kwargs)
            - 몇 개의 키워드 인자를 받을지 모르는 함수 정의에 유용
            - **kwargs는 딕셔너리로 묶여 처리되며, parameter에 **를 붙임
            
            ```python
            def family(**kwargs) : 
            	for key, value in kwargs.items()
            			print(key, ":", value)
            
            family(father='아부지', mother='어무이')
            ```
            
        - *args 는 **kwargs 와 같이 쓸 수 있나? YES!
            
            ```python
            def print_family_name(*parents, *pets): # 아빠 엄마는 필수. 반려동물은 추가적인 인자
            	print(f'아버지 : {parents[0]}')
            	print(f'어머니 : {parents[1]}')
            	print('반려동물들')
            	for title, name in pets.items():
            			print(f'반려동물: {title} = {name}')
            ```
            
    

### Python의 범위 (Scope)

- 함수는 코드 내부에 local scope 생성. / 이외 공간은 global scope
- scope
    - global scope  : 코드 어디에서나 참조 가능한 공간
    - local scope :  함수가 만든 scope. 함수 내부에서만 참조 가능
- variable
    - global variable : global scope에 정의된 변수
    - local variable : local scope에 정의된 변수

### 변수 수명주기(lifecycle)

- built-in scope
    - 파이썬 실행된 이후부터 영원히 유지
- global scope
    - 모듈이 호출된 시점 이후 혹은 인터프리터가 끝날 떄까지 유지
- local scope
    - 함수가 호출될 때 생성되고, 함수가 종료될 때까지 유지
    

### 이름 검색 규칙(Name Resolution)

- 파이썬의 식별자는 namespace에 저장되어 있음.
- a.k.a LEGB Rule
    - Local scope - 지역 범위(현재 작업)
    - Enclosed scope - 지역 범위 한 단계 위
    - Global scope - 최상단 위치
    - Built-in scope - 정의하지 않고 사용할 수 있는 모든 것
- 함수의 범위 주의
    - 기본적으로 함수에서 선언된 변수는 Local scope에 생성
    - 해당 scope에 변수가 없으면 LEGB 룰에 의해 검색.
        - 접근은 되도 수정은 안됨
        - 할당하면 해당 scope에 생성되므로
        - 함수 내에서 필요한 상위 scope는 argument로 넘겨서 활용해야 함
- 상위 scope 변수를 수정하려면 global, nonlocal 키워드를 활용
    - 그러나 코드 복잡해지고 오류발생 가능.
    

### 함수 응용

- map(함수, 순회가능한 데이터구조)
- zip(*iterables) - iterable들을 모아서 튜플형 object반환
- lambda[parameter] : 표현식
    - 리턴 없고 조건문 반복문 불가.
    - 간결한 함수정의 가능. def 없어도 사용가능
- 재귀함수는 stack overflow 조심하고, 1천회 넘기지 않게 조심할것
    - 재귀적 표현이 자연스러운 알고리즘에 사용할 것.
    - 변수 사용을 줄여줄 수 있으나 입력값이 커지면 연산 속도가 오래 걸림!

### 모듈

- 모듈과 패키지
    - module = 합, 평균, 표준편차 등 자주 쓰는 기능들을 하나의 파일로 묶은 것
        - 특정 기능을 하는 코드를 파이썬 파일(.py)단위로 작성
        
        ```python
        import module
        from module import var, function, Class
        from module import * #다 가져오기
        ```
        
    - package = 다양한 파일을 하나의 폴더로 묶은 것
        - 특정 기능과 관련된 여러 모듈의 집합
        - 패키지 안에는 서브패키지 포함
        
        ```python
        from package import module
        from package.module import var, function, Class
        ```
        
    - library = 다양한 패키지를 하나로 묶은 것.
        - 프레임워크와의 차이점? buzzword(논란되는 언어).
        - 교수님피셜 라이브러리는 삽, 프레임워크는 포크레인
    - pip = 관리자
        - PyPI(Python Package Index)에 저장된 외부 모듈 및 패키지 가져오는 시스템
        
        ```bash
        $ pip install SomePackage #최신버전
        $ pip install SomePackage==1.0.5 #특정 버전
        $ pip install SomePackage>=1.0.4 #최소 버전
        ```
        
        - 패키지 관리 (기록 파일은 보통 requirements.txt)로 정의
        
        ```bash
        $ pip freeze > requirements.txt # 리스트 박제
        $ pip freeze -r requirements.txt # 박제된 리스트 설치
        ```
        
    - 패키지 활용 공간은 가상환경
    

### 사용자 모듈과 패키지

- 패키지 만들기
    - 모든 폴더에는 **init**.py를 만들어 패키지로 인식
        - python 3.3 이후부터는 없어도 되지만 만드는 것 추천.
    

### 가상 환경

- 외부 패키지와 모듈을 사용하는 경우 모두 pip를 통해 설치해야 함.
- 복수의 프로젝트를 할 때 버전이 다를 수 있고, 따라서 가상환경에 독립적으로 패키지 관리해야함
- Python 3.5부터 생김
    - 특정 디렉토리에 가상 환경을 만들고, 고유한 파이썬 패키지 집합 가질 수 있음.
        - 특정 폴더에 환겨잉 있고
        - 실행 환경에서 가상환경을 활성화 시킴
        - 그에 따라서 폴더 관리
        
        ```bash
        $ python -m venv venv00 # venv00이라는 가상환경 생성
        
        $ pip list # 컴퓨터에 설치된 리스트
        
        $ sourse venv/Scripts/activate #나만의 작고 귀여운 가상환경 시작
        
        $ pip list # 이후에는 이 가상환경에 설치된 리스트
        ```

</div>
</details>


<details>
<summary>(220721)  8th Day - offline </summary>
<div markdown="1">


## **메모리 구조**

- 프로그램이 실행되기 위해서는 먼저 프로그램이 메모리에 로드(load)되어야 합니다.
- 또한, 프로그램에서 사용되는 변수들을 저장할 메모리도 필요합니다.
- 따라서 컴퓨터의 운영체제는 프로그램의 실행을 위해 다양한 메모리 공간을 제공하고 있습니다.
- 프로그램이 운영체제로부터 할당받는 대표적인 메모리 공간은 4가지 있습니다.
    - 코드(code) 영역
    - 데이터(data) 영역
    - 스택(stack) 영역
    - 힙(heap) 영역

![http://tcpschool.com/lectures/img_c_memory_structure.png](http://tcpschool.com/lectures/img_c_memory_structure.png)

### 1. **코드(code) 영역**

메모리의 코드(code) 영역은 실행할 프로그램의 코드가 저장되는 영역으로

텍스트(code) 영역이라고도 부릅니다.

CPU는 코드 영역에 저장된 명령어를 하나씩 가져가서 처리하게 됩니다.

### 2. **데이터(data) 영역**

메모리의 데이터(data) 영역은 프로그램의 전역 변수와 정적(static) 변수가 저장되는 영역입니다.

데이터 영역은 프로그램의 시작과 함께 할당되며, 프로그램이 종료되면 소멸합니다.

### 3. **스택(stack) 영역**

메모리의 스택(stack) 영역은 함수의 호출과 관계되는 지역 변수와 매개변수가 저장되는 영역입니다.

스택 영역은 함수의 호출과 함께 할당되며, 함수의 호출이 완료되면 소멸합니다.

이렇게 스택 영역에 저장되는 함수의 호출 정보를 스택 프레임(stack frame)이라고 합니다.

스택 영역은 푸시(push) 동작으로 데이터를 저장하고, 팝(pop) 동작으로 데이터를 인출합니다.

이러한 스택은 후입선출(LIFO, Last-In First-Out) 방식에 따라 동작하므로,

가장 늦게 저장된 데이터가 가장 먼저 인출됩니다.

스택 영역은 메모리의 높은 주소에서 낮은 주소의 방향으로 할당됩니다.

### 4. **힙(heap) 영역**

메모리의 힙(heap) 영역은 사용자가 직접 관리할 수 있는 ‘그리고 해야만 하는’ 메모리 영역입니다.

힙 영역은 사용자에 의해 메모리 공간이 동적으로 할당되고 해제됩니다.

힙 영역은 메모리의 낮은 주소에서 높은 주소의 방향으로 할당됩니다.

## **스택과 힙의 장단점**

### **스택**

매우 빠른 액세스

변수를 명시 적으로 할당 해제 할 필요가 없습니다.

공간은 CPU에 의해 효율적으로 관리되고 메모리는 단편화되지 않습니다.

지역 변수 만

스택 크기 제한 (OS에 따라 다름)

변수의 크기를 조정할 수 없습니다.

### **힙**

변수는 전역 적으로 액세스 할 수 있습니다.

메모리 크기 제한 없음

(상대적으로) 느린 액세스

효율적인 공간 사용을 보장하지 못하면 메모리 블록이 할당 된 후 시간이 지남에 따라 메모리가 조각화되어 해제 될 수 있습니다.

메모리를 관리해야합니다 (변수를 할당하고 해제하는 책임이 있습니다)

변수는 C언어 realloc() or 자바 new

## 체크할 것

### 딕셔너리

1. 딕셔너리 매소드 확인.
2. key - value
3.  순회도는 방법!

### 반복문

1. 순회 방법

### Data 추출

1. 인덱스 접근 방법
2. if문으로 수정하는 방법


</div>
</details>




<details>
<summary>(220722)  9th Day - offline </summary>
<div markdown="1">

- 프로젝트 제출기한은 20시.

### 01_PJT

- 목표
    - 파일 입출력 이해
    - 데이터 구조 분석과 이해
    - Json 형태로 구성
    
- 요구 사항
    - example 참고할 것
    - 데이터를 직접 추출하고 구성하는 과정
    - 필수와 선택 과제로 나뉨.
    - 제출은 gitlab

### 유의사항

```python
dict[’key’] 보다는 dict.get(’key’) 쓰기. 에러 때문에!
print(f’texttext{var1}text{var2} 쓰기.
```

[https://velog.io/@aonee/Python-%EC%A0%95%EB%A0%AC-sort-sorted-reverse](https://velog.io/@aonee/Python-%EC%A0%95%EB%A0%AC-sort-sorted-reverse)

</div>
</details>


<details>
<summary>(220723)  10th Day - weekend </summary>
<div markdown="1">

### import math

[[Python] 반올림, 올림, 내림](https://velog.io/@insutance/Python-%EB%B0%98%EC%98%AC%EB%A6%BC-%EC%98%AC%EB%A6%BC-%EB%82%B4%EB%A6%BC)

### divmod(var1, var2)

 → var1을 var2로 나눈 몫과 나머지를 튜플 객체로 반환

### pow(var1, var2)

 → var1을 var2 제곱하여 반환

### all()

→ 반복 가능한 자료형을 전달해 모두 True이면 True, 하나라도 False면 False

### any()

→ 반복 가능한 자료형을 전달해 모두 False이면 False, 하나라도 True면 True

### enumertae()

→ 시퀀스형을 입력받아 인덱스를 포함하는 튜플 객체를 항목으로 구성하는 enumerate 객체를 반환


</div>
</details>


<details>
<summary>(220724)  11th Day - weekend </summary>
<div markdown="1">

### print()
- print() 함수는 sep 파라미터로 구분자를 넣어줄 수도 있음.
	```
	print('A1', 'B2', sep=',') # A1,B2
	```
- f-string은 파이썬 3.6+에서만 지원한다.

	
### pass	
- Null Operation. 아무것도 하지 않는 기능이다. 목업부터 만들 때 오류를 막기 위해 사용.


- 리스트 컴프리헨션은 표현식이 2개가 넘어가면 가독성이 떨어진다.
	
	```
	import this #Zen of Python
	```

### 빅오
- 입력값이 커질 때 알고리즘의 실행 시간(시간 복잡도)와 함께 공간 요구사항(공간 복잡도)이 어떻게 증가하는지를 분류하는데 사용
- "빅오 표기법은 주어진 경우의 수행시간의 상한을 나타낸다"
- 빅오 표기법 종류
	- O(n)상수 시간을 갖는 알고리즘은 최고의 알고리즘이다!
	- O(log n) 큰 입력값에도 영향을 크게 받지 않는 편
	- O(n) 입력값만큼 실행 시간에 영향을 받음. -> 선형 시간 알고리즘이라고도 함. 모든 입력값을 적어도 한 번 이상 봐야 하는 수준.
	- O(n log n) 병합 정렬을 비롯한 효율 좋은 정렬 알고리즘.
	- O(n**2) 버블 정렬 같은 비효율적 정렬 알고리즘
	- O(2**n) 피보나치 수를 재귀로 계산하는 알고리즘 등.
	- O(n!) 가장 느린 알고리즘.
</div>
</details>


<details>
<summary>(220725)  12th Day - online </summary>
<div markdown="1">


</div>
</details>
