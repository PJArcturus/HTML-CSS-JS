# HTML
- Contents
    - Text
    - Media
        - Image, Video, Audio

- Structure
    - Semantic: 의미있는 구조
    - Layout

## HTML Basic
- HTML: Hyper Text Markup Language
    - Hyper Text: 하이퍼링크로 연결된 문서 --> 웹페이지 (콘텐츠, 구조)
    - Markup: 표시
    - Language: 언어

- HTML 문법
    - 명칭: Tag, Element
    - 구성: 시작 Tag ~ 종료 Tag
    - 종료 Tag가 없는 Tag: 빈 Tag(Empty Element)
```
e.g.
<tag> contents </tag> : Element 라고 부른다.

<tag ...>: Empty Element
```

- HTML 속성(Attributes)
    - HTML Element를 표시할 때 필요한 추가 정보 입력
    - name="value"
```
<a href="https://www.naver.com/">네이버</a>

<img scr="photo.png">
```

## HTML Basic Structure
```
<!DOCTYPE html>
<html>
    <head>
        <title></title>
    </head>
    <body></body>
</html>
```

### DOCTYPE
- HTML 문서타입
    - HTML 버전
    - HTML5 표준

### Head - 웹사이트 기본정보
- meta: 웹사이트 관련 정보(검색엔진)
- title: 웹사이트 제목

### Body - 웹사이트 콘텐츠
- 웹사이트에 contents, structure etc. 표시하는 모든 Tag

## HTML Contents

### Text

#### Heading(제목)
- h(Heading): 제목 태그
- 1 ~ 6 단계로 표시됨

#### Paragraph(단락)
- p(Paragraphs): 단락 태그
- 강제 줄 바꿈, 강제 공백은 인식이 되지 않고 공벡 한 칸으로만 인식
    - Line break(강제 줄 바꿈): br 태그
    - Space(강제 공백): &nbsp;(강제 공백 엔터티(Entity))

- hr(Horizontal rule): 수평선 긋기
    -단락을 선의 형태로 구분

#### List(목록)
- ul(Unordered List): 순서없는 목록
- ol(Ordered List): 순서있는 목록
- li(List Item): 목록 항목

★★ Nested HTML Lists 가장 중요한 목록 중 하나 ★★
- 포함관계(Nested Structure)
    - 태그안에 다른 태그들이 포함되는 것
    - 포함하는 요소
        - 조상 요소(Ancestors Element)
        - 부모 요소(Parents Element)
    - 포함되는 요소
        - 자식 요소(Children Element)
        - 자손 요소(Descendant Element)
    - 옆에 나란히 있는 요소
        - 형제 요소(Sibling Element)
```
1)<html>
2)      <body>
3)          <h1>Contents Title</h1>
4)          <p>
5)              단락내용<br>
            </p>
        </body>
</html>
```
(1) 조상 요소 | 기준 요소 | 조상 요소
(2) 조상 요소 | 자식 요소 | 부모 요소
(3)         | 자손 요소 | 형제 요소
(4) 부모 요소 | 자손 요소 | 기준 요소
(5) 기준 요소 | 자손 요소 | 자식 요소

- Description List(설명 목록)
    - dl(Description List) 
    - dt(Description Title): 항목
    - dd(Description Data): 항목에 대한 설명

#### Table(표)
- table
- thead(Table Head): 표 상단 - 제목
- tbody(Table Body): 콘텐츠, 데이터
- tr(Table row): 행
- th(Table header): 제목
- td(Table data): 열


#### Hyper Link(하이퍼링크)

- a(Anchor):
- 기본 속성: href(Hypertext Reference) - 연결할 위치(페이지)

- 링크 이동 위치
    - 외부링크
    - 내부링크: Bookmark

### Media
#### Image(이미지)

- img(Image)
    - 빈 요소
- 기본 속성
    - src(source): 이미지 파일 이름, 위치
    - alt(alternate text): 대체 텍스트 - 이미지가 화면에 표시되지 않을 때, screen reader와 관련

```
<img src="photo.png" alt="잔나-서포터">
```

#### Video(영상)
- video, source
- 속성
    - video 테그: on/off 형태 attribute
        - controls: 동영상 제어 버튼
        - autoplay: 자동 재생
        - muted: 음소거
        - loop: 반복 재생

    - source 테그
        - src: 파일 이름, 경로
        - type: 미디어 형식

- Youtube 영상
    

## HTML Structure

### Semantic

- header
    - logo, login ...
- nav(Navigation)
    - menu
- section
    - 본문 영역
- article
    - 본문 영역
- aside
    - 본문 영역, 부수적인 콘텐츠
- footer
    - 연락처, 주소, 회사 이름 ...

### Layout

- Block & Inline
    - Block 요소
        - 태그가 브라우저에 표시될 때 각 태그 영역이 새 줄에서 표시
        - 태그 영역이 부모요소에 전체 채워짐
    - Inline 요소
        - 태그가 브라우저에 표시될 때 각 태그 영역이 같은 줄에서 표시
        - 태그 영여이 콘텐츠에 맞춰짐

### container element

- div(Division)
    - block
- span
    - inline

## 경로 지정 방식

- 파일의 위치, 인터넷 주소(URL)
- 상대 경로
    - 리소스 파일을 사용하는 HTML파일 기준
    - html 파일 위치에 따라 주소(URL) 변경
    - root(/) 폴더를 기준으로 주소 적용 => root 상대 경로
```
root(/) - [html1] - home.html
        - [html2] - [about] - about.html
        - [images] - photo.png

1) home.html -> photo.png
-  ../images/photo.png
-  /images/photo.png

2) about.html -> photo.png
- ../../images/photo.png
- /images/photo.png
```

- 절대 경로
    - 이미지를 표시하는 HTML 페이지가 기준이 아니고, 해당 서버가 기준
    - 서버부터 주소(URL)를 사용하기 때문에 변동이 없음.

```
root(/) - [html1] - home.html
        - [html2] - [about] - about.html
        - [images] - photo.png

1) home.html
- www.image.com/images/photo.png

2) about.html -> photo.png

```

## 강조 태그, 기타 태그

- 텍스트 특정 부분 강조
    - strong: 강한 강조
    - em(emphasise): 일반 강조
    - mark: html5 버전, block 강조

- 텍스트를 표현할 때 부족한 태그를 보완하는 태그
    - i(Italic)
    - b(Bold)

# CSS
