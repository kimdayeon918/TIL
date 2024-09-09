HyperText Markup Language

HyperText : 단순 텍스트 이상의 링크 등의 개념이 포함된 텍스트

Markup : <, >로 이루어진 태그를 사용하는 규격

웹 사이트에서 화면에 표시되는 정보를 약속한 것

태그들을 이용하여 텍스트 이상의 요소를 정의하는 약속된 언어

## 마크업

HTML, XML 등이 대표적인 마크업 언어

```xml
<?xml version="1.0" encoding="UTF-8"?>
<note>
	<to>Tom</to>
	<from>Amy</from>
	<heading>Reminder</heading>
	<body>Don't forget me this weekend!</body>
</note>
```

태그 : <> 안에 들어간 것

<>로 열고 </ >로 닫으며, 둘 사이에는 값이 들어감

꺽쇠 안에 들어가는 문자는 속성의 이름

태그 내부에 들어가는 값은 속성의 값

ex) <to>Tom</to>은 to변수에 해당되는 값이 Tom이라는 의미

HTML에서 태그는 자신의 이름에 따라 각자 특정한 역할을 갖고 있음

일반적인 마크업 언어에서는 태그 이름을 사용자가 지정하지만

HTML은 태그의 이름이 규칙으로 정해져 있고, 그 태그마다 역할이 다름

태그는 대소문자를 가리지 않지만 나중을 위해 소문자 사용

프론트엔드 프레임워크 등을 사용하면 사용자가 임의로 태그를 만들어 사용하는 경우도 존재

## 웹 브라우징

1. 사용자가 주소 (URL) 입력
2. 어떤 IP에 접속해야 하는지 알아냄 (DNS)
3. 브라우저가 해당 서버에 입력한 주소로 요청
4. 서버에서 브라우저의 요청을 해석하고 실행하여 결과 데이터 전송 (HTML, CSS, JS …)
5. 브라우저가 서버에서 받은 값을 해석하여 화면으로 출력
6. 웹 브라우징

프론트엔드는 서버를 구축하지 않고 바로 5, 6번에 해당되는 작업만 우선적으로 실행하면서 공부할 수 있음

## HTML 시작

HTML문서는 <!DOCTYPE html>로 시작해서 document type문서 형식을 사용

실제적인 html은 <html></html> 2행에서 시작

<head></head> 사이에는 doument title, 외부 파일의 참조, 메타데이터의 설정 등을 기술

메타데이터 : 데이터에 관한 구조화된 데이터로, 다른 데이터를 설명해주는 데이터

이 부분은 브라우저에 포함 X

웹 브라우저에 표현되는 부분은 <body></body> 사이에 기술

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Hello World</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>안녕하세요! HTML5</p>
  </body>
</html>
```

HTML요소는 시작 태그와 종료 태그 사이에 content로 이루어짐

## 어트리뷰트 (속성)

요소의 성질이나 특성을 정의하는 명세

요소는 어트리뷰트를 가질 수 있음

어트리뷰트는 요소의 세부적인 사항 또는 추가적 정보를 추가

어트리뷰트는 시작 태그에 위치해야 함
