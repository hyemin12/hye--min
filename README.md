## 목차

- [사이트](#사이트)
- [VS CODE & NPM](#vs-code&npm)
- [Git 명령어](#git)
  - [github 연결](#github-연결하기)
  - [github 브런치](#git-branch)
  - [git 프로젝트복제](#git-프로젝트-복제)
- [HTML 특수문자](#html-특수문자)
- [마크다운 문법](#마크다운)
  - [마크다운 제목](#마크다운-제목)
  - [마크다운 강조](#마크다운-문장-및-강조)
  - [마크다운 목록](#마크다운-목록)
  - [마크다운 링크](#마크다운-링크)
  - [마크다운 이미지](#마크다운-이미지)
  - [마크다운 코드블럭](#마크다운-코드)
  - [마크다운 표](#마크다운-표)
  - [마크다운 인용문](#마크다운-인용문)

<br>
<hr>

## <span style="color:green;font-weight:bold">#사이트</span>

- [눈누](https://noonnu.cc/index)
- [color hunt](https://colorhunt.co/)
- [webgradients](https://webgradients.com/)
- [simple icons\_브랜드로고](https://simpleicons.org/?q=boot)
- [url-encoder_svg 변환](https://yoksel.github.io/url-encoder/)
- [material-icons](https://mui.com/material-ui/material-icons/)
- fontawesome 5 cdn :

```html
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.8.2/css/all.min.css"
/>'
```

- []()
- []()
<br>
<hr>
<hr>

## <span style="color:green;font-weight:bold">#Git</span>

### $ git 정보 등록(git git hub 아이디, 이메일과 같게 설정)

```bash
$git config --global user.name 'Your_Name'
$git config --global user.name 'Your_Email'
```

### $ 구성확인 (list)

```bash
$git config --global --list
```

### $ 버전 확인

입력 시 파일이 빨간색/초록색으로 나타남

```bash
$git status
```

### #Github 연결하기

```bash
/ 현재 프로젝트에서 변경사항 추적(버전관리)를 시작 /
$git init

/ Github 연결 /
$git remote add origin + github 주소
```

### $ git commit 하기

```bash
1. 변경내용 추적
$git add .

2. 버전 생성
$git commit -m '프로젝트 생성'

3. 업로드
$git push origin 'branch이름'

Eg.
$ git push origin master
```

### $ 연결내용 확인

```bash
$git log
```

### $ 변경사항을 추적할 특정 파일을 지정

```bash
$git add index.html
```

## #git branch

### $ 현재 branch 목록 확인

```bash
$git branch
```

### $ 새로운 branch 생성

```bash
$git branch "Name"
```

### $ 해당 branch로 이동

```bash
$git checkout "Name"
```

### $ 해당 branch 가져오기/서버에서 vs code로

```bash
$git checkout -t "Name"
```

### $ 해당 branch 삭제

```bash
$git branch -d "Name"
```

### $ 새로운 branch 생성 및 해당 branch로 이동

```bash
$git branch checkout -b "Name"
```

## #git 프로젝트 복제

> VS Code에서 복제하는 방법

```
1. git hub 로그인
2. 레퍼지토리 code에서 주소 복사하기
3. vs code에서 터미널 오픈
4. 현재 경로 확인하기
5. dir 입력 (맥 -ls) : 현재 경로에 있는 폴더 확인
6. cd desk tab키 누르면 cd .＼Desktop＼ 입력
   -> 엔터 하면 경로 변경됨
  //cd .. (밖에 폴더로 이동)
7. git clone 깃 주소
8. dir 입력 시 폴더 생성된 것을 확인할 수 있음
```

> github에서 알집파일로 다운받기

```
1. 레퍼지토리 들어가기
2. code버튼 누르기
3. Download ZIP 눌러서 프로젝트 다운받기
```

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FpENvf%2FbtrMjcU6elS%2FHtS7uolK46lGBrlT0eeb9k%2Fimg.jpg)

<br>
<hr>
<hr>

## <span style="color:green;font-weight:bold">#VS CODE & NPM</span>

### 1.확장자 설치

beautify : 코드 정리 (단축키 : ctrl + shift + L)  
Auto remain Tag : 태그 이름을 한번에 변경  
live server : 브라우저 출력

<br>

### 2.단축키

alt + ↑ or ↓ : 줄 이동  
alt + shift + ↑ or ↓ : 줄 복사  
ctrml + \ : 화면분할  
ctrl + B : 사이드바  
ctrl + K S : 전체저장
shift + tab : 내어쓰기

<br>

### 3. NPM

- [npm 설치] 구글에 npm-windows 검색 -> npm-setup 다운로드
- [npm 버전 확인] npm --version
- [해당 버전 설치] npm --install 12.14.1
- [npm 버전 리스트 확인] npm ls
- [해당 버전 사용] npm use 12.21.0
- [해당 버전 삭제] npm uninstall 12.21.0
- [node.js 버전 확인] node --version
- [npm 명령어 확인] npm --help

<br>
<hr>
<hr>

## <span style="color:green;font-weight:bold">#HTML 특수문자</span>

& 붙여서 사용

<br>

| 표현문자 | 특수문자 |
| :------: | :------: |
|   여백   |   #32;   |
|    &     |   #38;   |
|    ＜    |   #60;   |
|    ＞    |   #62;   |

[HTML 특수문자 리스트 더보기](http://kor.pe.kr/util/4/charmap2.htm)

<br>
<hr>

## <span style="color:green;font-weight:bold">#마크다운</span>

<br>

### #마크다운 제목

```md
# 제목 1 (h1)

## 제목 2 (h2)

### 제목 3 (h3)

#### 제목 4 (h4)

##### 제목 5 (h5)

###### 제목 6 (h6)
```

# 제목 1 (h1)

## 제목 2 (h2)

### 제목 3 (h3)

#### 제목 4 (h4)

##### 제목 5 (h5)

###### 제목 6 (h6)

---

### #마크다운 문장 및 강조

> 띄어쓰기 2번하면 줄바꿈 처리가 됨<br>
> 안되면 br 태그 사용

```md
_이텔릭_
**두껍게**
**_이텔릭 + 두껍게_**
~~취소선~~
<u>밑줄</u>
```

_이텔릭_  
**두껍게**  
**_이텔릭 + 두껍게_**  
~~취소선~~  
<u>밑줄</u>

<hr>

### #마크다운 목록

> 순서가 필요한 목록

```md
1. 순서가 필요한 목록
2. 순서가 필요한 목록
3. 순서가 필요한 목록
   1. 순서가 필요한 목록
   2. 순서가 필요한 목록
4. 순서가 필요한 목록
```

> 순서가 필요하지 않은 목록

```md
- 순서가 필요하지 않은 목록
- 순서가 필요하지 않은 목록
- 순서가 필요하지 않은 목록
  - 순서가 필요한 목록
  - 순서가 필요한 목록
- 순서가 필요하지 않은 목록

- 순서가 필요하지 않은 목록에 사용 가능한 기호
  - 대쉬(hyphen)
  * 별표(asterisks)
  - 더하기(plus sign)
```

---

### #마크다운 링크

```md
[보여지는 내용](이동할 링크)

예)
[GOOGLE](https://google.com)
```

> 내부에서 링크이동<br>
> 띄어쓰기는 - (하이픈으로 구분)

```md
[보여지는 내용](#이동할위치)

[보여지는 내용](#이동할-위치)
```

---

### #마크다운 이미지

```md
![대체 텍스트(alt)를 입력하세요!](이미지 주소)

이미지에 링크걸기
[![대체 텍스트](이미지 주소)](이동할 사이트 주소)
```

---

### #마크다운 코드

> 인라인 코드

```md
`backtick`기호 안에 작성하면됩니다.
```

`backtick`기호 안에 작성하면됩니다.

> 블록 코드

#### - HTML

````md
```html
<h1>html코드</h1>
```
````

```html
<h1>html코드</h1>
```

#### - CSS

````md
```css
* {
  padding: 0;
  margin: 0;
}
```
````

```css
* {
  padding: 0;
  margin: 0;
}
```

#### - Javascript

````md
```javascript
function func() {
  // 코드작성
}
```
````

```javascript
function func() {
  // 코드작성
}
```

---

### #마크다운 표

```md
| 구분 |    내용     |
| :--: | :---------: |
|  --  |  왼쪽 정렬  |
| :--: | 가운데 정렬 |
| --:  | 오른쪽 정렬 |
```

| 구분 |    내용     |
| :--: | :---------: |
|  --  |  왼쪽 정렬  |
| :--: | 가운데 정렬 |
| --:  | 오른쪽 정렬 |

---

### #마크다운 인용문

```md
> 인용문을 작성하세요!
>
> > 중첩됩 인용문
> >
> > > 중중첩된 인용문
```

> 인용문을 작성하세요!
>
> > 중첩됩 인용문
> >
> > > 중중첩된 인용문
