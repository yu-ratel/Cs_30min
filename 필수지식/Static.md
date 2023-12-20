# Static 🧑🏻‍💻

- Class의 Instance 가 아닌 Class에 직접 속해 변수, 메서드 등을 공유하는데 사용

  - 해당 Class로 만들어지는 객체 사이에서 _중복되는 메서드_, 속성등을 효율적으로 정의함

- 장점

  > Object 마다 하나의 Class의 메서드, 속성을 게속 이용하며 메모리를 먹는것이 아니라 Class 레벨에서 Static으로 지정하여 만드는 것이 명시적이고 메모리 효율성이 좋아진다.

- 단점

  > Static은 선언을 하자마자 사용하지않아도 메모리에 올라간다 => 쓰지않는 부분이 많다면 오히려 메모리를 효율이 떨어진다.

- Java 에서의 Static

  > static이 아닌 변수는 힙에 할당이 되서 자동으로 가비지에 들어가 처리가 되어 메모리가 회수 되지만 static으로 처리하면 메모리 에리어라는 영역에 흘러 가기 때문에 프로그램이 종료 될 때 까지 메모리가 회수되지않는다 => 메모리 효율이 떨어질 수있음.

- JavaScript 에서의 Static

  > Java와는 메모리 관리 방식이 달라서 JavaScript의 객체는 주로 메모리가 아닌 힙에 할당되고 메모리는 변수에대한 참조가 저장되기 때문에 가비지가 메모리 관리를 해준다 => Java와는 다르게 Class레벨 변수로 힙에 저장되지 않고 Class자체에 연결이 되어서 정적 메서드를 정의하는데 사용된다 -> 인스턴스와는 독립적이다.

```JavaScript
class MyClass {
  static staticVariable = "I'm a static variable";

  static staticMethod() {
    return "I'm a static method";
  }
}

// 클래스의 인스턴스 생성
const instance = new MyClass();

console.log(MyClass.staticVariable); // "I'm a static variable"
console.log(MyClass.staticMethod());   // "I'm a static method"

console.log(instance.staticVariable);  // undefined
console.log(instance.staticMethod());   // Error: instance.staticMethod is not a function

```
