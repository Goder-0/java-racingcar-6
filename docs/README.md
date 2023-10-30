# 자동차 경주

## 기능 목록
- [ ] 0에서 9 사이에서 무작위 값을 생성한다. - `NumberGenerator#createRandomNumber()`
- [ ] 자동차 경주는 n대의 자동차들이 참여할 수 있다. - `CarRacing#cars`
  - [ ] 자동차의 이름들을 입력받는다. - `Prompt#readCarNames()`
    - [ ] 자동차 이름은 쉼표로 구분한다. - `Splitter#splitCarNameWith()`
    - [ ] 자동차 이름은 5자 이내이어야 한다. - `Validator#isNotCarName()`
- [ ] 자동차 경주에서 자동자는 매 턴마다 행동한다. - `CarRacing#action()`
  - [ ] 자동차는 생성한 무작위 값이 4보다 크면 이동 가능하다. - `Car#isMovable()`
  - [ ] 전진 가능하면 전진한다. - `Car#move()`
- [ ] 경주에서 진행할 턴의 최대 횟수를 입력 받는다. - `Prompt#readMaxTurn()`
  - [ ] 입력 받는 턴은 숫자이다. - `Validator#isNumber()`
- [ ] 우승 자동차들을 알 수 있다. - `Referee#whichWinners()`
  - [ ] 자동차들중 우승 위치의 크기를 알 수 있다. - `Judgment#firstCarPosition()`
  - [ ] 우승 위치의 크기와 같은 자동차들을 알 수 있다. - `Judgment#isWinner()`

## 예외 요구 사항
- [ ] 사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException`을 발생시킨 후 애플리케이션은 종료되어야 한다.

### 추가 요구사항
- [ ] indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다.
- [ ] 3항 연산자를 쓰지 않는다. 
- [ ] 함수(또는 메서드)가 한 가지 일만 하도록 최대한 작게 만들어라. 
- [ ] JUnit 5와 AssertJ를 이용하여 본인이 정리한 기능 목록이 정상 동작함을 테스트 코드로 확인한다.

---
## 출력 문구
- 자동차 이름 입력 : `"경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)"`
- 횟수 입력 : `"시도할 회수는 몇회인가요?"`
- 실행 결과 : `"실행 결과"`
- 최종 우승자 : `"최종 우승자 :"`

## 입력 요구 사항
- 경주 할 자동차 이름 : 5자 이내의 문자열들(쉼표로 구분)
  - ex) `pobi,woni,jun`
- 시도할 회수 : 숫자