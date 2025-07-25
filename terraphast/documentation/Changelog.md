첫 회의 이후 변경 사항
=================

최적화
-------------

* 순위 지원 비트벡터 구현
* 부분 집합에 인덱스 벡터 대신 비트벡터 사용
* 자주 사용되는 여러 메소드 인라인 처리
* 제약 조건 중복 제거
* 제약 조건 재매핑 (번호 매기기에서 내부 노드 제거)
* 범위 벗어난 부모 트릭으로 합집합-찾기 저장 공간 절반으로 축소
* 이전 저장 공간 재사용으로 할당 방지
* 일부 마이크로 최적화

수정 및 기능
------------------

* 트리 끝까지 순회하지 않고 빠른 테라스 확인
* 하위 트리 계산 수정 (문제가 있는 입력 데이터로 인해 어설션 실패 발생)
* 카운팅 버그 수정 (통신 문제)
* 잘못된 루트를 가진 트리 카운트하지 않음
* 모든 계산을 콜백 메소드로 추출
* 로깅 + 스택 상태 데코레이터 구현
* 동형 검사 구현
* Appveyor로 Visual C++ 호환성 확인
* 이식성을 유지하기 위해 내장 함수 추출
