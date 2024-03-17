# CS
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

