# What is CSS?

## **Cascading Style Sheets**

오픈 웹의 핵심 언어 중 하나로

HTML이나 XML로 작성된 문서의 표시 방법을 기술하기 위한 언어

프로그래밍 언어 X 마크업 언어 X

웹 페이지를 꾸미려고 작성하는 코드임

요소가 화면, 종이, 음성이나 다른 매체 상에 어떻게 렌더링되어야 하는지 지정

### HTML 문서에 CSS 적용하기

인라인 스타일 Inline style

HTML요소 내부에 style 속성을 사용하여 CSS를 적용하는 방법

해당 요소에만 스타일을 적용할 수 있음

```html
<body>
  <h2 style="color:green; text-decoration:underline">인라인 스타일을 이용하여 스타일을 적용하였습니다</h2>
</body>
```

내부 스타일 시트 Internal style sheet

HTML문서 내의 head태그에 style태그를 사용하여 CSS 스타일을 적용

해당 HTML 문서에만 스타일 적용 가능

```html
<head>
  <style>
    body {
      background-color: lightyellow;
    }
    h2 {
      color: red;
      text-decoration: underline;
    }
  </style>
</head>
```

외부 스타일 시트 External style sheet

웹 사이트 전체의 스타일을 하나의 파일에서 변경할 수 있도록 해줌

외부에 작성된 이러한 스타일 시트 파일은 .css 확장자를 사용하여 저장됨

스타일을 적용할 웹 페이지의 head태그에 link태그를 사용하여

외부 스타일 시트를 포함해야만 스타일이 적용됨

```html
<haed>
  <link rel=”stylesheet” href=”styles/style.css” type="text/css"/>
  <head
/></haed>
```

### 스타일 적용의 우선순위

1. 인라인 스타일
2. 내부/외부 스타일 시트
3. 웹 브라우저 기본 스타일

인라인 스타일이 적용된 태그는 내부, 외부 스타일 시트와 상관없이 인라인이 적용됨

내부, 외부 스타일 시트는 가장 마지막에 적용된 스타일 시트가 적용됨

### Ruleset

```css
p {
  color: red;
}
```

위의 예시와 같은 CSS의 전체 구조를 ruleset이라고 함

### 선택자 Selector

ruleset의 맨 앞에 있는 HTML 요소 이름으로, 꾸밀 요소를 선택한다

다른 요소를 꾸미기 위해서는 선택자만 바꿔주면 됨

### 선언

`color: red;`와 같은 단일 규칙. 꾸미길 원하는 요소의 속성을 명시함

### 속성 Property

주어진 HTML요소를 꾸밀 수 있는 방법, CSS, rule내에서 영향을 줄 속성을 선택

ex) color는 p요소의 속성

### 속성 값

속성의 오른쪽, 콜론 뒤, 주어진 속성을 위한 많은 결과 중 하나를 선택하기 위해

속성 값을 가짐

- 각각의 rule은 반드시 { } 로 감싸져야 함
- 각각의 선언 안에, 각 속성을 해당 값과 구분하기 위해 : 을 사용
- 각각의 rule안에 각 선언을 그 다음 선언으로부터 구분하기 위해 ; 을 사용

```css
p {
  color: red;
  width: 500px;
  border: 1px solid black;
}
```

### 여러 요소 선택하기

, 로 구분

```css
p,
li,
h1 {
  color: red;
}
```

### 선택자 종류

| 요소 or 타입 선택자 | 특정 타입의 모든 HTML요소                                     |
| ------------------- | ------------------------------------------------------------- |
| 아이디 선택자       | 특정 아이디를 가진 페이지의 요소 ( 한 페이지에 하나만 )       |
| 클래스 선택자       | 특정 클래스를 가진 페이지의 요소 ( 한 페이지에 여러 개 가능 ) |
| 속성 선택자         | 특정 속성을 갖는 페이지의 요소                                |
| 수도 클래스 선택자  | 특정 요소이지만 특정 상태에 있을 때만                         |

### \* 선택자

모든 태그를 선택하는 선택자

```css
* {
  //css code
}
```

### tag 선택자

주어진 이름의 태그를 선택하는 선택자

```css
body {
  /*body css code*/
}

header {
  /*header css code*/
}
```

### class 선택자

주어진 이름의 클래스를 선택하는 선택자

.을 붙여 클래스임을 구분지어 줌

```css
.name {
  /*name class css*/
}
```

### id 선택자

주어진 이름의 아이디를 선택하는 선택자

#을 붙여 아이디임을 구분지어 줌

```css
#title {
  /*title id css*/
}
```
