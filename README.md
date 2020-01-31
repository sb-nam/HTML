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
