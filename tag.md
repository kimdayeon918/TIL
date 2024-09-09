# TAG

## 요소의 중첩

태그 안에 내용 뿐만 아니라 다른 태그도 들어갈 수 있음

태그는 연 순서대로 닫아야 함

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
  </head>
  <body>
    <h1>안녕하세요</h1>
    <p>반갑습니다!</p>
  </body>
</html>
```

위에서 html태그는 body태그 포함 등의 형식으로 부자관계 형성

중첩관계 표현을 위해서는 들여쓰기 사용

## 닫는 태그가 없는 태그

content를 가지지 않고 속성만을 가지는 태그로, 빈 요소라고 함

태그와 규칙을 맞춰주기 위해 <  /> 처럼 사용하기도 함

- 대표적인 빈 요소 태그
    
    <br> 줄 바꿈
    
    <hr> 선 긋기
    
    <img> 이미지
    
    <link> 외부에 있는 해당 문서나 외부 소스 사이의 관계를 나타낼 때
    
    <meta> 해당 문서에 대한 메타데이터를 정의
    
    <input> 입력 요소를 만듦
    

## 태그의 속성

태그는 내부에 값을 넣을 수 있을 뿐 아니라 태그마다 속성을 부여할 수 있음

<태그 속성=”값”>의 형태로 사용하며, 여러 속성을 부여할 수 있음

HTML에서는 태그의 속성도 미리 정의되어 있음

```html
<html>
<head>
	<link type="text/css" href="my_style.css">
</head>
<body>
	<font color="red" face="Dotum">Hello</font>
	<font color="yellow">World</font>
</body>
</html>
```

link태그에 link의 종류와 파일 위치가 어디인지를 정의하는 type와 herf 속성 사용

font태그에 색상과 글꼴을 정의하는 color와 face 속성 사용

## id, class 속성

모든 태그에는 id와 class속성을 지정해 줄 수 있음

id는 하나 당 하나의 태그에만 적용, class는 하나를 여러 태그에 적용 가능

```html
<div id="my-box1"></div>
<div id="my-box2" class="boxes"></div>
<div id="my-box3" class="boxes"></div>
<div class="boxes"></div>
```

## style 속성

태그의 스타일, 보이는 형태를 정의하는 속성

HTML문서 내에서 태그를 직접 설정할 때 쓰임

```html
<div style="width:500px; height:300px"></div>
<div style="height:40px; border: 1px solid green">mybox</div>
```

## DIV

Division

레이아웃을 나누는데 주로 쓰임

특별한 기능을 가지고 있지는 않음

가상의 레이아웃을 설계하는 데 쓰이며, 주로 CSS와 연동하여 쓰임

```html
<html>
	<body>
		<div style="background-color:cyan">구역1</div>
		<div style="width:100px; height:100px; background-color:#CF0">구역2</div>
	</body>
</html>
```

출력 결과

구역1                                                          

구역2                   

## SPAN

특별한 기능 X

CSS와 함께 쓰임

display속성이 block이 아닌 inline

div는 줄바꿈 O

span은 줄바꿈 X

```html
<html>
<body>
	<span style="background-color:red">span1</span>
	<span style="background-color:blue">span2</span>
	<span style="background-color:green">span3</span>
</body>
</html>
```

출력 결과

span1 span2 span3