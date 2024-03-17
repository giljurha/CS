##### CS
TDD(Test Driven Development)
테스트케이스를 작성하고
그 이후에 그에 맞는 코드를 작성한다
간단한 예를 들어 1 + 1, 3 + 3 등등 구현하고자 하는 다양한 케이스를 작성하고
그 이후에 코드를 작성한다.
선코딩 후 테스트를 하는 것이 아닌, 테스트 케이스 작성 후 코딩을 하는 기법이다.

Refactoring
코드를 다듬는 과정

DDD(Domain Driven Desgin)
추상적 철학, 접근법, 전략적 설계
큰도메인을 작은 도메인으로 나눈다
예컨대, 인터넷 예매 -> 예매 / 도면 / 상품 / 회원
<br>

MVI
Model View Intent
Model - UI의 상태, 로직
View - UI, ex) View, Compose
Intent - 의도 ex) user event

순수함수 view(model(Intent()))
Intent() - 모델을 변경, model() 새로운 모델로 렌더링, view() UI Evnets
단방향 흐름 user event -> Intent() -> Model -> View

MVI 는 MVVM에서 MV와 V부분을 심화한 부분
V는 그대로 두고 MV에서 Model과 Intent로 심화

MVVM
Model - Repository(Server, Room)
View Model - Intent, Model
View - View

SOLID

S Single Responsibility Principle SRP <br>
O Open-closed Principle OCP <br>
L Liskov Substitution Priniciple LSP <br>
I Interface Segregation Principle ISP <br>
D Dependency Inversion Principle DIP <br>

DRY 원칙

Don't Repeat Yourself

SRP 하나의 객체에 하나의 책임만 부여한다

OCP 확장에 열려있고, 변경에 닫혀있다
위반한 예제
```kotlin
class Animal(val name: String)

class AnimalSpeaker() {
  fun speak(animal: Animal) {
    when(animal.name) {
      "고양이" -> println("냐옹")
      "개" -> println("멍멍"
      }
    }
  }
}
```
준수한 예제
```kotlin
abstract class Animal( val name: String ) {
  abstract fun speak()
}
class Dog : Animal("개") {
  override fun speak() = println("멍멍")
}
class Lion : Animal("사자") {
  override fun speak() = println("어흥")
}
```
리스코프 치환 원칙

자식 클래스는 부모 클래스로 대체 가능해야 한다.
```Java
Collection<String> collection = new ArrayList<>();
collection.add("A");
collection.add("B");
collection.add("C");
```
인터페이스 분리 원칙

목적과 용도에 적합한 인터페이스만을 제공한다

의존성 역전 원칙







