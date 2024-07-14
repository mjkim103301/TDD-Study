## 보험료 정산하기

### 주요 기능
- 사용자는 다수의 사람들에게 금액을 지정하여 정산 요청을 할 수 있습니다.
- 요청받은 사용자는 정산하기 버튼을 통해서 요청한 요청자에게 금액을
  송금할 수 있습니다.
- 요청한 모든 인원이 정산을 완료한 경우에는 해당 요청은 정산완료
  처리됩니다.

### 부가 기능
- 요청자는 자신이 요청한 정산하기 전체 리스트의 정보를 확인할 수
  있습니다.
- 요청받은 사람은 자신이 요청받은 정산하기 전체 리스트의 정보를 확인할 수
  있습니다.
- 요청하기 또는 요청받는 사람은 여러 개의 요청을 생성 또는 요청받습니다.

## 클래스 역할 분리
- 사용자
- 보험료 계산
- 정산금 계산
- 정산 요청
- 정산금 송금
- 다른 계좌에서 부족한 금액 가져오기
- 정산 완료 확인
- 내가 요청받은 정산 목록
- 내가 요청한 정산 목록

## Entity
- 사용자(아이디, 이름)
- 보험료(아이디, 사용자 아이디, 보험료, 납부완료 여부, 납부 완료일 )
- 정산 요청(아이디, 요청자 아이디, 요청 이름, 요청일, 정산 완료일, 정산금 총액, 보험료 아이디)
- 정산액(아이디, 정산 요청 아이디, 피요청자 아이디, 정산금, 정산완료 여부, 정산 완료일)
- 계좌(아이디, 소유자 아이디, 잔액)