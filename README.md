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
## <thead>,<tbody>,<tfoot> 태그- 표 구조 정의하기
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

## <col>,<colgroup> 태그 - 여러 열 묶어 스타일 지정하기
```html
```
