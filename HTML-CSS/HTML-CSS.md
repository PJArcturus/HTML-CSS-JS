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
#### Video(영상)


## HTML Structure

### Semantic

### Layout


# CSS
