# Class, Object, Instance 🧑🏻‍💻

### Class

- Object를 만들어 내는 틀 (객체의 속성과 메서드의 집합)

### Object

- Class로 부터 만들어지는 실체, Class로 선언된 변수

### Instance

- Object가 메모리에 할당 된 상태, 런타임에 구독 되는 Object 이기도하고 Object 자체의 의미로 쓰이기도 함(AWS의 클라우드 가상서버의 의미도있음)

```javascript
class PersonUpdata {
  constructor(name = "ratel", age = 20) {
    //생성자 안에 props 값 지정시 기본옵션
    this.name = name; // this는 클래스로 부터 만들어지는 메모리가 할당 되었을 인스턴스를 가리킴 아래에 예시에서는 james를 가리켜서 james.name 등이 가능함.
    this.age = age;
  }

  ageUp() {
    //메서드
    this.age++;
  }
}

const ratel = new PersonUpdata(); //인스턴스 객체
const james = new PersonUpdate("james", 26); // 인스턴스 객체

james.ageUp();

console.log(james); // 결과값 => { name: "james", age: 27 }
```

- Js 의 객체, 인스턴스
  - Js는 객체지향언어지만 타 언어와 달리 prototype기반 객체지향을 구현하고 클래스없이 객체 생성이 가능하다 prototype의 객체를 내부적으로 상속하기에 모든 객체는 object 클래스의 인스턴스이다. 때문에 인스턴스와 객체를 따로 구분할 필요가 없다.
    > 따라서 타 언어의 엄격한 클래스와 인스턴스 모델과는 조금 다르다.
