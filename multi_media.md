# 멀티미디어

## IMG 태그

이미지를 삽입하는 태그

src 속성을 통해 이미지 경로를 지정함

이미지 파일이 src 속성에서 지정한 경로에 없을 경우, 출력되지 않음

| attribute | Description                                  |
| --------- | -------------------------------------------- |
| src       | 이미지 파일 경로                             |
| alt       | 이미지 파일이 없을 경우 표시되는 문장        |
| width     | 이미지의 너비 (CSS에서 지정하는 것이 일반적) |
| height    | 이미지의 높이 (CSS에서 지정하는 것이 일반적) |

```html
<!DOCTYPE html>
<html>
  <body>
    <img src="assets/images/doug.jpg" alt="doug" width="100" />
    <img src="assets/images/wrongname.gif" alt="이미지가 없습니다." />
  </body>
</html>
```

## 미디어

### audio

| attribute | Description                                                                       |
| --------- | --------------------------------------------------------------------------------- |
| src       | 음악 파일 경로                                                                    |
| preload   | 재생 전에 음악 파일을 모두 불러올 것인지 지정                                     |
| autoplay  | 음악 파일을 자동의 재생 개시할 것인지 지정                                        |
| loop      | 음악을 반복할 것인지 지정                                                         |
| controls  | 음악 재생 도구를 표시할 것인지 지정. 재생 도구의 외관은 브라우저마다 차이가 있다. |

```html
<!DOCTYPE html>
<html>
  <body>
    <audio src="assets/audio/Kalimba.mp3" controls></audio>
  </body>
</html>
```

웹 브라우저마다 지원하는 음악 파일 형식이 다름

| Browser           | MP3    | Wav | Ogg |
| ----------------- | ------ | --- | --- |
| Internet Explorer | O      | X   | X   |
| Chrome            | O      | O   | O   |
| Firefox           | O(24~) | O   | O   |
| Safari            | O      | O   | X   |
| Opera             | O(25~) | O   | O   |

source태그를 사용하여 파일 형식의 차이 문제 해결 가능

type 속성은 생략 가능

```html
<!DOCTYPE html>
<html>
  <body>
    <audio controls>
      <source src="assets/audio/Kalimba.mp3" type="audio/mpeg" />
      <source src="assets/audio/Kalimba.ogg" type="audio/ogg" />
    </audio>
  </body>
</html>
```

## 비디오

| attribute | Description                                                                         |
| --------- | ----------------------------------------------------------------------------------- |
| src       | 동영상 파일 경로                                                                    |
| poster    | 동영상 준비 중에 표시될 이미지 파일 경로                                            |
| preload   | 재생 전에 동영상 파일을 모두 불러올 것인지 지정                                     |
| autoplay  | 동영상 파일을 자동의 재생 개시할 것인지 지정                                        |
| loop      | 동영상을 반복할 것인지 지정                                                         |
| controls  | 동영상 재생 도구를 표시할 것인지 지정. 재생 도구의 외관은 브라우저마다 차이가 있다. |
| width     | 동영상의 너비를 지정                                                                |
| height    | 동영상의 높이를 지정                                                                |

브라우저별 차이

| Browser           | MP4    | WebM | Ogv |
| ----------------- | ------ | ---- | --- |
| Internet Explorer | O      | X    | X   |
| Chrome            | O      | O    | O   |
| Firefox           | O(21~) | O    | O   |
| Safari            | O      | X    | X   |
| Opera             | O(25~) | O    | O   |

```html
<!DOCTYPE html>
<html>
  <body>
    <video width="640" height="360" controls>
      <source src="assets/video/wildlife.mp4" type="video/mp4" />
      <source src="assets/video/wildlife.webm" type="video/webm" />
    </video>
  </body>
</html>
```
