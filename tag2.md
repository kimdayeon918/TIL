# 문서 형식 정리 태그

출력할 웹 페이지의 형식을 브라우저에게 전달

문서의 최상위에 위치하고, 대소문자 구분 X

```html
<!DOCTYPE html>
```

## html 태그

HTML 모든 요소의 부모이며, 웹페이지에 단 한개만 존재함 (!doctype은 예외)

lang태그는 html태그의 속성으로 이용되며 주로 사용할 언어를 지정해줄 때 사용

```html
<html lang="ko"></html>
```

## head 태그

문서의 머리를 나타내는 태그, 숨은 데이터를 정의하는 태그들이 들어감

메타데이터 사용을 위한 태그

주로 style, title, script, link 요소들 사용

이 부분은 화면에 표시되지 X

## title 태그

문서의 제목을 정의

웹페이지 본문에는 보이지 않으며, 브라우저의 탭 등에 표시됨

검색 엔진 등에서 가장 크게 보여지는 텍스트이므로 페이지의 특성을 드러내는 제목을 작성하는 것이 중요함

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>문서 제목</title>
  </head>
  <body>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
    aliqua.
  </body>
</html>
```

## style 태그

HTML 문서를 위한 style 정보 정의

## link 태그

외부 리소스와 연계 정보를 정의. html과 css연계에 많이 사용됨

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>문서 제목</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
    aliqua.
  </body>
</html>
```

## script 태그

client-side javascript 정의

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <script>
      document.addEventListener("click", function () {
        alert("Clicked!");
      });
    </script>
  </head>
  <body>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
    aliqua.
  </body>
</html>
```

src속성을 이용하면 외부 javascript파일을 로드할 수 있음

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <script src="main.js"></script>
  </head>
  <body>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
    aliqua.
  </body>
</html>
```

## meta 태그

웹 페이지의 보이지 않는 정보를 제공하는 데 쓰이는 태그

페이지 설명 요약, 핵심 키워드, 제작자, 크롤링 정책 등 수많은 정보 제공

descirpttion, keyworld, author 기타 메타데이터에 사용됨

메타데이터는 웹브라우저, 검색엔진 등에 의해 사용됨

### SEO

Search Engine Optimization 검색 엔진 최척화

meta 태그를 이용하여 description, keyworld, author, subject, classification 등의 정보 표기 가능

검색 엔진은 이런 정보를 적극 활용함

```html
<html>
  <head>
    <title>HTML 태그의 속성 - ofcourse</title>

    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />

    <meta
      name="description"
      content="태그는, 태그 내부에 값을 넣을 수 있을 뿐만 아니라, 태그마다 속성을 부여할 수 있습니다."
    />
    <meta name="subject" content="태그의 속성" />
    <meta name="classification" content="html" />
    <meta name="keywords" content="www,web,world wide web,html,css,javascript" />
    <meta name="robots" content="ALL" />
  </head>
  <body>
    ...
  </body>
</html>
```

charset속성은 : 브라우저가 사용할 문자셋 정의

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
  </head>
  <body>
    <p>안녕하세요</p>
    <p>Hello</p>
    <p>你好</p>
    <p>שלום</p>
    <p>สวัสดี</p>
  </body>
</html>
```

SEO를 위해 검색엔진이 사용할 키워드 작성

```html
<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript" />
```

웹페이지 설명

```html
<meta name="description" content="Web tutorials on HTML and CSS" />
```

코드를 30초마다 새로고침

```html
<meta http-equiv="refresh" content="30" />
```

메타데이터를 제외한 웹 페이지에 표시되는 대부분의 요소는 body안에 들어감

```html
<html>
  <head>
    <meta charset="utf-8" />
    <title>문서 제목</title>
  </head>
  <body>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
    aliqua.
  </body>
</html>
```
