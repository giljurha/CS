# CS
<details>
  <summary> TDD란 무엇인가 ?</summary>
  
  테스트 케이스를 작성하고 그 이후에 그에 맞는 코드를 작성한다  
  예) 1 + 1, 3 + 3 등등 구현하고자 하는 다양한 케이스를 작성 후 코드를 작성  
  선코딩 후 테스트를 하는 것이 아닌, 테스트 케이스 작성 후 코딩을 하는 기법  
</details>

<details>
  <summary> Refactoring </summary>
  코드를 다듬는 과정
</details>

<details>
  <summary> DDD </summary>
  
  DDD(Domain Driven Design)  
  추상적 철학, 접근법, 전략적 설계  
  큰 도메인을 작은 도메인으로 나눈다  
  예컨대, 인터넷 예매 -> 예매 / 도면 / 상품 / 회원
</details>

<details>
  <summary> MVI </summary>
  
  MVI(Model View Intent)    
  M - UI의 상태 로직  
  V - UI  
  I - 의도, user event  
  순수함수 view(model(Intent()))  
  Intent() - 모델을 변경, model() 새로운 모델로 렌더링, view() UI Evnets  
  단방향 흐름 user event -> Intent() -> Model -> View  
  MVI 는 MVVM에서 MV와 V부분을 심화한 부분  
  V는 그대로 두고 MV에서 Model과 Intent로 심화  
</details>

<details>
  <summary> MVVM </summary>
  
  Model - Repository(Server, Room)  
  View Model - Intent, Model  
  View - View  
</details>

<details>
  <summary> SOLID 원칙 </summary>
  
  S Single Responsibility Principle SRP <br>
  O Open-closed Principle OCP <br>
  L Liskov Substitution Priniciple LSP <br>
  I Interface Segregation Principle ISP <br>
  D Dependency Inversion Principle DIP <br>
  
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

</details>

<details>
  <summary> List </summary>
  
  List - 순서 o 중복 o
</details>


<details>
  <summary> Set </summary>
  
  Set - 순서 x 중복 x  
  Set - HashSet, SortedSet( TreeSet은 SortedSet를 상속)
</details>


<details>
  <summary> Map </summary>
  
  Map - 순서 x, 중복 (키 x, 값 o)  
  Map - Hashtable, HashMap( LinkedHashMap이 상속 ), SortedMap( TreeMap이 상속 )
</details>

<details>
  <summary> Stack, Queue </summary>
  
  Stack - First in last out 선입후출, Queue - First in First out 선입선출
</details>

<details>
  
  <summary> Kotlin의 object를 통한 싱글톤, 스레드 세이프한가? </summary>
</details>

<details>
  <summary> 데이터 클래스란? </summary>
  
  - 생성자가 아닌 위치에 변수가 선언 됐을 때 발생할 수 있는 문제점
</details>

<details>
  <summary> 동물이라는 추상클래스에 대해 run이라는 메서드가 있는데, 이를 구현한 자식 클래스에서 run을 수행 시에 정지하도록 구현을 했다면 SOLID의 어떤 원칙을 위배한 건가? </summary>
</details>

<details>
  <summary>  원시 타입과 참조 타입에 대해 설명 </summary>
</details>

<details>
  <summary> 오토 박싱, 언박싱에 대해 설명 </summary>
</details>

<details>
  <summary> Checked Exception과 Unchecked Exception에 대해 설명 </summary>
</details>

<details>
  <summary> 라이브러리 vs 프레임워크 </summary>
</details>

<details>
  <summary> 동기와 비동기에 대한 설명 </summary>
</details>

<details>
  <summary> 동일성과 동등성에 대해 설명 </summary>
</details>

<details>
  <summary> 메소드 overriding vs overloading 에 대해 설명해주세요 </summary>
</details>

<details>
  <summary> abstract class 와 interface 의 차이점에 대해 설명해주세요 </summary>
</details>

<details>
  <summary> 캡슐화와 접근제한자에 대해 설명해주세요 </summary>
</details>

<details>
  <summary> Java와 Kotlin 언어의 차이점에 대해 설명해주세요 </summary>
</details>

<details>
  <summary> 함수형 프로그래밍에 대해 설명해주세요 </summary>
</details>

<details>
  <summary> 고차함수에 대해 설명해주세요 </summary>
</details>

<details>
  <summary> Kotlin 에서 null-saftey 기법을 설명해주세요 </summary>
</details>

<details>
  <summary> Kotlin SAM에 대해 설명해주세  </summary>
</details>

<details>
  <summary> lateinit, lazy 각각의 늦은 초기화 방법에 대해 설명해주세요 </summary>
</details>

<details>
  <summary> MSA(Micro Service Architecture)에 대해 설명해주세요 </summary>
</details>

<details>
  <summary> 정적이라고 하는 static에 대해 설명해주세요 </summary>
</details>

<details>
  <summary>  </summary>
</details>

<details>
  <summary>  </summary>
</details>

<details>
  <summary>  </summary>
</details>

<details>
  <summary>  </summary>
</details>





