# Chapter 8. Other Compliance-related Practices
본 챕터에서는 오픈소스 컴플라이언스 업무와 함께 수반되어야 하는 부가적인 업무들을 설명합니다.
<br>
<br>

### 1. 직원 평가
- 사용한 오픈소스 컴포넌트를 양식에 기입하여 제출해야 함
- 컴플라이언스 티켓에 대해 응답해야 함
- OSRB가 정한 가이드라인을 준수해야 함
- 내부 오픈소스 교육을 이수해야 함
<br>

### 2. 웹 포탈
- 내부/외부에서 접근 가능한 오픈소스 포탈을 운영해야 함
- 내부 포탈은 오픈소스 가이드라인과 교육 자료 등을 게시해야 함
- 외부 포탈은 오픈소스 패키지를 공개하고 라이선스 의무사항을 이행하는 목적으로 운영되어야 함
<br>

### 3. 메세징
- 내/외부적으로 명확하고 일관된 기조로 오픈소스 정책과 프로세스를 수립해야 함
- 오픈소스 관련 문의에 답변할 때 웹 사이트를 갖는 것이 특히 중요함
<br>

### 4. 교육
- 컴플라이언스 교육은 오픈소스 정책과 전략을 인지시키는 것임
- 비공식적인 교육
  - Brown Bag Seminar: 주로 점심시간에 진행됨
  - 신입사원 오리엔테이션: 컴플라이언스 정책에 대해 소개
- 공식적인 교육
  -	오픈소스를 사용하는 직원은 누구나 교육을 받아야 함
<br>

### 5. 개발자가 소스코드 변경 시 고려사항
- GPL, LGPL의 경우 의무사항이 따르므로 변경했을 때 고려해야 하는 내용을 안내해야 함
- 소스코드 공개해야 하는 경우 독점 소스코드는 절대로 연동되지 않도록 안내해야 함
<br>

### 6. 고지문 고려사항
- 라이선스 전문, Copyright Notice, 소스코드 공개 시 획득 정보 포함해야 함
- 사용자 도큐먼트에 고지문을 게시하거나, UI상에 게시해야 함
<br>

### 7. 오픈소스 배포 시 고려사항
- 오픈소스 공개 의무사항을 적용 받는 모든 소스코드가 제품 출시 전에 모든 컴플라이언스가 준수되었는지 확인해야 함
<br>

### 8. 오픈소스 사용 시 고려사항
- BOM을 확정해야 함
  -	어떠한 소프트웨어도 오픈소스 사용 여부가 불확실하면 안됨
-	각 오픈소스 컴포넌트마다 OSRB 양식 제출
- M&A 거래 시 고려해야 할 사항
  -	기업 간 거래가 이루어지기 전에 사용한 오픈소스를 확인해야 함
- 사용하지 않는 오픈소스 패키지 관련
  - 오픈소스 패키지가 더 이상 사용되지 않는다면, OSRB에게 반드시 알려야 하며 오픈소스 사용 목록을 업데이트 해야 함
  - BOM diff 검증 툴을 활용하여 해당 오픈소스가 더 이상 사용하지 않는지 확인해야 함
- 대규모 소스코드 변경 관련
  - 대규모 변경사항이 있는 경우, OSRB에게 소스코드를 재 스캔 요청해야 함
  -	OSRB는 이전 버전과 변경된 소스코드를 확인하고, 아키텍처에 변경사항이 있는지 확인해야 함
- 원본 소스코드 출처
  - 오픈소스 소스코드 원본을 다운로드한 링크를 기입해야 함
- 오픈소스 업그레이드
  -	오픈소스 컴포넌트를 새 버전으로 업그레이드를 했다면 해당 컴포넌트를 검토받아야
  -	이전 버전과 라이선스가 변경되지 않았음을 확인해야 하고, 라이선스가 변경되었다면 다른 라이선스와 충돌은 없는지 검토해야 함
- 오픈소스 검증은 제품별, 서비스별로 진행
  - 오픈소스 컴포넌트가 승인되었다고 해서 다른 서비스에서도 사용되도록 승인된 것은 아님
  - 새로운 제품과 서비스라면 새로운 검증 절차를 거쳐야 함
- 소스코드 복사/붙여넣기
  -	소스코드 스니펫을 사용하거나 오픈소스 소스코드를 복사하여 독점 소스코드나 3rd Party 소스코드에 붙여넣기 하지 않아야 함
  - 이러한 경우는 컴플라이언스 검증에 심각한 영향을 미침
- 다른 라이선스와 혼합
  -	오픈소스 라이선스가 호환되지 않는 경우가 있기 때문에 원본 저작물에서 파생된 작업물의 라이선스를 혼합해서 사용하지 않아야 함
- 라이선스 정보 기입
  -	저작권과 라이선스 정보를 일부로 삭제하거나 수정하지 않아야 함
  -	모든 저작권과 라이선스 정보는 오픈소스 컴포넌트에 존재해야 함
<br>

### 9. 출처 표시 고려사항
제품에 오픈소스가 포함되어 있다면 최종 사용자에게 필수 권한을 알려야 함

- Attribution 종류
  - 전체 라이선스 사본
  - 저작권 표시
  - 취급 방침
  - 소스코드를 획득할 수 있는 정보 등

- Attribution 표시 방법
  - 제품이나 서비스마다 문서나 CDROM/DVD으로 Attribution을 포함하거나 웹사이트에서 다운로드 받도록 제공
  - 만약 GUI나 명령행 인터페이스를 제공하는 서비스라면, UI를 통해 표시할 수 있음
<br>

### 10. 특수한 라이선스 의무사항
- 최종 사용자가 반드시 라이선스를 볼 수 있도록 해야 함
- 최종 사용자가 반드시 copyright을 볼 수 있도록 해야 함
- 웹 매거진이나 웹 뉴스 등의 광고성 매체는 특별한 문구가 필요할 수 있음
  > 예) This product includes software developed by the University of California, Berkeley and its contributors.
<br>

### 11. 일반적인 라이선스 가이드라인
-	오픈소스 프로젝트, 저작자 이름, 컨트리뷰터를 허용 없이는 홍보나 마케팅에 사용할 수 없음
-	수정된 오픈소스 소스코드를 다시 배포하는 경우, 기존 저작권은 유지하면서 해당 변경사항에 대해 회사 및 년도 등 저작권을 명확히 표시해야 함
-	기존 라이선스와 저작권 및 출처는 유지해야 함
-	소스코드의 주석에 사적인 코멘트나 경쟁 업체의 이름 등을 넣지 않아야 함
-	라이선스는 삭제하거나 수정하지 않아야 함