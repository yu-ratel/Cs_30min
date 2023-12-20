# Json 🧑🏻‍💻

- **JavsScript 객체 문법으로 구조화 된 데이터 교환형식**

  - 여러 언어에서 데이터 교환형식으로 쓰이며 객체 문법 말고도 *단순 배열, 문자열*로도 표현 가능하다.

- JavaScript 객체 문법

  - Key && Value 로 구성 {key: value} (중복선언 => 후에 선언 된 key에 대응한 value가 덮어진다)

- Json 은 *독립적*이다

  - 독립적이기에 js 뿐만아닌 다양한 언어에서 사용할 수 있다.

- Json에서 데이터를 다룰 때는 스키마(tpye)구축이 중요하다.

  - 여러가지 tpye으로 작성한다면 혼동이 올 뿐더러 그것을 제어 하기 위한 코드가 더 필요하기 때문에
  - Json의 tpye

    - Js ob와 비슷하지만 undefined, 메서드는 포함되지않음

      > number, string, boolean, array, object, null ⭕️

      > undefined, method ❌

- Json의 직렬화(serialization), 역직렬화(Deserialization)

  - 직렬화

    - 외부의 시스템도 사용 가능하도록 하는 것

      > js -> json -> python

      > python -> json -> js

  - 역직렬화

    - 직렬화와 반대의 경우
      > json -> js

    > json -> python

- Json의 활용
  - 독립적인 강점을 가지고 있으므로 다른 시스템간 데이터를 교환하기에 api, 시스템을 구성하는 설정파일 등

#### json 역직렬화 예시

```javascript
const fs = require("fs");
// 파일에 관한 모듈 (파일을 읽고 쓰는 등)
const path = require("path");
// 디렉토리 경로 설정 모듈
const file = fs.readFileSync(path.join(_dirname, "__.josn"));
// fs 의 파일을 읽는 메서드
const jsObject = JSON.parse(file);
// json을 js ob 형태로 변환해주는 함수
```
