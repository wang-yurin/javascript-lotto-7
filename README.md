# javascript-lotto-precourse

## 기능 구현 목록

### 1. 로또 구매 단계

- 구입 금액 입력

  - [x] 로또 구입 금액을 입력받는다.
  - [x] 숫자만 입력할 수 있다.
  - [x] 1,000원 단위로 구매할 수 있다.
  - [x] 구매 한도는 최대 100,000원이다.
  - [ ] 구입 금액에 따른 로또 발행 개수를 계산한다.

- 예외 처리

  - [x] 숫자가 아닌 값을 입력한 경우
  - [x] 1,000원 미만의 금액을 입력한 경우
  - [x] 1,000원으로 나누어떨어지지 않는 금액을 입력한 경우
  - [x] 구매 한도를 초과한 값을 입력한 경우

### 2. 로또 발행 단계

- 로또 발행 개수만큼 반복하여 수행한다.
  - [ ] 1부터 45 사이의 중복되지 않는 랜덤한 숫자를 6개 생성한다.
  - [ ] 오름차순으로 정렬한다.
- [ ] 모든 로또 번호를 출력한 후 다음 단계로 넘어간다.

### 3. 당첨/보너스 번호 입력 단계

- 당첨 번호 입력
  - [ ] 당첨 번호를 입력받는다.
  - [ ] 당첨 번호는 쉼표(,)를 기준으로 구분한다.
  - [ ] 각 숫자는 1부터 45 사이의 정수만 가능하다.
  - [ ] 6개의 숫자만 입력할 수 있다.
  - [ ] 중복되는 숫자를 입력할 수 없다.
- 보너스 번호 입력
  - [ ] 보너스 번호를 입력받는다.
  - [ ] 숫자는 1부터 45 사이의 정수만 가능하다.
  - [ ] 1개의 숫자만 입력할 수 있다.
  - [ ] 보너스 번호가 앞서 입력한 당첨 번호와 중복될 수 없다.
- 예외 처리
  - [ ] `당첨 번호 =>` 숫자와 쉼표(,) 이외의 문자가 입력된 경우
  - [ ] `당첨 번호 =>` 6개의 숫자가 아닌 경우
  - [ ] `당첨 번호 =>` 중복된 숫자가 있는 경우
  - [ ] `보너스 번호 =>` 숫자 이외의 문자가 입력된 경우
  - [ ] `보너스 번호 =>` 1개의 숫자가 아닌 경우
  - [ ] `보너스 번호 =>` 당첨 번호와 중복되는 경우
  - [ ] 1부터 45 사이의 정수가 아닌 경우

### 4. 로또 결과 분석 단계

- 당첨 내역 계산

  - 각 로또 번호에 대해 반복하여 수행한다.
    - [ ] 당첨 번호와 일치하는 숫자의 개수를 센다.
    - [ ] 보너스 번호와 일치하는지 확인한다.
    - [ ] 당첨 번호와 일치하는 숫자의 개수와 보너스 번호 일치 여부에 따라 등수를 판단한다.
  - [ ] 등수 별로 당첨된 로또 개수를 집계한다.

- 당첨 내역 출력
  - [ ] 당첨 통계 메시지를 출력한다.
  - [ ] '---' 구분선을 출력한다.
  - [ ] 등수별 당첨 개수를 아래 형식으로 출력한다.
    ```
    3개 일치 (5,000원) - X개
    4개 일치 (50,000원) - X개
    5개 일치 (1,500,000원) - X개
    5개 일치, 보너스 볼 일치 (30,000,000원) - X개
    6개 일치 (2,000,000,000원) - X개
    ```
- 수익률 계산 및 출력
  - [ ] 총 당첨 금액을 계산한다.
  - [ ] 수익률을 계산한다.
  - [ ] 수익률을 소수점 둘째 자리에서 반올림한다.
  - [ ] '총 수익률은 X%입니다.' 형식으로 수익률을 출력한다.

### 5. 공통 예외 처리 사항

- 사용자가 잘못된 값을 입력할 경우 에러를 발생시킨다.
- 에러 메시지는 `[ERROR]`로 시작한다.
- 에러 메시지를 출력한 후 해당 입력 단계부터 다시 진행한다.
- 모든 과정이 정상적으로 완료되면 프로그램을 종료한다.
