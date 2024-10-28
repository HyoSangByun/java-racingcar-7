java-racingcar-precourse
=========================
* * *

🚀 기능 요구 사항
-----------------

- 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
- 각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.
- 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
- 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
- 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.


🚀 입출력 요구 사항
----------------------
### 입력 
- 경주할 자동차 이름(이름은 쉼표(,) 기준으로 구분)
- 시도할 횟수

### 출력
- 차수별 실행 결과
- 단독 우승자 문구 or 공동 우승자 문구


✨ 구현할 기능 목록
-------------------------
### 1. 입력 처리
- **기능**: 사용자로부터 자동차 이름들을 입력받기
  - **입력 형식**: 문자열
  - **유효성 검사**: 이름의 길이가 5이하인지 확인
  - **유효성 검사**: 이름이 null이거나 빈 문자열이 아닌지 확인
  - **유효성 검사**: 이름이 중복되지 않은지 확인
  - **유효성 검사**: 이름의 갯수가 n개를 넘지 않은지 확인
  - **유효성 검사**: 이름의 갯수가 최소 2개 이상인지 확인

- **기능**: 사용자로부터 이동할 횟수 입력받기
  - **입력 형식**: 정수
  - **유효성 검사**: 입력값이 정수 형태인지 확인
  - **유효성 검사**: 입력값이 n을 넘지 않는지 확인

### 2. 로직 구현
- **기능**: 무작위 값을 구한 후 무작위 값이 4이상인지 확인한다.
  - **알고리즘**: 라이브러리를 이용한다.

- **기능**: 자동차를 전진시킨다.
  - **알고리즘**: String 타입의 진행현황 변수에 "-"를 append한다.

- **기능**: 우승자를 확인한다
  - **알고리즘**: 정렬을 사용한다.

### 3. 출력 처리
- **기능**: 자동차 이름 입력 안내 메세지 출력
  - **출력 형식**: "경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)"

- **기능**: 이동 횟수 입력 안내 메세지 출력
  - **출력 형식**: "시도할 횟수는 몇 회인가요?"

- **기능**: 차수별 결과 출력
  - **출력 형식**: "_자동차 이름_ :  _현재 전진 횟수_"

- **기능**: 우승자 출력
  - **출력 형식**: "최종 우승자 : _우승자 목록_"

### 4. 예외 처리
- **기능**: 잘못된 입력 처리
  - **오류 메시지**: "유효하지 않은 입력입니다."

### 5. 테스트
- **기능**: 테스트 케이스 작성
  - **예외 1**: 이름의 길이 5초과 입력 => 오류 메시지 출력
  - **예외 2**: 이름으로 null이나 빈 문자열 입력 => 오류 메시지 출력
  - **예외 3**: 중복 이름 입력 => 오류 메시지 출력
  - **예외 4**: 이름 갯수 n 초과 입력 => 오류 메시지 출력
  - **예외 5**: 이동 횟수 양의 정수 외에 숫자 입력 => 오류 메시지 출력
  - **예외 6**: 이동 횟수 빈 문자열이나 null 입력 => 오류 메시지 출력
  - **예외 6**: 이동 횟수 정수 형태 외 문자열 입력 => 오류 메시지 출력
  - **예외 7**: 이동 횟수 n 초과 입력 => 오류 메시지 출력
  - **정상 1**: 단독 우승 조건 입력 => 단독 우승자 출력
  - **정상 2**: 중복 우승 조건 입력 => 중복 우승자 출력