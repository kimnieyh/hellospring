## Payment Service 개발
### 요구사항
- 해외 직구를 위한 원화 결제 준비 기능 개발
- 주문번호, 외국통화 종류, 외국 통화 기준 결제 금액을 전달받아서 다음 정보를 더해 Payment를 생성한다.
  - 적용 환율
  - 원화 환산 금액
  - 원화 환산 금액 유효시간 (30분)
- PaymentService.prepare() 메소드로 개발 
  - 결제 준비 기능이기 때문

### 개발 방법
- 빠르게 완성해서 가장 간단한 방법을 찾는다
- 작성한 코드가 동작하는지 확인하는 방법을 찾는다
- 조금씩 기능을 추가하고 다시 검증
- 코드를 이해하기 쉽게 코멘트 설명을 담는다 (3초 이내에 알아볼 수 없다면)

### 환율 가져오기
- https://open.er-api.com/v6/latest/{기준통화} 이용
- JSON 포맷으로 리턴되는 값을 분석해서 원화 환율 값을 가져온다
- JSON을 자바 오브젝트로 변환 
