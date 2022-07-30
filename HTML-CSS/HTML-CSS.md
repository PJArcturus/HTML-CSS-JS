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

- Contents styling
    - text styling
    - media styling

- Layout(structure styling)
    - 가로배치(Flexbox)

## CSS Basic

- CSS: Cascading Style Sheet

```
h1 {color: blue; font-size: 20px;}

h1 {
    color: blue;
    font-size: 20px;
}
```

## Selector(선택자)

- 선택자로 HTML 요소를 선택
- HTML 요소 선택 방법
    - Simple Selector(단순 선택자)
        - tag/element 이름 사용
        - class 이름 사용
        - id 이름 사용

```
<a href="www.google.com" class="google">Google</a>
<a href="www.apple.com" id="apple">Apple</a>

/* a 태그 2개 모두 red 색상 적용 */
a {
    color: red;
}


/* a 태그 각각 다른 색상을 적용 */

요소 앞에 . 을 붙이면 class로 인식
.google {
    color: blue;
}

요소 앞에 # 을 붙이면 id 값으로 인식
#apple {
    color: green;
}
```

### id, class 이름의 특징

- id
    - 같은 HTML 페이지에서 유일(고유) 해야 한다.
        - 프로그래밍 언어의 변수와 연결 가능성이 있기 때문
    - HTML 요소에 여러개의 id 이름 사용 불가

- class
    - 같은 HTML 페이지에서 여러변 사용 가능하다.
    - HTML 요소에 여러개의 class 이름 사용 가능

```
<p class="paragraph">단락1</p>  <o>
<p class="paragraph">단락2</p>  <o>

<p id="contents">단락3</p>  (o)
<p id="contents">단락4</p>  (x)


<p class="gnb-list-item">회사소개</p>
```

### CSS 선택자 우선순위

- Cascading 규칙
    - 동일한 대상에 여러 스타일이 적용될 때 제일 마지막에 적용된 스타일이 반영

- 선택자 우선순위
    - 선택자 종류에 따라 css 적용 우선순위가 다르게 정의
    - cascading 규칙에 따르지 않고 css를 적용할 때 사용
    - inline: 1000점
    - id: 100점
    - class: 10점
    - tag: 1점

### Text Styling

#### Color

```
h1 {
    color: blue;
}
```

#### Text alignment
```
p {
    text-align: center;
}
```

- 정렬 값: left, center, right, justify(양쪽맞춤)
- 단어 중간에 줄바꿈

```
p {
    word-break: break-all;
}
```

#### Text Decoration

```
h1 {
    text=decoration: underline;
}


h1 {
    text=decoration: line-through;
}


h1 {
    text=decoration: overline;
}


h1 {
    text=decoration: none;
}
```

#### Text Spacing

```
p {
    text-indent: 16px;
}


h2 {
    letter-spacing: 5px;
}


p {
    word-spacing: 3px;
}


p {
    white-space: nowrap;
}
```

- line-hight
    - 텍스트 줄을 포함한 줄 높이
    - 값(단위)
        - px
        - 배수: 소수점을 포함한 숫자 가능, 폰트 크기를 기준

★★ 조상요소나 부모요소에 CSS 속성을 적용했을 때, 자식요소에도 적용되는 것을 상송
    - HTML Element 중에 상속되지 않는 테그가 있음
    - CSS 속성중에 상속되지 않는 속성이 있음


#### Font Family

- CSS 파일이 브라우저에서 렌더링되기 때문에 폰트 파일을 클라이언트 PC에서 찾음
    - 다수의 클라이언트 PC에 설치될 만한 폰트를 선택 (Web Safe)
- font-family 속성에 값으로 정해준 폰트 종류를 차례대로 찾음(Fallback)

- 서버에서 폰트롤 사용할 수 있게 하는 기능
    - Web Font 기능

- 구글 Font

- 폰트 종류(저작권)
    - 폰트 파일 포함 여부


#### Font Size

- font-size
- 폰트 크기: px


#### Font Style

- font-style
- 기울임꼴 설정
- italic 값


#### Font weight

- font-weight
- 굵기
- normal / bold
- 단위 없는 100단위 숫자 값 사용

#### Link Style
- a 태그가 4가지 상태를 구분함
- link, visited, hover, active

```
<a href="https://www.naver.com" class="link">Naver</a>

a: link{

}

.link: visited{

}

a: hover{

}

a: active{

}
```

### Media contents styling

- Image, Video
    - 위치 지정
    - Box Model 적용

### Layout styling
- Element 영역
    - Block, Inline Element
- Element 영역 styling
 - Box Model
- Element 배치
 - 배치 지정
    - 인접해있는 박스들의 관계
    - 인접해있는 박스들 사이에 영향
 - 위치 지정
    - 박스의 위치를 단독으로 지정

#### Box Model

- Box Model 구성요소
    -  content(width / height), padding, border, margin

- inline 요소에 box model 적용
    - width / height: 적용 안됨
    - margin: 위아래 적용 안됨, 좌우 적용됨

##### width / height
    - block 요소
        - width는 부모 요소에 채워짐
        - height는 contents 또는 자식 요소에 맞춰짐
    - px
        - 수치 값으로 크기 고정
    - %
        - 부모 요소를 기준으로 일정 비율 크기만큼 지정
        - height는 적용이 되지 않음
    - auto
        - width / height 자동으로 크기 지정
        - width / height의 원래 특성으로 적용

##### padding

- 안쪽 여백

```
padding-top
padding-right
padding-bottom
padding-left
(** 방향 순서: top을 기준으로 시계방향 순서)

padding: 10px 20px 30px 40px; -> 4방향 각각 적용

padding: 10px 20px 30px; -> 2번째 값: 좌우 공통 적용

padding: 10px 20px; -> 1번째 값: 위 아래 공통 적용, 2번째 값: 좌우 공통 적용

padding: 10px; -> 4방향 공통 적용
```

##### margin

- margin 사용 방법은 padding과 동일함

- margin collapse(겹침/상쇄)
    - 위아래에 인접한 박스의 margin이 상쇄되는 현상
    - 두 여백중 큰 쪽 여백만 적용
    - 좌우로 인접한 박스는 양쪽의 margin이 모두 적용되어 합쳐짐

##### border

- 굵기, 모양, 색

```
border: 1px solid red;

border-top: 1px solid red;
border-right
border-bottom
border-left
```

##### background

- 배경색, 배경 이미지 표시
- 배경은 box model 요소 중 content, padding 영역까지 적용

```
background-color: blue;

background-image: url(이미지파일)
background-repeat: no-repeat;
background-position: 10px 20px;
background-attachment: fixed;
```

- background-repeat
    - repeat(default), repeat-x, repeat-y

- background-position
    - px
    - left, center, right
    - top, center, bottom
    - 배경이미지의 위치 지정은 이미지 반복이 안될 때 적용

- background-attachment
    - 배경 이미지 고정
    - fixed

#### display

- 박스의 표시 속성을 변경해서 표시

```
display: inline;  /* block 요소가 inline 요소의 특성으로 화면에 표시 */
display: block;  /* inline 요소가 block 요소의 특성으로 화면에 표시 */
display: inline-block;  /* inline과 block의 특성을 모두 표시: 나란히 표시, 박스모델 */
```

### layout 배치

- float
- flex
- grid

- flexbox