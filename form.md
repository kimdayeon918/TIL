사용자가 입력한 데이터를 수집하기 위해서 사용하는 방식

웹 페이지에서의 입력 양식

ex) 로그인 창, 회원가입 폼

텍스트 필드에 글자를 입력하거나, 체크박스나 라디오 버튼을 클릭하고 제출 버튼을 누르면

백엔드 서버에 양식이 전달되어 정보를 처리

- 입력 방식 태그
  input
  textarea
  butten
  select
  checkbox
  radio butten
  submit butten

form 속성

| attribute | Value      | Description                              |
| --------- | ---------- | ---------------------------------------- |
| action    | URL        | 입력 데이터(form data)가 전송될 URL 지정 |
| method    | get / post | 입력 데이터(form data) 전달 방식 지정    |
| name      |            | 폼의 이름                                |

### HTTP requast method

GET과 POST는 HTTP프로토콜로 서버에 사용자 입력 데이터를 전달하는 방법

### GET

전송 URL에 입력 데이터를 쿼리스트링으로 보내는 방식

ex) http://jsonplaceholder.typicode.com/posts?userId=1&id=1

URL뒤에 ?를 붙여서 데이터의 시작을 알린 후, key-value의 형태로 데이터 전송

1개 이상의 데이터는 &를 사용해서 표기

데이터가 모두 노출되므로 보안의 위험

데이터의 한계 (255자)

Rest API에서 GET메소드는 모든 또는 특정 리소스의 조회 요청

### POST

Request body에 데이터를 담아 보내는 방식

ex) http://jsonplaceholder.typicode.com/posts

URL에 모든 데이터가 노출되지는 않지만 GET보다 속도는 느림

Rest API에서 특정 메소드의 생성 요청

```html
<!DOCTYPE html>
<html>
  <body>
    <form action="http://jsonplaceholder.typicode.com/users" method="get">
      ID: <input type="text" name="id" value="1" /><br />
      username: <input type="text" name="username" value="Bret" /><br />
      <input type="submit" value="Submit" />
    </form>
  </body>
</html>
```

submit butten 클릭 → input태그 안에 있는 값이 form태그 안에 있는 method속성 방식으로 action

속성에 있는 URL로 값 전달

## INPUT

form태그에서 가장 중요한 역할로, 사용자로부터 데이터를 입력받기 위해서 사용됨

type어트리뷰트로 기능이 결정됨

form태그 안에 있어야 데이터 전송이 가능하나, ajax를 사용할 때에는 안에 없어도 됨

서버로 전송되는 데이터는 name어트리뷰트를 키, value어트리뷰트를 값으로 하여 key = value

형으로 전송됨

type 속성을 통해 종류를 나타내고,

name을 통해 데이터의 이름

value를 통해 기본 값을 지정

| type 어트리뷰트 값 | Description                                      | HTML5 추가 | IE     | FF  | CR  | SF  | OP  |
| ------------------ | ------------------------------------------------ | ---------- | ------ | --- | --- | --- | --- |
| button             | 버튼 생성                                        |            | ◯      | ◯   | ◯   | ◯   | ◯   |
| checkbox           | 체크박스 생성                                    |            | ◯      | ◯   | ◯   | ◯   | ◯   |
| color              | 색깔 선택                                        | ◯          | X      | ◯   | ◯   | X   | ◯   |
| date               | 날짜 선택                                        | ◯          | X      | X   | ◯   | ◯   | ◯   |
| datetime           | 날짜와 시간 선택 (년 월 일 시 분 초)             | ◯          | X      | X   | X   | X   | X   |
| datetime-local     | 지역, 날짜 생성 (년 월 일 시 분 초)              | ◯          | X      | X   | ◯   | ◯   | ◯   |
| email              | 이메일 입력 (submit시에는 자동 검증한다)         | ◯          | ◯(10~) | ◯   | ◯   | X   | ◯   |
| file               | 파일 선택 form                                   |            | ◯      | ◯   | ◯   | ◯   | ◯   |
| hidden             | 숨겨진 form생성                                  |            | ◯      | ◯   | ◯   | ◯   | ◯   |
| image              | 이미지로 만들어진 submit버튼 생성                |            | ◯      | ◯   | ◯   | ◯   | ◯   |
| month              | 월 선택 form                                     | ◯          | X      | X   | ◯   | ◯   | ◯   |
| number             | 숫자 선택 (버튼으로 올리고 내릴 수 있다)         | ◯          | ◯(10~) | ◯   | ◯   | ◯   | ◯   |
| password           | 비밀번호 입력(비밀번호 입력처럼 내용이 감춰진다) |            | ◯      | ◯   | ◯   | ◯   | ◯   |
| radio              | radio버튼 생성 (다중 택일이다)                   |            | ◯      | ◯   | ◯   | ◯   | ◯   |
| range              | 슬라이드 바로 범위 내의 숫자 선택                | ◯          | ◯(10~) | ◯   | ◯   | ◯   | ◯   |
| reset              | 리셋 버튼                                        |            | ◯      | ◯   | ◯   | ◯   | ◯   |
| search             | 검색 버튼 (입력했을 때 x자가 나온다)             | ◯          | X      | X   | ◯   | ◯   | X   |
| submit             | 제출 버튼                                        |            | ◯      | ◯   | ◯   | ◯   | ◯   |
| tel                | 전화번호 입력                                    | ◯          | X      | X   | X   | X   | X   |
| text               | 텍스트 입력                                      |            | ◯      | ◯   | ◯   | ◯   | ◯   |
| time               | 시간 선택                                        | ◯          | X      | X   | ◯   | ◯   | ◯   |
| url                | url입력 form                                     | ◯          | ◯(10~) | ◯   | ◯   | X   | ◯   |
| week               | 주 선택 입력 form                                | ◯          | X      | X   | ◯   | ◯   | ◯   |

## SELECT, OPTION

드롭다운 리스트를 만듦 즉, 복수개의 리스트에서 복수개를 선택할 때 사용

input과 같은 형태로 전달

| tag      | Description      |
| -------- | ---------------- |
| select   | select form 생성 |
| option   | option 생성      |
| optgroup | option을 그룹화  |

| 어트리뷰트 | 설명                                        |
| ---------- | ------------------------------------------- |
| select     | 아무것도 선택하지 않았을 때 선택이 되어있음 |
| disabled   | 선택 할 수 없이 그냥 보임                   |
| size       | 한번에 얼마나 보일 것인가                   |
| multiple   | 한 번에 2개 이상을 선택 가능                |

## TEXTAREA

여러 줄의 글자를 입력할 때 사용

### 어트리뷰트

rows : 텍스트 입력 중에 보이는 라인 수

cols : 텍스트 입력 영역의 너비를 정함

## BUTTEN

클릭할 수 있는 버튼 생성

<input type =”button”> ≠

butten은 빈 태그가 아니기 때문에 텍스트나 이미지 삽입 가능

type 속성은 반드시 넣는 것이 좋다

어트리뷰트 종류

- butten
- submit
- reset

어트리뷰트만을 받는 input과 달리 butten 태그는 콘텐츠로 텍스트나 HTML요소를 받을 수 있다.

그러나 오래된 IE의 경우 value값이 아닌 콘텐츠를 보낼 수도 있어 주의해야 함

```html
<button type="submit" name="mybutton" value="foo">Click me</button>
```

위의 경우 IE6, IE7은 submit으로 click me를 보내기 때문에 input을 쓰는 것이 바람직

## FIELDLIST/LEGEND

관련된 입력 태그들을 그룹화 하기 위해 사용

legend는 fieldlist의 제목을 지어줌

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
  </head>
  <body>
    <fieldset>
      <legend>Login</legend>
      Username <input type="text" name="username" /> Password <input type="text" name="password" />
    </fieldset>
  </body>
</html>
```
