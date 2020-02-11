# HTML

## 텍스트를 덩어리로 묶어주는 태그
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h2>텍스트를 묶어주는 태그</h2> // 제목 표시하기

    <p>여기는 <strong>첫번째</strong> 단락입니다.</p> 
    <p><b>여기는 두번째 <br>  단락입니다.</b></p>
    <pre></pre> 
    <p><i>세번째 단락입니다.</i></p>
    <p><em>네번째 단락</em></p>
    <hr>
    //단락을 표시하는 <p>//
    //줄을 바꿀수 있는 <br>//   
    // 인용문을 넣을때 쓰는 <blockquote></blockquote> //
    // 가로 줄을 만드는 <hr>//
    // 테그에 입력하는 그대로 나오는 <pre></pre>//
  </body>
</html>
```
## 텍스트를 한줄로 표시하는 태그
```html
굵게 표시하는 <strong></strong>,<b></b>
이탤릭체 표시하는 <i>,<em>
인용 내용 표시하기<q cite=""></q>
형광펜 효과 내기 <mark></mark>
줄바꿈 없이 영역 묶기<span></span> 
동아시아 글자 표시하기<ruby></ruby>
```
## 목록을 만드는 태그
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <ul> <!--  순서 없는 목록   -->
      <li>1일차
        <ol type = "a" reversed> <!-- 순서 있는 목록 -->
          <li>해녀박물관</li>
          <li>낚시체험</li>
        </ol>
       </li>
      <li>2일차
        <ol type="a" start="3">
          <li>용눈이오름</li>
          <li>만장굴</li>
          <li>카약체험</li>
        </ol>
      </li>
    </ul>
  </body>
</html>
```
## dl,dt,dd
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h2>웹 과정을 통해 배우는 것</h2>
    <dl>
      <dt>HTML,CSS</dt>
      <dd>HTML:웹문서의 내용을 구성한다.</dd>
      <dd>CSS:웹문서의 스타일을 구성한다.</dd>
      <dt>JavaScript</dt>
      <dd>역동적인 웹을 만들 수 있다.</dd>
      <dd>프로그래밍 언어를 알아야 한다.</dd>
    </dl>
  </body>
</html>
```
## 표를 만드는 태그
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <table border="1">
      <tr>
        <th>1행1열 제목</th>
        <td>1행2열</td>
        <td>1행3열</td>
      </tr>
      <tr>
        <th>2행1열 제목</th>
        <td>2행2열</td>
        <td>2행3열</td>
      </tr>
    </table>

  </body>
</html>

------------------------------------------------------------------

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
    <style media="screen">
      table{border-collapse: collapse;}
    </style>
  </head>
  <body>
    <table border="1">
      <caption>
        <strong>내 소개</strong>
        <p>아래를 봐주세요</p>
      </caption>
      //    <figure>
      //     <figcaption>
      //     <p>caption 대신 figcaption 사용가능</p>
      //     </figcaption>
      <colgroup>
        <col style = "width:100px";>
        <col style = "width:300px";>
        <col style = "width:100px";>
        <col style = "width:300px";>
      </colgroup>
      <tr>
        <th>이름</th>
        <td>남설빈</td>
        <th>연락처</th>
        <td>010-1234-1234</td>
      </tr>
      <tr>
        <th>주소</th>
        <td colspan="3">경기도 수원시 영통구</td>
      </tr>
      <tr>
        <th>자기소개</th>
        <td colspan="3">html을 학습 중인 학생입니다.</td>
      </tr>
    </table>

  </body>
</html>


```
## thead,tbody,tfoot 태그- 표 구조 정의하기
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
    <style media="screen">
      table{border-collapse: collapse;}
      thead{background-color: rgb(132, 235, 118);}
      tfoot{background-color:rgb(132, 235, 118);}
    </style>
  </head>
  <body>
    <table border="1">
      <thead>
        <tr>
          <th>방이름</th>
          <th>대상</th>
          <th>크기</th>
          <th>가격</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>유채방</td>
          <td>여성 도미토리</td>
          <td rowspan="3">4인실</td>
          <td rowspan="4">1인, 20,000원</td>
        </tr>

        <tr>
          <td rowspan="2">동백방</td>
          <td>동성 도미토리</td>
        </tr>

        <tr>
          <td>가족1팀</td>
        </tr>

        <tr>
          <td>천혜향방</td>
          <td>-</td>
          <td>2인실</td>
        </tr>

      </tbody>
      <tfoot>
        <tr>
         <th colspan="4">바깥채 전체를 렌트합니다.</th>
        </tr>
      </tfoot>
    </table>
  </body>
</html>

```  

## 링크 만들기
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
    <style media="screen">
      ul{list-style-type: none;} //동글뱅이 표시 제거
      a{text-decoration: none;} //밑줄 제거
      a:hover{color: blue;} //마으스 커서시 반응
    </style>
  </head>
  <body>
    <ul>
       li*3>a // li 가 3 개 만들어짐
      <li><a href="a-1.html">첫번째 이동</a></li> <!-- a-1로 이동 하게 만듬 -->
      <li><a href="a-2.html">두번째 이동</a></li> <!-- a-2로 이동 하게 만듬 -->
      <li><a href="a-3.html">세번째 이동</a></li> <!-- a-3로 이동 하게 만듬 -->
      <li><a href="https://www.naver.com/" target="_blank">네이버로 이동</a></li> //새창열림
      <li><a href="https://www.daum.net/">다음으로 이동</a></li>
      <li><a href="https://www.nate.com/">네이트로 이동</a></li>
      <a href="https://www.naver.com/"><img src="images/Tulips.jpg" alt="툴립">누르면 네이버로</a>
    </ul>
    <iframe src="" width="" height=""></iframe>
  </body>
</html>

```
## 한문서 안에서 점프 하기
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>앵커 만들기</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <ul id="menu">
      <li><a href="#content1">메뉴1</a></li>
      <li><a href="#content2">메뉴2</a></li>
      <li><a href="#content3">메뉴3</a></li>
    </ul>

    <h2 id="content1">내용1</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. </p>
    <a href="#menu">[메뉴로]</a>


    <h2 id="content2">내용2</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. .</p>
    <p><a href="#menu">[메뉴로]</a></p>

  </body>
</html>

```
## 폼태그 만들기
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
    <style media="screen">
      li{margin-top: 20px;}
    </style>
  </head>
  <body>
    <form method="post">
      <input type="text" title="검색">
      <input type="submit" title="검색">

      <ul style="list-style:none;">
        <li>
          <label for="id">아이디</label>
          <input type="text" id="id">
        </li>
        <li>
          <label for="pw">비밀번호</label>
          <input type="password" id="pw">
        </li>
         <li> <button type="button" name="button">로그인</button> </li>
      </ul>
    </form>
  </body>
</html>
```
## 폼 요소에 라벨 붙이기
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <form>
      <h3>수강 분야(다수 선택 가능)</h3>
      <ul>
        <li><input type="checkbox" value="grm">문법</li>
        <li><input type="checkbox" value="wr">작문</li>
        <li><input type="checkbox" value="rd">독해</li>
      </ul>

      <h3>수강 분야(1과목만 선택 가능)</h3>
      <ul>
        <li><label><input type="radio" name="subject" value="eng">영어회화</label></li>
        <li><label><input type="radio" name="subject" value="ch">중국어 회화</label></li>
        <li><label><input type="radio" name="subject" value="jp">일어회화</label></li>
      </ul>
    </form>

  </body>
</html>
```
## fieldset,legend 태그
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
    <link rel="stylesheet" href="css/design.css">
    <!-- css라는 파일에 design.css 이름으로 파일저장. -->
    // design.css 파일에서 접근
  </head>
  <body>
    <form>
      <fieldset>
        <legend>개인정보</legend>
        <ul>
          <li>
            <label for="name">이름</label>
            <input type="text" id="name">
          </li>
          <li>
            <label for="mail">메일 주소</label>
            <input type="text" id="mail">
          </li>
        </ul>
      </fieldset>
    </form>
  </body>
</html>

design.css에서 사용한 명령어.
li{margin-top: 20px; }
ul{list-style-type: none;}

```

## 주요 intput 태그
```html
hidden
text
tel
password
checkbox
radio
submit
reset
button

hidden ) <intput type="hidden" name="이름" value ="서버로 넘길 값">
password ) <input type="password" [속성 ="속성 값"]  
text ) <input type="text" [속성="속성 값"]
-name : 텍스트 필드를 구별할 수 있는 이름
-size : 텍스트 필드의 최대 길이 지정, 지정길이를 초과시 화면에 표시되지 않음
-value : 텍스트 필드가 화면에 표시될때 필드 부분에 표시될 내용
           이 속성 미 사용시 빈 텍스트 필드 표시됨.
-maxlength  : 텍스트 필드에 입력할 수 있는 최대 문자 개수 지정.  

  <!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <form>
      <fieldset>
        <label>아이디: <input type="text" id="user_id" size="10"></label>
        <label>비밀번호: <input type="password" id="user_pw" size="10"></label>
        <input type="submit"  value="로그인">
      </fieldset>
    </form>
  </body>
</html>

  
```
## 분화된 텍스트 필드
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <ul>
      <li>
        <label for="user-name">이름</label>
        <input type="text" id="user-name">
      </li>
      <li>
        <label for="mail">메일주소</label>
        <input type="email" id="mail">
      </li>
      <li>
        <label for="phone">연락처</label>
        <input type="tel" id="phone">
      </li>
      <li>
        <label for="homep">블로그/홈페이지</label>
        <input type="url" id="homep">
      </li>
    </ul>
  </body>
</html>
```
## number 타입
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <ul>
      <li>
        <label class="reg" for="member">참여인원<small>(최대10명)</small></label>
        <input type="number" id="member" value="1" min="0" max="10" step="1">
      </li>
      <li>
        <label class="reg" for="stuffs">지원물품 <small>(1인당 5)</small></label></li>
        <input type="number" id="stuffs" value="1" min="0" max="50" step="5">
      <li>
        <label class="reg" for="satis">희망단계 <small>(하,중,상)</small></label></li>
        <input type="range" id="satis" value="1" min="1" max="3">
    </ul>
  </body>
</html>
```
## 라디오 버튼과 체크박스 삽입 하기
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <fieldset>
      <legend>신청 과목</legend>
      <p>이 달에 신청할 과목을 선택하세요</p>
      <label><input type="radio" name="subject" value="speaking">회화</label>
      <label><input type="radio" name="subject" value="grammar">문법</label>
      <label><input type="radio" name="subject" value="writing">작문</label>
    </fieldset>

    <fieldset>
      <legend>메일링</legend>
      <p>메일로 받고 싶은 뉴스 주제를 선택해 주세요(복수선택 가능)</p>
      <label><input type="checkbox" name="mailing1" value="news">해외 단신</label>
      <label><input type="checkbox" name="mailing1" value="dialog">5분 회화</label>
      <label><input type="checkbox" name="mailing1" value="pops">모닝팝스</label>
    </fieldset>
  </body>
</html>
```
## 날짜,시간,버튼 삽입 하기
```html
날짜
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <label><input type="date" id="start"></label>
    <label><input type="date" id="end"></label>
  </body>
</html>
------------------------------------
시간
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h3>원하는 대관시간을 선택하세요.(오늘)</h3>
    <label>시작 시간 <input type="time"  value="09:00" id="start"></label>
    <label>종료 시간 <input type="time" value="18:00" id="end"></label>

    <h3>대관시간을 선택하세요(다른날짜)</h3>
    <label>시작 시간 <input type="datetime-local"  value="2020-01-30T09:00" id="start2"></label>
    <label>종료 시간 <input type="datetime-local" value="2020-01-30T18:00" id="end2"></label>
  </body>
</html>
-------------------------------------
SUBMIT
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <form action="index.html" method="post">
      <label>메일 주소<input type="text"></label>
      <input type="submit" value="제출">
      <input type="reset" value="다시입력">
    </form>
  </body>
</html>
-------------------------------------
버튼
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <input type="button" value="새 탭 열기" onclick="window.open()">
  </body>
</html>
```
## 드롭다운 태그 만들기
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <label class="reg" for="class">학과</label>
    <select size="5" id="class" multiple>
      <option value="archi">건축공학과</option>
      <option value="mechanic">기계공학과</option>
      <option value="indust">산업공학과</option>
      <option value="elec">전기전자공학과</option>
      <option value="computer">컴퓨터공학과</option>
      <option value="chemical">화학공학과</option>
    </select>
  </body>
</html>
```
## 태그 - 옵션끼리 묶기
```html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <title></title>
</head>

<body>
  <label class="reg" for="class">학과</label>
  <select id="class">
    <optgroup label="공과대학">
      <option value="archi">건축공학과</option>
      <option value="mechanic">기계공학과</option>
      <option value="indust">산업공학과</option>
      <option value="elec">전기전자공학과</option>
      <option value="computer">컴퓨터공학과</option>
      <option value="chemical">화학공학과</option>
    </optgroup>
    <optgroup label="인문대학">
      <option value="history">사학과</option>
      <option value="lang">어문학부</option>
      <option value="philo">철학</option>
    </optgroup>
  </select>
</body>

</html>

```
## 데이터 목록 만들기
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <input type="text" id="interest" list="choices">
    <datalist id="choices">
      <option value="grammar" label="문법"></option>
      <option value="voca" label="어휘"></option>
      <option value="speaking" label="회화"></option>
      <option value="listening" label="리스닝"></option>
      <option value="news" label="뉴스청취"></option>
    </datalist>
  </body>
</html>
```

## 여러줄을 입력하는 텍스트 영역 만들기
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <textarea name="intro" rows="5" cols="60">
      열심히 사는 사람들의 손을 잡아주는곳
    </textarea>
  </body>
</html>
```
## 결과값 계산하기
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <form oninput="result.value=parseInt(num1.value)+parseInt(num2.value)">
      <input type="number" name="num1" value="0">
      +<input type="number" name="num2" value="0">
      =<output name="result" for="num"></output>
    </form>
  </body>
</html>
```

# CSS
```html
스타일 우선 순위
1.인라인 스타일
2.id 스타일
3.클래스 스타일
4.태그 스타일
*동일 순서적용시 마지막에 적용된 스타일을 따름.

## CSS linear
```html
@charset "EUC-KR";
.grad{
	background: blue;
	background: -webkit-linear-gradient(left top,blue,white);
	background: -moz-linear-gradient(right top,blue,white);
	background: -o-linear-gradient(right top,blue,white);
	background: linear-gradient(to left bottom,#ff0000,#ffffff);
}

div{
	width: 500px;
	height: 300px;
	border-radius: 20px; 
}
```
## 박스 모델의 너비와 높이 지정
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
.box1 {
	width: 200px;
	height: 100px;
	background: #ff6a00;
}

.box2 {
	width: 50%;
	height: 100px;
	background: #0094ff;
}

div {
	margin: 10px;
}

</style>
</head>
<body>
	<div class="box1">
	
	</div>
	<div class="box2"></div>
</body>
</html>
```
## 이미지를 인라인 혹은 블록 레벨로 배치하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style media="screen">
    #block img{
        display: block;
        margin: 10px;
}

</style>
</head>
<body>
	<div id="inline">
		<img alt="그림1" src="images/bg1.png">
	    <img alt="그림1" src="images/bg2.jpg">
	    <img alt="그림1" src="images/bg3.jpg">
	</div>
	<div id="block">
		<img alt="그림1" src="images/bg1.png"> 
		<img alt="그림1" src="images/bg2.jpg"> 
		<img alt="그림1" src="images/bg3.jpg">
	</div>
</body>
</html>
```
## 블록 레벨 요소를 인라인 레벨 요소로 변경하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
nav ul li {
	display: inline;
}
</style>
</head>
<body>
	<nav>
		<ul>
			<li><a href="#">애완견 종류</a></li>
			<li><a href="#">입양 하기</a></li>
			<li><a href="#">건강 돌보기</a></li>
			<li><a href="#">더불어 살기</a></li>
		</ul>
	</nav>
</body>
</html>
```
## 블록 레벨 속성을 가지면서 인라인으로 배치
```html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <title>Insert title here</title>
  <style>
    nav ul li {
      display: inline-block;
      
    }

    nav {
      width: 100%;
      height: 60px;
      background-color: gray;
    }


    nav ul li {
      display:inline-block;
      
    }

    nav ul a {
      display:inline-block;
      text-decoration:none;
      color: #fff;
      padding:20px;

    }

    nav ul a:hover {
      background-color: rgb(27, 162, 215);
    }
  </style>

</head>

<body>
  <nav>
    <ul>
      <li><a href="#">애완견 종류</a></li>
      <li><a href="#">입양 하기</a></li>
      <li><a href="#">건강 돌보기</a></li>
      <li><a href="#">더불어 살기</a></li>
    </ul>
    <h2>애완견 종류</h2>
  </nav>
</body>

</html>
```
## 테두리 스타일 지정하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
div {
	width: 200px;
	height: 100px;
	display: inline-block;
	margin: 15px;
	border-width: 15px;  //테두리굵기;
	border-color: rgb(000,153,204);
}

.box1 {
	border-style: solid;
}
.box2 {
	border-style: dotted;
}
.box3 {
	border-style: dashed;
}
</style>
</head>
<body>
	<div class="box1"></div>
	<div class="box2"></div>
	<div class="box3"></div>
</body>
</html>
```

## 테두리 스타일 한꺼번에 지정하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
h1 {
	padding-bottom: 5px;
	border-bottom: 3px solid #ccc;
}
p{
    padding: 10px;
    border: 3px dotted black;
}
</style>
</head>
<body>
	<h1>박스모델</h1>
	<p>박스 모델은 실제 코넨츠 영역, 박스와 콘텐츠 영역 사이의 여백인 패딩(padding), 박스의
		테두리(border), 그리고 여러 박스 모델 간의 여백 인 마진(margin) 등의 요소로 구성되어 있습니다.</p>
</body>
</html>
```

## 테두리 모서리를 둥글게 처리하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
.round{
border: 2px solid red;
border-radius: 20px;

}
#bg{
background: url(../images/bg1.png) no-repeat;
background-size: cover;
}
div{
margin: 20px;
display: inline-block;
width: 300px;
height: 300px;
}
</style>
</head>
<body>
<div class="round"></div>
<div class="round" id="bg"></div>
</body>
</html>
```

## 테두리에 그림자 효과 추가하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
div {
	width: 200px;
	height: 100px;
	display: inline-block;
	margin: 15px;
	border: 2px solid;
	border-radius: 20px;
}

.box1 {
	box-shadow: 2px -2px 5px 0px black;
}

.box2 {
	box-shadow: 5px 5px 15px 5px gray;
}
</style>
</head>
<body>
	<div class="box1"></div>
	<div class="box2"></div>
</body>
</html>
```

## 다양하게 마진 값 지정 하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
div {
	width: 200px;
	height: 100px;
	background: #0094ff;
}

.box1 {
	margin: 30px 50px 30px 50px;
}

.box2 {
	margin: 40px 70px;
}

.box3 {
	margin: 50px;
}

.box4 {
	margin: 20px 5px 10px;
}

.box5 {
	margin: 0px auto;
}
</style>
</head>
<body>
	<div class="box1"></div>
	<div class="box2"></div>
	<div class="box3"></div>
	<div class="box4"></div>
    <div class="box5"></div>
</body>
</html>
```
## 다양하게 패딩값 지정하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
div {
	width: 200px;
	height: auto;
	margin: 15px;
	background: #0094ff;
	display: inline-block;
	color: white;
}

.box1 {
	padding: 10px 30px 10px 30px;
}

.box2 {
	padding: 30px 30px;
}

.box3 {
	padding: 10px;
}
</style>
</head>
<body>
	<div class="box1">패딩(padding)이란 콘텐츠 영역과 테두리 사이의 여백을 말합니다.</div>
	<div class="box2">패딩(padding)이란 콘텐츠 영역과 테두리 사이의 여백을 말합니다.</div>
	<div class="box3">패딩(padding)이란 콘텐츠 영역과 테두리 사이의 여백을 말합니다.</div>
</body>
</html>
```
## 박스 모델의 너비 결정하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
.box1 {
	box-sizing: content-box; width : 300px;
	height: 150px;
	margin: 10px;
	padding: 30px;
	border: 2px solid red;
	width: 300px;
}

.box2 {
	box-sizing: border-box;
	width: 300px;
	height: 150px;
	margin: 10px;
	padding: 30px;
	border: 2px solid red;
}
</style>
</head>
<body>
	<div class="box1">box-sizing="content-box</div>
	<div class="box2">box-sizing="border-box</div>
</body>
</html>
```
## 여러가지 박스를 가로로 배치하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
.box1 {
	padding: 20px;
	margin-right: 10px;
	background: #ffd800;
	float: left;
}

.box2 {
	padding: 20px;
	margin-right: 10px;
	background: #0094ff;
	float: left;
}

.box3 {
	padding: 20px;
	background: #00ff21;
	float: left;
}

.box4 {
	padding: 20px;
	border: 1px solid black;
	float: right;
	background: #ffffff;
}
</style>
</head>
<body>
	<div class="box1">박스1</div>
	<div class="box2">박스2</div>
	<div class="box3">박스3</div>
	<div class="box4">박스4</div>
</body>
</html>
```

## 2단 레이아웃 만들기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
div {
	border: 1px solid #ccc;
}

#container {
	width: 960px;
	padding: 20px;
	margin: 0 auto;
}

#header {
	padding: 20px;
	margin-bottom: 20px;
}

#contents {
	width: 620px;
	padding: 20px;
	float: left;
	margin-bottom: 20px;
}

#sidebar {
	width: 220px;
	padding: 20px;
	float: right;
	margin-bottom: 20px;
}

#footer {
	clear: both;
	padding: 20px;
}
</style>
</head>
<body>
	<div id="container">
		<div id="header">
			<h1>사이트 제목</h1>
		</div>

		<div id="sidebar">
			<h2>사이드바</h2>
			<ul>
				<li>일단 제 상황을 말하자면.. 일단 제 상황을 말하자면.. 일단 제 상황을 말하자면.. 일단 제 상황을 말하자면..
				일단 제 상황을 말하자면.. 일단 제 상황을 말하자면..
				</li>
			</ul>
		</div>
		<div id="contents">
			<h2>본문</h2>
			<ul>
				<li>잘털어 놓으셨어요. 마음에 힘든걸 담아두기만 하면 더 병이되더군요. 저는 그래서 마음이 엄청 힘들곤
					했었답니다. 예전에는 우울했지만 지금은 그정도는 아니더라도 한번씩 그러신것이면 분명히 마음에 상처나 힘든점이 있고,
					그것을 그저 인식하지 못하고 있는것 같습니다. 어쩌면 부모님을 걱정 시킬까 아니면 다른이유로 무의식적으로 누르고
					있을수도 있고요. 일단 일기를 쓰든 한글과 컴퓨터에 쓰든 자신의 마음을 솔직하게 써보는것을 추천드릴게요. 마음을
					정리하시고 정말 안되겠다면 부모님께도 말씀드리세요. 아니면 친구들한테도 정말 믿을수 있는 친구라면, 친구한테도
					해보시고요. 무슨 마음의 상처인지는 모르지만 꼭 낫기를 기도드립니다.</li>
			</ul>
		</div>
		<div id="footer">
			<h2>푸터</h2>
			<ul>
				<li>본 답변은 참고 용도로만 활용 가능하며 정확한 정보는 관련기관에서 확인해보시기 바랍니다. 위 답변은
					답변작성자가 경험과 지식을 바탕으로 작성한 내용입니다. 포인트로 감사할 때 참고해주세요.</li>
			</ul>
		</div>
	</div>
</body>
</html>
```

## 3단 레이아웃
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
div {
	border: 1px solid #ccc;
}

#container {
	width: 960px;
	padding: 20px;
	margin: 0 auto;
}

#header {
	padding: 20px;
	margin-bottom: 20px;
}

#contents {
	width: 420px;
	padding: 20px;
	float: left;
	margin-bottom: 20px;
}

#left-sidebar {
	width: 180px;
	padding: 20px;
	float: left;
	margin-bottom: 20px;
	margin-right: 20px;
	background: #ccc;
}

#right-sidebar {
	width: 180px;
	padding: 20px;
	float: right;
	margin-bottom: 20px;
	background: #ccc;
}

#footer {
	clear: both;
	padding: 20px;
}
</style>
</head>
<body>
	<div id="container">
		<div id="header">
			<h1>사이트 제목</h1>
		</div>
		
		<div id="left-sidebar">
			<h2>left 사이드바</h2>
			<ul>
				<li>일단 제 상황을 말하자면.일단 제 상황을 말하자면.. 일단 제 상황을 말하자면.. 일단 제 상황을
					말하자면.. 일단 제 상황을 말하자면.. 일단 제 상황을 말하자면.. 일단 제 상황을 말하자면...</li>
			</ul>
		</div>
		<div id="right-sidebar">
			<h2>right 사이드바</h2>
			<ul>
				<li>일단 제 상황을 말하자면.일단 제 상황을 말하자면.. 일단 제 상황을 말하자면.. 일단 제 상황을
					말하자면.. 일단 제 상황을 말하자면.. 일단 제 상황을 말하자면.. 일단 제 상황을 말하자면...</li>
			</ul>
		</div>
		<div id="contents">
			<h2>본문</h2>
			<ul>
				<li>잘털어 놓으셨어요. 마음에 힘든걸 담아두기만 하면 더 병이되더군요. 저는 그래서 마음이 엄청 힘들곤
					했었답니다. 예전에는 우울했지만 지금은 그정도는 아니더라도 한번씩 그러신것이면 분명히 마음에 상처나 힘든점이 있고,
					그것을 그저 인식하지 못하고 있는것 같습니다. 어쩌면 부모님을 걱정 시킬까 아니면 다른이유로 무의식적으로 누르고
					있을수도 있고요. 일단 일기를 쓰든 한글과 컴퓨터에 쓰든 자신의 마음을 솔직하게 써보는것을 추천드릴게요. 마음을
					정리하시고 정말 안되겠다면 부모님께도 말씀드리세요. 아니면 친구들한테도 정말 믿을수 있는 친구라면, 친구한테도
					해보시고요. 무슨 마음의 상처인지는 모르지만 꼭 낫기를 기도드립니다.</li>
			</ul>
		</div>
		<div id="footer">
			<h2>푸터</h2>
			<ul>
				<li>본 답변은 참고 용도로만 활용 가능하며 정확한 정보는 관련기관에서 확인해보시기 바랍니다. 위 답변은
					답변작성자가 경험과 지식을 바탕으로 작성한 내용입니다. 포인트로 감사할 때 참고해주세요.</li>
			</ul>
		</div>
	</div>
</body>
</html>
```
## relative 값으로 요소 배치하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
.box1 {
	float: left;
	width: 100px;
	background: #ffd800;
	margin-right: 10px;
	padding: 20px;
}

.box2 {
	position: relative;
	left: -50px;
	top: 30px;
	width: 300px;
	background: #0094ff;
	float: left;
	padding: 20px;
}
</style>
</head>
<body>
	<div class="box1">박스1</div>
	<div class="box2">박스2</div>
</body>
</html>
```

## absolute 값으로 요소 배치하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
#wrap {
	position: relative;
	width: 300px;
	height: 300px;
	border: 1px solid #ccc;
}

.box {
	position: absolute;
	width: 50px;
	height: 50px;
	background: #0094ff;
}

#crd1 {
	top: 0;
	left: 0;
}

#crd2 {
	top: 0;
	right: 0;
}

#crd3 {
	bottom: 0;
	left: 0;
}

#crd4 {
	bottom: 0;
	right: 0;
}

#crd5 {
	top: 100px;
	left: 100px;
}
</style>
</head>
<body>
	<div id="wrap">
		<div class="box" id="crd1"></div>
		<div class="box" id="crd2"></div>
		<div class="box" id="crd3"></div>
		<div class="box" id="crd4"></div>
		<div class="box" id="crd5"></div>
	</div>
</body>
</html>
```

## fixed 값으로 요소 배치하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
#fx {
	position: fixed;
	top: 5px;
	right: 5px;
	width: 50px;
	height: 50px;
	background: #ff6a00;
}

#content {
	width: 400px;
}

p {
	line-height: 30px;
}
</style>

</head>
<body>
	<div id="fx"></div>
	<div id="content">
		<p>fixed 값을 ...... 됩니다.</p>
	</div>
</body>
</html>
```
## 특정 요소 화면에서 감추기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
img{
margin: 10px;
padding: 5px;
border: 1px solid black;
}
.invisible{
visibility: hidden;
}
</style>
</head>
<body>
<img src="../images/bg1.png">
<img src="../images/bg2.jpg" class="invisible">
<img src="../images/bg3.jpg">
</body>
</html>
```
## 여러요소 쌓는 순서 조절하기
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
div#wrapper {
	position: relative;
}

#b1 {
	z-index: 1;
	background-color: red;
	top: 0;
	left: 0;
}

#b2 {
	z-index: 3;
	background-color: yellow;
	top: 20px;
	left: 70px;
}

#b3 {
	z-index: 1;
	background-color: blue;
	top: 70px;
	left: 20px;
}

div.box {
	position: absolute;
	width: 100px;
	height: 100px;
	border: 1px solid black;
	font-size: 26px;
}
</style>
</head>
<body>
	<div id="wrapper">
		<div class="box" id="b1">1</div>
		<div class="box" id="b2">2</div>
		<div class="box" id="b3">3</div>
	</div>
</body>
</html>
```
## 표 테두리 통합하기 및 분리하기
```html
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="utf-8">
<title>표 스타일</title>
<style>
.table1 {
	border: 1px solid black;
	caption-side: top;
	border-collapse: collapse; //안쪽 점선1개;
	border-collapse: separate; //안쪽 점선2개;
	border-spacing: 20px 10px;
}

.table1 td {
	border: 1px dotted black;
	padding: 10px;
	text-align: center;
}

body {
	font-family: "맑은 고딕", "고딕", "굴림";
}
</style>
</head>
<body>
	<table class="table1">
		<caption>프로축구 경기 일정</caption>
		<tr>
			<td>울산</td>
			<td>울산 vs 인천</td>
		</tr>
		<tr>
			<td>부산</td>
			<td>부산 vs 대전</td>
		</tr>
		<tr>
			<td>서울</td>
			<td>서울 vs 강원</td>
		</tr>
	</table>
</body>
</html>
```
## 빈 셀 표시하기 감추기
```html
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="utf-8">
<title>표 스타일</title>
<style>
.schedule {	
	border-collapse: separate; //안쪽 점선2개;
	margin: 20px;
}

td {
	border: 1px solid black;
	padding: 10px;
	text-align: center;
}
#tb1{
empty-cells: show;
}
#tb2{
empty-cells: hide;
}

body {
	font-family: "맑은 고딕", "고딕", "굴림";
}
</style>
</head>
<body>
	<table class="schedule" id="tb1">
		<caption>프로축구 경기 일정</caption>
		<tr>
			<td>울산</td>
			<td>울산 vs 인천</td>
			<td>Tv중계</td>
		</tr>
		<tr>
			<td>부산</td>
			<td>부산 vs 대전</td>
			<td></td>
		</tr>
		<tr>
			<td>서울</td>
			<td>서울 vs 강원</td>
			<td></td>
		</tr>
	</table>
	<table class="schedule" id="tb2">
		<caption>프로축구 경기 일정</caption>
		<tr>
			<td>울산</td>
			<td>울산 vs 인천</td>
			<td>Tv중계</td>
		</tr>
		<tr>
			<td>부산</td>
			<td>부산 vs 대전</td>
			<td></td>
		</tr>
		<tr>
			<td>서울</td>
			<td>서울 vs 강원</td>
			<td></td>
		</tr>
	</table>
</body>
</html>
```
## 연결 선택자
```html
ex) * section ul : section 밑에 ul 모두 적용.
    * section > ul : 자식중 바로 다음 ul만 적용.
    * section + ul : 형제중 바로 다음 ul 만 적용.
    * section ~ ul : 형제중 모든 ul 적용.

<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
#container ul{
  border: 1px dotted blue;
}
</style>
</head>
<body>
	<section id="container">
		<header>
			<h1>예약 방법 및 요금</h1>
		</header>
		<p>요안도라에 예약 하려면??</p>
		<ul>
			<li>예약 방법
				<ul>
					<li>직접 통화</li>
					<li>문자 남기기</li>
				</ul>
			</li>

			<li>요금
				<ul>
					<li>1인 40,000원</li>
					<li>2인 60,000원</li>
					<li>3인 80,000원</li>
					<li>4인 100,000원</li>
				</ul>
			</li>

		</ul>
	</section>
</body>
</html>
```

## 속성 선택자
``` html
[속성 = 값] 선택자 = 특정 값을 갖는 속성에 스타일 적용
[속성 |= 값] 선택자 = 특정 값이 가진 요소를 찾아 스타일 적용.
[속성 ~= 값] 선택자 = 여러 속성 값 중에 해당값이 포함 되어있는 요소를 찾아 스타일 적용.
[속성 ^= 값] 선택자 = 특정 값으로 시작하는 속성에 스타일 적용하기
[속성 $= 값] 선택자 = 특정 값으로 끝나는 속성에 스타일 적용하기

ex)  a[target ="_blank"]
     [title |="us]
     [class ~="button"]
     a[title ^="eng"]
     a[href $="html]


<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>속성 선택자</title>
<style media="screen">
ul {
	list-style: none;
}

li {
	display: inline;
	float: left;
	margin: 10px;
}

li a {
	padding: 5px 20px;
	font-size: 14px;
	color: blue;
	text-decoration: none;
}

.flat {
	background: blue;
	color: white;
}

[class~="button"] {
	border: 2px solid black;
	box-shadow: rgba(0, 0, 0, 0.4) 5px 5px;
}
</style>
</head>
<body>
	<ul>
		<li><a href="#">메뉴 1</a></li>
		<li><a href="#">메뉴 2</a></li>
		<li><a href="#" class="button">메뉴 3</a></li>
		<li><a href="#" class="flat button">메뉴 4</a></li>
	</ul>
</body>
</html>
```

## 속성 선택자

```html

<!DOCTYPE html>
<html>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style media="screen">
a[title |="us"]{
   background: url('../images/us.png') no-repeat left center;
   padding: 5px 25px;
}
a[title |="jap"] {
   background: url('../images/jp.png') no-repeat left center;
   padding: 5px 25px;
}

</style>
</head>
<body>
<ul>
<li>외국어 서비스</li>
<li><a href="#" title="us">영어</a></li>
<li><a href="#" title="us-english">영어</a></li>
<li><a href="#" title="japanese">일본어</a></li>
</ul>
</body>
</html>
```
## 가상클래스 선택자
```html

:link = 방문하지 않은 링크에 스타일 적용.
:visited = 방문한 링크에 스타일 적용.
:active = 웹 요소를 활성화 했을때 스타일 적용.
:hover = 웹 요소에 마우스 커서를 올려놓을 때의 스타일 적용.
:focus = 웹 요소에 초점이 맞추어 졌을때의 스타일 적용.
:enabled,:disabled = 요소를 사용 할 수 있을 때와 없을 때의 스타일 지정.
:checked = 라이오 박스나 체크 박스에서 항목을 선택했을 때와 스타일 지정.
:nth-child(n),nth-last-child(n) = n번째 자식 요소에 스타일 적용하기.

<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
.container {
	width: 960px;
	margin: 0 auto;
	background-color: #fff;
	border: 1px solid #E7E7E7;
}

header {
	height: 280px;
	margin: 0;
	background-image: url('../images/header-bg.png');
	background-position: left top;
}

.navi {
	background: #031a44;
	width: 960px;
	height: 60px;
}

.navi ul {
	list-style: none;
	height: 40px;
	padding-top: 10px;
	padding-bottom: 5px;
}

.navi ul li {
	float: left;
	display: inline;
}

.navi a:link, .navi a:visited {
	padding: 10px 5px 5px 35px;
	display: block;
	color: #fff;
	width: 150px;
	text-decoration: none;
}

.navi a:hover, .navi a:focus {
	text-shadow: 0px 2px 2px #000;
	color: #FC0;
}
.navi a:active {
	color: blue;
}
</style>
</head>
<body>
	<div class="container">
		<header></header>
		<nav class="navi">
			<ul>
				<li><a href="#">이용 안내</a></li>
				<li><a href="#">객실 소개</a></li>
				<li><a href="#">예약 방법 및 요금</a></li>
				<li><a href="#">예약 하기</a></li>
			</ul>
		</nav>
	</div>
</body>
</html>
```
## 가상 클래스 선택자

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
:root {
	font-family:"궁서";
}
body {
	background-color: #fff;
}

form fieldset {
	margin-bottom: 25px;
}

form legend {
	font-size: 15px;
	font-weight: 600;
}

input:disabled {
	background: #ddd;
	border: 1px #ccc solid;
}

input:checked+span {
	color: blue;
}
</style>
</head>
<body>
	<form>
		<fieldset>
			<legend>사용자 정보</legend>
			<label>이름<input type="text" disabled></label>
		</fieldset>
		<fieldset>
			<legend>신청 과목</legend>
			<p>이 달에 신청할 과목을 선택하세요.</p>
			<label><input type="radio" name="subject" value="speaking"><span>회화</span></label>
			<label><input type="radio" name="subject" value="grammar"><span>문법</span></label>
			<label><input type="radio" name="subject" value="white"><span>작문</span></label>
		</fieldset>
	</form>
</body>
</html>
```

## 가상 클래스 선택자
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
<style>
#container {
	text-align: center;
	color: #2b2b2b;
}
table {
	width: 200px;
	margin: 0 auto;
	border-collapse: collapse;
}
td {
	text-align: left;
	padding: 10px;
	padding-left: 20px;
}
table tr:nth-child(2n+1) {
	background-color: lightgray;
	color: black;
}
</style>
</head>
<body>
	<div id="container">
		<h1>건강에 좋은 건강 식품</h1>
		<table border="1">
			<tr>
				<td>블루베리</td>
			</tr>
			<tr>
				<td>귀리</td>
			</tr>
			<tr>
				<td>토마토</td>
			</tr>
			<tr>
				<td>블루베리</td>
			</tr>
			<tr>
				<td>블루베리</td>
			</tr>
			<tr>
				<td>블루베리</td>
			</tr>
			
		</table>
	</div>
</body>
</html>
```
