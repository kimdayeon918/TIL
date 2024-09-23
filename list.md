## li 태그

목록을 만드는 태그

단독으로 쓰이지 않고 <ul></li> <ol></ol> 태그 내부에 들어감

단순히 리스트 나열 뿐만 아니라 메뉴 등을 만들 때도 사용

이중 리스트를 만들기 위해서는 ul이나 ol하위에 다시 ul, ol태그를 쓰면 됨

## 순서 없는 목록 Unordered List

```html
<!DOCTYPE html>
<html>
  <body>
    <h2>순서없는 목록 (Unordered List)</h2>
    <ul>
      <li>Coffee</li>
      <li>Tea</li>
      <li>Milk</li>
    </ul>
  </body>
</html>
```

## 순서 있는 목록 Ordered List

```html
<!DOCTYPE html>
<html>
  <body>
    <h2>순서있는 목록 (Ordered List)</h2>
    <ol>
      <li>Coffee</li>
      <li>Tea</li>
      <li>Milk</li>
    </ol>
  </body>
</html>
```

type 속성을 이용하여 순서를 나타내는 문자를 지정할 수 있음

| Value | Description     |
| ----- | --------------- |
| “1”   | 숫자 (기본값)   |
| “A”   | 대문자 알파벳   |
| “a”   | 소문자 알파벳   |
| “I”   | 대문자 로마숫자 |
| “i”   | 소문자 로마숫자 |

```html
<ol type="I">
  <li value="2">Coffee</li>
  <li value="4">Tea</li>
  <li>Milk</li>
</ol>
```

start 속성으로 시작 번호 지정 가능

```html
<ol start="3">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

reversed 속성은 순서를 반대로 바꿔줌

```html
<ol reversed>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

### 중첩된 목록

```html
<!DOCTYPE html>
<html>
  <body>
    <h2>중첩 목록</h2>
    <ul>
      <li>Coffee</li>
      <li>
        Tea
        <ol>
          <li>Black tea</li>
          <li>Green tea</li>
        </ol>
      </li>
      <li>Milk</li>
    </ul>
  </body>
</html>
```

## 테이블 (표)

| tag   | description                    |
| ----- | ------------------------------ |
| table | 표를 감싸는 태그               |
| tr    | 표 내부의 행(table row)        |
| th    | 표 내부의 제목 (table heading) |
| td    | 표 내부의 일반 셀 (table data) |
| thead | 표의 제목                      |
| tbody | 표의 본문                      |

```html
<!DOCTYPE html>
<html>
  <body>
    <table border="1">
      <tr>
        <th>First name</th>
        <th>Last name</th>
        <th>Score</th>
      </tr>
      <tr>
        <td>Jill</td>
        <td>Smith</td>
        <td>50</td>
      </tr>
      <tr>
        <td>Eve</td>
        <td>Jackson</td>
        <td>94</td>
      </tr>
      <tr>
        <td>John</td>
        <td>Doe</td>
        <td>80</td>
      </tr>
    </table>
  </body>
</html>
```

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/151abb81-d3dd-4a78-94a1-22300e104c3e/b62b7cbb-dafa-4762-bc91-b3c88f4dbc17/Untitled.png)

### 테이블 태그의 어트리뷰트

| attribute | Description                                                                  |
| --------- | ---------------------------------------------------------------------------- |
| border    | 표 테두리 두께 지정. (CSS border property를 사용하는 것이 더 나은 방법이다.) |
| rowspan   | 해당 셀이 점유하는 행의 수 지정                                              |
| colspan   | 해당 셀이 점유하는 열의 수 지정                                              |

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      table,
      th,
      td {
        border: 1px solid black;
        border-collapse: collapse;
      }
      th,
      td {
        padding: 15px;
      }
    </style>
  </head>
  <body>
    <h2>2개의 culumn을 span</h2>
    <table>
      <tr>
        <th>Name</th>
        <th colspan="2">Telephone</th>
      </tr>
      <tr>
        <td>Bill Gates</td>
        <td>555 77 854</td>
        <td>555 77 855</td>
      </tr>
    </table>

    <h2>2개의 row를 span</h2>
    <table>
      <tr>
        <th>Name:</th>
        <td>Bill Gates</td>
      </tr>
      <tr>
        <th rowspan="2">Telephone:</th>
        <td>555 77 854</td>
      </tr>
      <tr>
        <td>555 77 855</td>
      </tr>
    </table>
  </body>
</html>
```

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/151abb81-d3dd-4a78-94a1-22300e104c3e/db99438f-bdc5-44c7-a4e1-728fa31871fe/Untitled.png)
