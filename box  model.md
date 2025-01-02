### 박스 모델 Box model

모든 HTML요소는 박스 모양으로 구성되며, 이를 박스 모델이라고 함

1. 내용 content - 텍스트나 이미지가 들어있는 박스의 실질적인 내용 부분
2. 패딩 padding - 내용과 테두리 사이의 간격. 눈에 보이지 X
3. 테두리 border - 내용과 패딩 주변을 감싸는 테두리
4. 마진 margin - 테두리와 이웃하는 요소 사이의 간격. 눈에 보이지 X

- width - 한 요소의 너비
- background-color - 요소의 콘텐츠와 padding의 배경색
- color - 한 요소의 콘텐츠 색 (글자 색)
- text-shadow - 한 요소 안의 글자에 그림자를 적용
- display - 요소의 표시 형식을 설정함

![스크린샷 2024-05-08 230049.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/151abb81-d3dd-4a78-94a1-22300e104c3e/c264b9ea-f0dd-418d-844d-b71dfcdbc433/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-05-08_230049.png)

```html
<style>
  div {
    background-color: red;
    padding: 50px;
    border: 20px;
    margin: 50px;
  }
</style>
```

### 페이지 색 바꾸기

```css
html {
  background-color: #00539f;
}
```

### body 외부 정렬하기

```css
body {
  width: 600px;
  margin: 0 auto;
  background-color: #ff9500;
  padding: 0 20px 20px 20px;
  border: 5px solid black;
}
```

width: 600px; - body가 항상 600pixels의 너비를 갖도록 설정

margin: 0 auto; - margin 또는 padding 처럼 한 속성에 두 개의 값을 설정할 때,

                           첫번째 값은 요소의 상단과 하단

                           두번째 값은 좌측과 우측에 영향을 줌

padding: 0 20px 20px 20px; - padding은 콘텐츠 주위에 약간의 공간을 주기 위한 네 개의 값이 있음

                                                이 코드의 경우 상단에 no padding, 좌하우에 20pixels 설정

                                                상단, 우측, 하단, 좌측 순서로 값 설정

border: 5px solid black; - body 모든 면의 border를 5pixels 두께의 실선으로 설정
