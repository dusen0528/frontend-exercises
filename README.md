# frontend-exercises

![](https://velog.velcdn.com/images/_inho/post/9bd4d97c-0f51-4e70-9aea-201af3ca137c/image.png)

```
<head> 요소의 내용은 브라우저에 표시되지 않음
페이지에 대한 metadata를 포함

제목을 표시하는 <title>

<title>Datamotion Movie Database</title>
파일 링크와 스크립트

CSS : <style> 태그로 사입

<style>
    p {
        font-family: helvetica, sans-serif;
        letter-spacing: 1px;
        text-transform: uppercase;
        border: 2px solid rgba(0,0,200,0.6);
        display: inline-block;
        cursor:pointer;
    }
</style>
<link> 태그로 파일 참조

<link rel="stylesheet" href="sample.css">
JavaScript : <script> 태그로 삽입

<script>
    const para = document.querySelector('p');
    para.addEventListener('click', updateName);
    function updateName() {
        let name = prompt('Enter a new name');
        para.textContent = 'Player 1: ' + name;
    }
</script>
script src = 로 파일 참조

<script src="sample.js"></script>
페이지에 대한 메타 데이터를 포함
인코딩 설정

<meta charset="UTF-8">
IE 호환성

<meta http-equiv="X-UA-Compatible" content="IE=edge">
페이지 설명

<meta name="keywords" content="movie">
<meta name="description" content="Simple Movie Database">
<meta name="author" content="Randy">
````

## Open Graph Protocol 페이지에 대한 요약 정보
웹사이트가 OGP 를 지원한다면, 웹사이트를 들어가기도 전에 뭐하는 사이트인지 미리 알 수 있습니다.
payco.com의 url을 카카오톡 or dooray 메신저에 붙여 넣으면 다음과 같이 확인 할 수 있습니다.
![](https://velog.velcdn.com/images/_inho/post/ca0f6f79-01e9-4ea8-b6dd-258dae89f843/image.png)

```<meta name="og:url" content="http://www.payco.com">
<meta name="og:image" content=“http://image.toast.com/aaaaac/paycoNoti/payco_com.jpg">
<meta name="og:title" content="PAYCO.COM 사는게 니나노PAYCO">
<meta name="og:description" content="NHN 페이코의 간편결제 서비스, 착한소비 제로페이, 송금수수료 없는 제휴계좌, 매달 PAYCO포인트 리워드 혜택, 실적 조건 없이 적립되는 제휴카드, 실속있는금융 생활의 중심, PAYCO">
``` 
<br>
<br> 


---
# Character Sets and Encodings
- 글자나 기호들의 집합을 숫자로 정의한 것 

### ASCII
- 영문 알파벳을 사용하는 대표적인 문자 인코딩
- 7bit
- 한글 표현 불가능
<br>
### EUC-KR
- 한글 완성형 인코딩
- 8bit 문자 인코딩
- 한글은 2byte 사용하는 문자 집합

### UTF-8 (유니코드)
- 전세계 모든 문자열을 하나의 코드표로 통합
- 한문자를 저장하기 위해 최소 1byte ~ 최대 4byte까지 동적으로 사용
- 조합형, 완성형 등이 있다

#### charset이 잘못되면 생기는 일

charset = euc-kr, 파일은 UTF-8 인코딩이면..

또는 charset=utf-8 파일은 euc-kr 이면 ..

```
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="euc-kr" />
        <title>실습-02</title>
    </head>
    <body>
        <h1>euc-kr 한글 인코딩 테스트</h1>
    </body>

</html>
```
![](https://velog.velcdn.com/images/_inho/post/d876fa6e-aeb4-427b-bc37-34db3fe3df16/image.png)


--- 

## HTML 문서를 표현하는 모든 TAG는 두 분류중 하나에 속합니다.
#### Inline Tag
자신의 내용과 앞뒤 태그의 내용을 같은 라인에 출력하는 태그
```
대표적인 tag는 <span></span>

반드시 알아야할 테그

<span>, <a>, <br>
,<button>,<img>,<input>,<select>,<textarea>,<label>,<strong>
<abbr>, <acronym>, <b>, <bdo>, <big>, <cite>, <code>, <dfn>, <em>, <i>, <kbd>,<map>, <object>, <q>, <samp>, <small>, <script>,<sub>, <sup>,<tt>, <var>
```
#### Block Tag
자신의 내용과 앞뒤 태그의 내용을 다른 라인에 출력하는 태그(즉 좌우 너비가 100%)

```
주로 구조를 만들 때 사용

대표적인 tag는 <div></div>

다만 <p> 태그는 내부에는 인라인 요소만 표현할 수 있습니다.

반드시 알아야할 테그

<form>, <ul>, <p>, <table>, <div>,<address>
<h1>,<h2>, <h3>, <h4>, <h5>, <h6>
<article>, <aside>, <audio>, <blockquote>, <canvas>, <dd>, <dl>, <fieldset>, <figcaption>, <figure>, <footer>,
<header>, <hgroup>, <hr>, <noscript>, <ol>, <output>, <pre>, <section>, <video>

```

--- 
## HTML Text
```
<p> : 문단
<br> : new line
List
계층구조(목록)을 표현

순서 없는 목록 : <ul>, <li>

<ul>
    <li>우유</li>
    <li>계란</li>
    <li>빵</li>
    <li>후무스(중동의 김치)</li>
    <li>베이컨</li>
</ul>

순서 있는 목록(Ordered) : <ol>, <li>

<ol>
    <li>Avatar</li>
    <li>Avengers: Endgame</li>
    <li>Titanic</li>
    <li>Starwars: Force Awaken</li>
    <li>Avengers: Infinity War</li>
</ol>
```

**중요(Emphasis)와 강조(Strong importance)**
중요한 글자를 강조하기 위해 글자를 두껍게 표현하거나 기울여서 표현

```
<p><em>스래시 메탈</em> 밴드로는 <strong>메탈리카</strong>가 있습니다</p> <p>그리고 <strong>메가데스</strong>또한 말하지 않을 수 없죠.</p>
```
![](https://velog.velcdn.com/images/_inho/post/99a98055-b59f-4364-b34f-d4e9f099745b/image.png)

**a tag**

```
문법
<a href="링크할 주소">텍스트 또는 이미지</a>

예제1
<p>영화 데이터베이스</p>
<p><a href="http://www.imdb.com">IMDB</a>로 연결</p>
<p>영화 데이터베이스 <a href="http://www.imdb.com" title="세계에서 가장 큰 영화 데이터베이스">IMDB</a>로 연결
</p>
```

---
### URL 과 Path
- URL(Unified Resource Locator) : 웹 상의 어디에 위치하는지 결정하는 텍스트 문자열
- Path은 내부 파일을 찾기 위해 Path 사용
![](https://velog.velcdn.com/images/_inho/post/5c7ab020-7da3-4779-9126-8a6b300a2bf4/image.png)

### table ( 테이블 )
웹 문서에서 자료를 정리할 때 가장 많이 사용하는 태그
```
<table> 태그로 테이블을 시작

<tr> 태그로 테이블을 시작

<td> 태그로 행을 만듦

<th> 태그는 셀의 문자를 가운데 굵게 표시(제목에 사용)

```
<table border="1">
    <tr>
        <td>아바타</td> <td>2009</td> <td>제임스 카메론</td>
    </tr>
    <tr>
        <td>어벤저스: 엔드게임</td> <td>2019</td>
        <td>루소 형제</td>
    </tr>
</table>

```
<table border="1">
    <tr>
        <td>아바타</td> <td>2009</td> <td>제임스 카메론</td>
    </tr>
    <tr>
        <td>어벤저스: 엔드게임</td> <td>2019</td>
        <td>루소 형제</td>
    </tr>
</table>
```
#### 행 합치기 : colspan, 열 합치기 : rowspan
```
<style>
    *{
        font-size:20pt;
    }
    table,th,td {
        border: 1px double black;
        width: 800px;
    }

    .border-red{
        border: 1px double red;
        color:red;
    }
    .border-blue{
        border:1px double blue;
        color:blue;
    }
</style>

<table>
    <catpion>전 세계 박스 오피스</catpion>
    <thead>
        <tr>
            <th>제목</th>
            <th>연도</th>
            <th>감독</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>아바타</td>
            <td>2009</td>
            <td rowspan="2" class="border-blue">제임스 카메론</td>
        </tr>
        <tr>
            <td>타이타닉</td>
            <td>2002</td>
        </tr>
        <tr>
            <td>어벤저스: 엔드게임</td>
            <td>2019</td>
            <td>루소 형제</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="3" class="border-red">www.boxoffice.com</td>
        </tr>
    </tfoot>
</table>
```

![](https://velog.velcdn.com/images/_inho/post/72af2c2a-c1a0-4529-a850-deb291f5668b/image.png)

---
## Element

### Opening tag , Closing tag
![](https://velog.velcdn.com/images/_inho/post/5f502db7-3d44-425f-9565-06ad22c2bca2/image.png)

### 영역을 나누는 태그
- div
	- Division의 약자, 웹 사이트의 레이아웃을 만들 때 사용하는 태그
	웹 페이지에서 논리적 구분을 정의
	각각의 블록(공간)을 알맞게 배치하고 CSS  스타일을 적용
	Block level element
    ![](https://velog.velcdn.com/images/_inho/post/ecda754e-6423-4490-84bd-d0fb23c02850/image.png)

- span
	- 자체만으로는 어떠한 의미도 가지지 않음
	class, id의 전역 속성으로 스타일링을 위해 요소들을 그룹화
	Inline level element


- form
![](https://velog.velcdn.com/images/_inho/post/951550c8-f990-4009-9a8e-c5ecf8a33e03/image.png)

### 내용을 표현하는 태그
![](https://velog.velcdn.com/images/_inho/post/6c9b6858-7c0e-465f-96f3-7778bc006b56/image.png)

### Semantic tags
- 의미 없는 div 태그의 사용보다 문서의 내용을 쉽게 이해할 수 있도록 의미를 가지는 새로운 태그요소
![](https://velog.velcdn.com/images/_inho/post/68dde18a-d126-4fe2-a5cd-3b5f8b125834/image.png)

<table border="1">
  <thead>
    <tr>
      <th>Tag명</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>&lt;main&gt;</td>
      <td>문서의 주요 콘텐츠를 포함, 문서 내에 단 하나만 존재</td>
    </tr>
    <tr>
      <td>&lt;header&gt;</td>
      <td>문서 소개나 탐색을 돕는 요소들의 그룹</td>
    </tr>
    <tr>
      <td>&lt;nav&gt;</td>
      <td>현재 페이지 내, 또는 다른 페이지로의 링크</td>
    </tr>
    <tr>
      <td>&lt;aside&gt;</td>
      <td>주요 내용과 간접적으로만 연관된 부분</td>
    </tr>
    <tr>
      <td>&lt;section&gt;</td>
      <td>문서의 일반적인 구획, 여러 줌심 내용을 감싸는 공간</td>
    </tr>
    <tr>
      <td>&lt;footer&gt;</td>
      <td>문서의 아래쪽 작성자 구획, 저작권 데이터, 관련된 문서의 링크에 대한 정보</td>
    </tr>
    <tr>
      <td>&lt;figure&gt;</td>
      <td>문서의 멀티미디어 요소</td>
    </tr>
    <tr>
      <td>&lt;article&gt;</td>
      <td>글자가 많이 들어가는 부분(그 자체로 독립적으로 구분되거나 재사용 가능한 영역)</td>
    </tr>
  </tbody>
</table>

![](https://velog.velcdn.com/images/_inho/post/8ab28a7c-68c1-4a94-876a-3c6ecf2b7078/image.png)


---

# HTTP Method
<table border="1">
  <thead>
    <tr>
      <th>HTTP 메서드</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>GET</td>
      <td>특정 리소스의 표시를 요청합니다. GET을 사용하는 요청은 오직 데이터를 받기만 합니다.</td>
    </tr>
    <tr>
      <td>HEAD</td>
      <td>GET 메서드의 요청과 동일한 응답을 요구하지만, 응답 본문을 포함하지 않습니다.</td>
    </tr>
    <tr>
      <td>POST</td>
      <td>특정 리소스에 엔티티를 제출할 때 쓰입니다. 이는 종종 서버의 상태의 변화나 부작용을 일으킵니다.</td>
    </tr>
    <tr>
      <td>PUT</td>
      <td>목적 리소스 모든 현재 표시를 요청 payload로 바꿉니다.</td>
    </tr>
    <tr>
      <td>DELETE</td>
      <td>특정 리소스를 삭제합니다.</td>
    </tr>
    <tr>
      <td>OPTIONS</td>
      <td>목적 리소스의 통신을 설정하는 데 쓰입니다.</td>
    </tr>
    <tr>
      <td>PATCH</td>
      <td>리소스의 부분만을 수정하는 데 쓰입니다.</td>
    </tr>
    <tr>
      <td>CONNECT</td>
      <td>목적 리소스로 식별되는 서버로의 터널을 맺습니다.</td>
    </tr>
    <tr>
      <td>TRACE</td>
      <td>목적 리소스의 경로를 따라 메시지 loop-back 테스트를 합니다.</td>
    </tr>
  </tbody>
</table>

### GET 방식의 특징

데이터가 URL에 노출됩니다

예시: https://httpbin.org/get?no=1&id=marco&age=30
URL에 파라미터가 ?key=value 형태로 전달됨


데이터는 args 객체 안에 저장됩니다
URL에 데이터가 포함되어 있어 북마크가 가능합니다
데이터 크기에 제한이 있습니다 (브라우저마다 다르지만 보통 2048자)

### POST 방식의 특징

데이터가 URL에 노출되지 않습니다

예시: https://httpbin.org/post
데이터는 HTTP 요청 본문(body)에 포함됨


데이터는 form 객체 안에 저장됩니다
보안성이 상대적으로 높습니다 (URL에 데이터가 노출되지 않음)
대용량 데이터 전송이 가능합니다

### 사용 용도
GET: 데이터 조회(검색, 읽기)와 같은 단순 요청
POST: 데이터 생성/수정/삭제와 같이 서버의 상태나 데이터를 변경하는 요청

---
# HTTP Status Code
<div class="container mx-auto p-4">
    <table class="w-full border-collapse border border-gray-300">
        <thead class="bg-gray-100">
            <tr>
                <th class="border border-gray-300 p-2">상태 코드</th>
                <th class="border border-gray-300 p-2">분류</th>
                <th class="border border-gray-300 p-2">설명</th>
                <th class="border border-gray-300 p-2">세부 코드</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="border border-gray-300 p-2 font-bold">1XX</td>
                <td class="border border-gray-300 p-2">정보 전달</td>
                <td class="border border-gray-300 p-2">요청을 받았고, 작업을 진행 중</td>
                <td class="border border-gray-300 p-2">웹 소켓에서 주로 사용</td>
            </tr>
            <tr>
                <td class="border border-gray-300 p-2 font-bold">2XX</td>
                <td class="border border-gray-300 p-2">성공</td>
                <td class="border border-gray-300 p-2">요청이 성공적으로 처리됨</td>
                <td class="border border-gray-300 p-2">
                    <ul class="list-disc pl-4">
                        <li><strong>200</strong> - OK (성공)</li>
                        <li><strong>201</strong> - Created (리소스 생성 성공)</li>
                        <li>202 - Accepted (요청 수락, 미처리)</li>
                        <li>203 - Non-Authoritative Information</li>
                        <li>204 - No Content (성공, 컨텐츠 없음)</li>
                    </ul>
                </td>
            </tr>
            <tr>
                <td class="border border-gray-300 p-2 font-bold">3XX</td>
                <td class="border border-gray-300 p-2">리다이렉션</td>
                <td class="border border-gray-300 p-2">요청 완료를 위해 추가 동작 필요</td>
                <td class="border border-gray-300 p-2">
                    <ul class="list-disc pl-4">
                        <li>301 - Moved Permanently (영구 이동)</li>
                        <li>302 - Found (일시적 이동)</li>
                    </ul>
                </td>
            </tr>
            <tr>
                <td class="border border-gray-300 p-2 font-bold">4XX</td>
                <td class="border border-gray-300 p-2">클라이언트 오류</td>
                <td class="border border-gray-300 p-2">잘못된 요청</td>
                <td class="border border-gray-300 p-2">
                    <ul class="list-disc pl-4">
                        <li><strong>400</strong> - Bad Request (잘못된 요청)</li>
                        <li><strong>401</strong> - Unauthorized (인증 필요)</li>
                        <li><strong>403</strong> - Forbidden (접근 거부)</li>
                        <li><strong>404</strong> - Not Found (리소스 없음)</li>
                        <li><strong>405</strong> - Method Not Allowed (허용되지 않은 메소드)</li>
                    </ul>
                </td>
            </tr>
            <tr>
                <td class="border border-gray-300 p-2 font-bold">5XX</td>
                <td class="border border-gray-300 p-2">서버 오류</td>
                <td class="border border-gray-300 p-2">서버 응답 불가</td>
                <td class="border border-gray-300 p-2">
                    <ul class="list-disc pl-4">
                        <li><strong>500</strong> - Internal Server Error (서버 내부 오류)</li>
                        <li>501 - Not Implemented (미구현 기능)</li>
                        <li>502 - Bad Gateway (게이트웨이 오류)</li>
                        <li>503 - Service Unavailable (서비스 이용 불가)</li>
                        <li>504 - Gateway Timeout (게이트웨이 시간 초과)</li>
                    </ul>
                </td>
            </tr>
        </tbody>
    </table>
</div>