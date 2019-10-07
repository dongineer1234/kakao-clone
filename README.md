####################################################################################################

#2-2. What is HTML

# HTML(hyper-Text-Markup-Language)
: 브라우저에게 각 요소가 무엇인지 설명
그저 많은 Tag로 이루어진 Text Document일 뿐임

# HTML, CSS
: 프로그래밍 언어가 아님

####################################################################################################

#2-3. Anatomy of a HTML tag

# index.html
: Web Server들은 index file을 제일 먼저 찾도록 설계돼 있음

# <a href="http://www.naver.com" target="blank">naver</a>
: Target을 Blank로 주면 새로운 창으로 이동함

####################################################################################################

#2-4. Our first HTML document

# <!DOCTYPE html>
: Self-Contained Tag, 혼자 열고 닫는 태그
그 자체로 정보를 제공함 Google Chrome으로 하여금 이 문서가 HTML Document임을 알려줌

# <html>
: 이 태그 사이에 있는 그 무슨 내용이든 다 몽땅 HTML Document

# Head, Body
: Document의 2가지 부분
항상 Tag는 열었으면 닫아야함

# <head>
: 브라우저에게 웹사이트에 관한 필요한 정보를 제공할 뿐
유저에게 보이지 않음

# <Body>
: 사람들이 읽는 Contents

# <title>
: head Tag에서 쓰일 수 있고 Web의 Title을 생성 

# <h1>
: body Tag에서 쓰일 수 있고 큰 제목을 쓰고 싶을 때
이 태그는 1(가장큼)부터 6(가장작음)까지 크기 순서대로 있음

####################################################################################################

#2-5. Adding meta information to our document

# meta
: Head Tag에서 쓰일 수 있는 브라우저를 위한 정보
유저를 위한 정보는 아님

# <meta charset="utf-8">
: meta의 기능(charset)
Character Encoding이라는 뜻
UTF-8 방식의 encoding으로 해당 문서를 작성할 것이라는 뜻

# <meta name="author" content="Dongenius">
: meta의 기능(author)
    
# <meta name="description" content="Welcome to my Kakao Clone">
: meta의 기능(description)

####################################################################################################

#2-6. Semantic vs Non Semantic Tags

# Semantic Tag
: 뜻, 의미가 있는 Tag
h1

# Non-Semantic Tag
: 아무 의미가 없는 Tag
div, span

# Semantic Tag vs Non-Semantic Tag
: div vs article
div는 그 안에 있는게 링크, 이미지, 리스트인지 알 수 없음 의미가 없음 반면 article의 경우 article이라는 걸 알 수 있음

# div
: 컨테이너, 박스와 같은 Tag
안에 내용물을 넣는 것

# span
: Text를 위한 컨테이너

####################################################################################################

#2-7. Giving our tags a name (ID's and Classes)

# div
: 컨테이너, 박스와 같은 Tag
안에 내용물을 넣는 것

# ID, Class
: Tag에 이름을 지정해주는 2가지 방법
우리는 주로 Class를 사용하게 될 것
그 이유는 WebSite상에서 아예 고유한 element는 많이 없기 때문

# ID
: element마다 ID는 한개만 갖을 수 있음
고유하기 때문 Header나 Navigation에 사용

# Class
: ID와 다르게 반복 될 수 있음

####################################################################################################

#2-8. Recap

# 정리
: 
- Header 보이지 않는 부분

- Body 보이는 부분

- meta Tag는 브라우저에 전달하는 추가정보 당연히 Header에 속하게 됨 

- div는 그 안에 있는게 링크, 이미지, 리스트인지 알 수 없음 의미가 없음 반면 article의 경우 article이라는 걸 알 수 있음 

- ID는 여권번호(고유), Class는 콜롬비아 국적(수천만명이 갖고 있음)

####################################################################################################

#3-1. Introduction

# CSS(Cascading Style Sheet)
: 각 요소의 색상, 크기. 배경은 어떠한지 등등을 설명

# Box Model
: 우리의 element를 위치

####################################################################################################

#3-2. CSS Syntax

# CSS의 2가지 Part
: Selector Part, Property Part

# Property Part
: 무조건 소문자, 공백 허용안됨, value, 마지막 세미콜론
property-name: value;

# Selector Part
: property를 내 html의 element에 link하고 싶을 때
h1 괄호가 Selector Part
h1 {
    property-name: value;
}

h1자리에 ID, Class도 쓸 수 있는데 ID인 경우 #을 붙임
#name {
    property-name: value;
}

Class인 경우 .을 붙임
.name {
    property-name: value;
}

####################################################################################################

#3-3. Mixing CSS with HTML

# CSS와 HTML을 Link하는 방법
: 첫번째 방법은 Inline, HTML File 안에 style Tag
두번째 방법은 External, 따로 밖에 File을 생성 
external이 훨씬 좋음

# Inline방식이 구린 이유
: 다른 HTML의 같은 element에 똑같이 적용할 수 없음
직접 HTML마다 따로 따로 만들어 줘야함

# HTML 양식 자동완성
: HTML:5

# External방식
: styles.css File 생성 후
HTML 파일 Head Part에 <link href="styles.css" rel="stylesheet">

####################################################################################################

#3-4. Box Model

# Element
: Box

# Box의 4개 요소
: 컨텐츠(contents), 박스의 보더(border/경계), 패딩(padding), 마진(margin), 박스의 보더에서 바깥쪽으로 있는 간격

# 박스의 경계에서 안쪽이 Padding, 바깥쪽이 Margin

# Padding
: 경계에서 안쪽으로 있는 간격 
padding: 상 우 하 좌; (시계방향)

# Margin
: 경계에서 바깥쪽으로 있는 간격
Margin: 상 우 하 좌; (시계방향)

# border
: border: 폭, 스타일, 색상;

####################################################################################################

#3-5. Inline vs Block vs Inline Block

# Block
: element가 크기와 상관없이 그 옆에 다른 element가 위치하는 것을 허용하지 않는 것 display의 default value

# display: inline-block;
: 각 박스들이 서로서로 옆에 있음

# display: inline
: 모든 property 설정 value를 지움
Inline으로 설정하면 이건 Block이 아님
Text처럼 적용 됨 Inline이라 함은 Text
Text는 높이도 폭도 없음 컨텐츠의 길이만 존재할 뿐
그래서 높이와 폭을 지정해주면 Syntax Error가 발생

####################################################################################################

#3-6. Position property

# position: static;
: default value이며 
element를 거기 놓으면 거기 있을 것임

# position: fixed;
: element를 위치시키면 
오버랩해서 고정되어 그대로 붙어있음
그렇기 때문에 스크롤해도 볼 수 있음
고정 시킨 채로 상하좌우 간격을 줄 수 있음

# position: absolute;
: fixed와 마찬가지로 어디에든 붙일 수 있지만
스크롤하면 보이지 않음
position absolute가 설정되면 HTML상에서 해당 element와 관계가 있는 (relative-부모박스) element를 살펴보고 이에 상응해서 position이 결정 근데 부모 박스와의 상응관계가 없는 경우 우리가 설정한 값대로 움직임 예에서 처럼
position relative를 주어 부모-자식의 관계를 만들어주면
부모 박스의 포지션에 상대적으로 자식 박스도 움직임
부모박스가 없으면 body에 상응해서 움직임

absolute position을 부모 element에 상대적으로 사용하려면
부모 element에게 relative position을 먼저 설정해야 됨

####################################################################################################

#3-7. Fluid layouts with Flexbox

# Flex
: 부모에 display: flex;를 주면
그 안에 종속된 칠드런 박스들을 움직일 수 있음
그래서 각각 박스에게 일일히 명령할 필요가 없음

# justify-content
: 수평으로 적용

# align-item
: 수직으로 적용

# flex-direction
: default value는 row이고,
flex-direction이 row가 되면 justify-content가 수평
align-item은 수직

flex-direction이 column이 되면 justify-content가 수직
align-item은 수평 

# flex-wrap: wrap;
: flex-wrap은 default value는 no wrap

####################################################################################################

#3-8. CSS Selectors and Pseudo Selectors

# 가상 셀렉터(Pseudo Selector)
: 태그 이름이나, class, id를 쓰지 않고 선택하는 방법
셀렉터인데 element가 아닌 것
input[type="submit"] {background-color: red;}
...
<input type="submit">

# .box:first-child {background-color: pink;}
: box class의 첫번째 자식

# .box:last-child {background-color: pink;}
: box class의 마지막 자식

# .box:nth-child(n) {background-color: pink;}
: box class의 n번째 자식

# .box:nth-child(2n) {background-color: pink;}
: box class의 2n번째 자식들(수식으로 선택가능)

# input > box
: direct child 직계라는 의미

####################################################################################################

#3-9. Element States with CSS

# .box:hover {background-color: pink;}
: box class에 hover action을 적용 
hover action시 background가 pink

# .box:active {background-color: green;}
: box class에 active action을 적용 
click action을 유지하고 있을 때 background가 green

# 요소검사 창
: 어떤 action을 적용할 수 있는지 알 수 있음

####################################################################################################

#3-10. Recap

# 정리
: 
- css-syntax, css-html 연결

- 박스모델(마진, 패딩)

- position(static, fixed, relative, absolute)

- display(block, inline-block, inline)

- flexbox, 가상 셀렉터(type, nth child)

- element states(hover, active, focus, visited)


####################################################################################################

#4-1. Introduction

# transitions
: hover같은 효과, active해지거나, click되는 효과

# animations
: customized된 애니메이션

# transformations
: 크기가 커지거나, 회전하거나, 움직이거나

# media query
: 브라우저 크기를 알아내서 그거에 맞춰서 움직이는 것
웹사이트-모바일 반응형

###################################################################################################

#4-2. Transitions

# transition: background-color 5s ease-in-out;
: 천천히 배경색이 다음 action에 맞게 변경됨
transition: all 5s ease-in-out; 적으면 모든 속성이 적용

###################################################################################################

#4-3. Transformations

# transformations
: HTML 문서의 element들을 변경 모습이 변하는 효과

# transform: rotate(20deg);
: 20도 만큼 회전

# transform 속성
: https://developer.mozilla.org/en-US/docs/Web/CSS/transform

###################################################################################################

#4-4. Animations

# keyframes
: none에서 1.5초동안 scaleAndRotateSquare 실행 infinite(계속)
from-to(2part) 대신 0%, 50%, 100%(3part)를 쓸 수 있음
keyframes에 animation을 작성하고 스테이지별로 0%, 50%, 100%을 정함
.box {
      width: 100px;
      height: 100px;
      background: red;
      animation: 1.5s scaleAndRotateSquare infinite ease-in-out
    }

    @keyframes scaleAndRotateSquare {
      from {
        transform: none;
      }

      to {
        transform: rotate(1turn) scale(.5, .5);
      }
    }

###################################################################################################

 #4-5. Media Queries

# mobile 환경일 때
: screen size가 mobile size일 때 배경색이 변경
body {
      background-color: green;
    }

    @media screen and (min-width:320px) and (max-width:640px) {
      body {
        background-color: blue;
      }
    }

###################################################################################################

#4-6. Recap

# 정리
: 
- transition : 하나의 state에서 다른 state로 넘어갈 때 나타나는 효과

- tranformation : element의 모양새를 바꾸는 것 뒤집거나, 비틀거나, 크기를 키우거나

- transition - tranformation mix

- animation - keyframes : from-to(2part), 0% 50% 100%(3part)

- media query : 브라우저 사이즈 조정

###################################################################################################




