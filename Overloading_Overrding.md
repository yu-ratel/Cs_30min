# Overloading, Overrding 🧑🏻‍💻

### Overloading

- 같은 클래스 내에서 같은 메서드 이름으로 매개변수의 개수, 타입, 순서를 다르게하여 하나의 이름으로 *중복적*으로 처리할 수 있는 것 => 코드 가독성 ⬆️, 유연성 ⬆️ (add1, add2, add3 이런식의 작명은 지저분하고 유연성, 가독성이 떨어짐)

```java
public class OverloadingExample {
    public int add(int x, int y) {
        return x + y;
    }

    public String add(String x, String y) {
        return x.concat(y);
    }

    public static void main(String[] args) {
        OverloadingExample example = new OverloadingExample();
        System.out.println(example.add(1, 2));           // 3
        System.out.println(example.add("Hello, ", "World!")); // "Hello, World!"
    }
}
```

### Overrding

- 같은 클래스내에서 메서드를 중복적으로 처리하는 Overloading 과는 다르게 자식 클래스가 부모에게 상속받은 메서드를 _재정의_ 하는 것 => 다형성 ⬆️ (코드의 재사용성과 유연성을 높임)

```java
interface Shape {
    void draw();
}

class Circle implements Shape {
    public void draw() {
        System.out.println("원을 그립니다.");
    }
}

class Square implements Shape {
    public void draw() {
        System.out.println("사각형을 그립니다.");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape circle = new Circle();
        Shape square = new Square();

        circle.draw(); // "원을 그립니다."
        square.draw(); // "사각형을 그립니다."
    }
}
```

### JS에서는?

- Overloading

  - Js는 동적 타입 언어이기 때문에 메서드 오버로딩을 지원하지 않기에 함수 내에서 조건문을 사용하여 비슷한 동작을 구현한다.

- Overrding
  - 오버로딩과 같이 동적 타입 언어이기 때문에 개념적인 오버라이딩은 없지만 비슷한 효과를 내기 위하여 클래스 상속과, 프로토타입 체인을 이용하여 부모클래스에서 정의된 메서드를 재정의 할 수있다.
