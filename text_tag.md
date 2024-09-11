# 텍스트 관련 태그

## headings 태그

<h1></h1>, <h2></h2>

숫자가 작을수록 글자의 크기가 커짐

제목 이외에는 사용하지 않는 것이 좋음

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>heading 1</h1>
    <h2>heading 2</h2>
    <h3>heading 3</h3>
    <h4>heading 4</h4>
    <h5>heading 5</h5>
    <h6>heading 6</h6>
  </body>
</html>
```

## TEXT Formatting 태그

### B태그

(bold) 글씨체가 두꺼워짐. 의미론적 중요성 X

```html
<!DOCTYPE html>
<html>
  <body>
    <p>This text is normal.</p>
    <b>This text is bold.</b>
    <p style="font-weight: bold;">This text is bold.</p>
  </body>
</html>
```

### Strong

B태그와 동일하나, 의미론적 중요성 O

```html
<!DOCTYPE html>
<html>
  <body>
    <p>This text is normal.</p>
    <strong>This text is strong.</strong>
  </body>
</html>
```

### I

(ltalic) 텍스트 기울어짐. 의미론적 중요성 X

```html
<!DOCTYPE html>
<html>
  <body>
    <p>This text is normal.</p>
    <i>This text is italic.</i>
    <p style="font-style: italic;">This text is italic.</i>
  </body>
</html>
```

### EM

I태그와 동일하나, 의미론적으로 강조, 중요한 이라는 의미를 가짐

```html
<!DOCTYPE html>
<html>
  <body>
    <p>This text is normal.</p>
    <em>This text is emphasized.</em>
  </body>
</html>
```

### SMALL

작은 텍스트

```html
<!DOCTYPE html>
<html>
  <body>
    <h2>HTML <small>Small</small> Formatting</h2>
  </body>
</html>
```

### MARK

형광펜 사용

```html
<!DOCTYPE html>
<html>
  <body>
    <h2>HTML <mark>Marked</mark> Formatting</h2>
  </body>
</html>
```

### DEL

취소선

```html
<!DOCTYPE html>
<html>
  <body>
    <p>The del element represents deleted (removed) text.</p>
    <p>My favorite color is <del>blue</del> red.</p>
  </body>
</html>
```

### INS

밑줄

```html
<!DOCTYPE html>
<html>
  <body>
    <p>The ins element represent inserted (added) text.</p>
    <p>My favorite <ins>color</ins> is red.</p>
  </body>
</html>
```

### SUB/SUP

각각 아래첨자, 윗첨자 사용

```html
<!DOCTYPE html>
<html>
  <body>
    <p>This is <sub>subscripted</sub> text.</p>
    <p>This is <sup>superscripted</sup> text.</p>
  </body>
</html>
```

## 본문 태그

### P

단락 지정. 하나의 문단을 만들 때 쓰임

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>This is a heading.</h1>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
      magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
      consequat.
    </p>
    <p>
      Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
      sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
  </body>
</html>
```

### BR

강제 개행을 지정. 줄 바꿈

```html
<!DOCTYPE html>
<html>
  <body>
    <p>This is<br />a para<br />graph with line breaks</p>
  </body>
</html>
```

여러 개의 공백 입력 방법

```html
<!DOCTYPE html>
<html>
  <body>
    <p>This is&nbsp; a para&nbsp; &nbsp; graph</p>
  </body>
</html>
```

### PRE

pre태그 안에 작성된 content는 작성된 그대로 브라우저에 표시됨

```html
<!DOCTYPE html>
<html>
  <body>
    <p>HTML은 1개 이상의 연속된 공백(space)과 1개 이상의 연속된 줄바꿈(enter)을 1개의 공백으로 표시한다.</p>
    <pre>
var myArray = [];
console.log(myArray.length); // 0

myArray[1000] = true;  // [ , , ... , , true ]

console.log(myArray.length); // 1001
console.log(myArray[0]);     // undefined
    </pre>
  </body>
</html>
```

출력 결과

```html
var myArray = []; console.log(myArray.length); // 0 myArray[1000] = true; // [ , , ... , , true ]
console.log(myArray.length); // 1001 console.log(myArray[0]); // undefined
```

### HR

수평줄 삽입

```html
<!DOCTYPE html>
<html>
  <body>
    <h1>HTML</h1>
    <p>HTML is a language for describing web pages.</p>
    <hr />
    <h1>CSS</h1>
    <p>CSS defines how to display HTML elements.</p>
  </body>
</html>
```

### Q

짧은 인용문 지정. q태그 안 요소를 “(인용부호)”로 감싼다

```html
<!DOCTYPE html>
<html>
  <body>
    <p>Browsers usually insert quotation marks around the q element.</p>
    <p>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></p>
  </body>
</html>
```

### BLOCKQUOTE

긴 인용문 블록 지정. 브라우저에서 들여쓰기가 되어 출력

```html
<!DOCTYPE html>
<html>
  <body>
    <p>Browsers usually indent blockquote elements.</p>
    <blockquote>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore
        magna aliqua.
      </p>
    </blockquote>
  </body>
</html>
```
