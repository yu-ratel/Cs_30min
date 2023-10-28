# Abstraction (추상화) 🧑🏻‍💻

- 복잡한 데이터, 구조, 시스템 등을 *핵심*을 가려내 덜 자세하게 만드는 것 -> 복잡도 ⬇️

- 데이터 추상화

  - 공통점을 모으고 차이점은 버린다.

  ```javascript
  class Person {
    eat() {
      console.log("살기위해서 밥을 먹어야한다");
    }
  }

  class Ratel extends Person {
    eatingHabits() {
      console.log("고기가 없으면 안먹는다");
    }
  }

  class Minsu extends Preson {
    eatingHabits() {
      console.log("다이어트를 위해 샐러드만 먹는다");
    }
  }

  const ratel = new Ratel();
  const minsu = new Minsu();

  ratel.eat(); // 살기위해서 밥을 먹어야한다
  ratel.eatingHabits(); // 고기가 없으면 안먹는다
  minsu.eat(); // 살기위해서 밥을 먹어야한다
  minsu.eatingHabits(); //다이어트를 위해 샐러드만 먹는다
  ```

- 프로세스 추상화
  - 내부 프로세스를 숨기는 것 ex) 키오스크의 인터페이스
    > 주문하기를 누르면 어떤식으로 데이터를 활용하는지 단순히 주문할 수 있는 것 처럼 사용자입장에서 내부의 복잡한 로직을 알지않아도 되는 장점이 있다.
