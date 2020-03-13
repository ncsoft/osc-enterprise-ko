# Chapter 5. Compliance Processes and Policies
본 챕터에서는 오픈소스 컴플라이언스 프로그램에서 규정해야 할 정책과 프로세스에 대해 설명합니다. 소스코드를 공개해야 하는 프로세스와 버전 관리 프로세스도 함께 소개합니다.
<br>
<br>

## 정책
오픈소스 사용 정책은 컴플라이언스 프로그램에 필수적인 요소이며, 이해하기 어렵거나 복잡하지 않게 설정되어야 함

> 짧고 심플한 정책일수록 효과적이다!

(예)
```
- 개발자들은 어떠한 오픈소스라도 사용하기 전에 승인을 받아야 한다.
- 모든 소프트웨어는 검증이 되어야 한다.
- 고객에게 제품을 내보내기 전에 모든 라이선스 의무사항을 만족해야 한다.
- 변경된 오픈소스 컴포넌트는 모든 승인을 거친 후 라이선스를 변경해야 한다.
```
<br>


## 프로세스
소스코드 스캔, 오픈소스 식별, 법적 검토, 사용 승인 등의 과정 전체를 말함
<p align="center">
<img src="/image/chapter5/process-diagram.png">
</p>

### 1. 소스코드 스캔
스캐닝 툴로 스캔하는 과정

**스캔하는 시점**
  - 개발자가 사용 양식을 적어서 소스코드 스캔 요청 (Jira 등의 시스템으로 티켓 생성)
  - 정기적으로 스캔
  - 이전에 승인된 소프트웨어의 변경사항이 있는 경우
  - 3rd Party 개발사로부터 소스코드를 받은 경우
  - 웹에서 다운로드 받은 소스코드를 사용하는 경우
  - 빌드 시스템에 새로 통합되는 소프트웨어가 있는 경우
<br>

### 2. 이슈 식별
소스코드 스캔 결과에서 생성되는 이슈들을 식별해내는 과정
<br>


### 3. 법적 검토
법률 전문가가 라이선싱 이슈를 확인하고 해결 방안을 제공하는 단계

**라이선싱 이슈가 없다면** <br> 소프트웨어의 라이선스를 결정하고 다음 단계로 넘어가기 <br>

**라이선싱 이슈가 있다면** <br> 코드 재 작업을 위해 개발부서에 통보해야 함

> 라이선스를 정확히 식별할 수 없거나 판단할 수 있는 정보가 없는 경우, 해당 개발 부서에 문의하여 라이선스 확인을 받아야 함
<br>

### 4. 아키텍처 검토
컴플라이언스 담당자와 기술 담당자가 오픈소스와 독점 코드 등의 상호작용을 분석하는 단계

**분석 대상**
- 오픈소스 컴포넌트
- 독점 코드
- 3rd Party 개발사에서 제공받은 코드
- 의존성
- 통신 프로토콜
<br>


### 5. 최종 리뷰
오픈소스 사용 승인 여부를 알려주는 단계 <br> 일반적으로 대면 미팅으로 개발 부서에세 결과를 공유하며, 소프트웨어 구성요소가 승인되면 라이선스 의무사항을 작성하여 전달
<br>


## 프로세스별 Input과 Output
<p align="center">
<img src="/image/chapter5/input-output.png"> </p>

## 예상 시나리오별 프로세스
**100% 개발자가 개발한 코드라면** <br> 컴플라이언스를 진행할 것이 없기 때문에 바로 법적 검토와 아키텍처 검토만 진행함


**양립할 수 없는 라이선스가 있다면** <br> 소프트웨어를 스캔했을 때 양립할 수 없는 라이선스가 혼재되어 있다면 티켓을 개발부서에 넘겨서 코드를 수정하도록 안내


**링킹 방식과 관련해서 이슈가 있다면** <br> 법적 검토는 통과했으나 아키텍처 검토에서 이슈가 있다면 다시 티켓을 이슈 식별 단계로 되돌리고, 개발부서에 코드 수정하도록 안내


**더이상 사용되지 않는 소스코드가 있다면** <br> 제품에 포함되지 않도록 결정하고 티켓은 종료 & 다음에 이 소스코드를 사용하게 된다면 제품에 통합되기 전에 컴플라이언스를 거쳐야 함을 안내


**소스코드를 공개해야 한다면** <br> 법률 전문가는 독점 코드를 제거하도록 개발 부서에 안내해야 함 & 개발 부서에서 독점 코드도 포함해야 한다고 주장하는 경우, 독점 코드를 오픈소스로 공개해야 함을 인지시켜야 함


**해결되지 않은 이슈가 있다면** <br> 소프트웨어에 해결되지 않은 이슈가 남아 있다면 이슈 해결 후 다시 스캔하여 검토 과정을 거쳐야 함


**오픈소스가 승인되었다면** <br> BOM관리 툴에 소프트웨어 버전과 오픈소스 사용 목록을 업데이트하고 고지문 작성하여 소프트웨어 배포


**오픈소스가 반려되었다면** <br> 반려 사유를 기록해야 함
<br>


## Incremental Compliance
이미 검증 완료한 소프트웨어가 버전이 업그레이드될 때 진행하는 컴플라이언스 과정, 이 때 오픈소스 컴포넌트들을 BOM관리 툴로 기록하고 버전에 따른 변경사항은 BOM diff 툴로 추적 관리하는 것이 중요함
<p align="center">
<img src="/image/chapter5/incremental.png"> </p>


## 소스코드 감사 프로세스
감사 정책은 모든 소스 코드를 감사하고 준수 보고서에 감사 보고서를 첨부해야 함
<p align="center">
<img src="/image/chapter5/audit.png"> </p>


## 소스코드 공개 프로세스
이 제품에 오픈소스를 포함하고 있음과 고객이 소스코드를 희망한다면 제공받을 수 있다는 권한을 알려주는 것이며, 아래 절차가 포함되어야 함

### 1.소스코드 배포 방법 결정
- 누구나 접근할 수 있는 웹사이트로 배포
- 특정 고객에게만 보안을 거친 후 접근할 수 있는 웹사이트로 배포
- (GPL/LGPL의 경우) Written Offer로 공지하고 고객이 요구 시 배포
  ```
  Written Offer 예시
  To obtain a copy of the source code being made publicly available by FooBar, Inc.
  (“FooBar”) related to software used in this FooBar product (“Product”), you should
  send your request in writing to:
  FooBar Inc.
  Attention: Open Source Compliance
  Street Address
  City, State, Postal Code Country
  FooBar makes every possible effort to make the source code publicly available at http://opensource.foobar.com (“Website”) within reasonable business delays. Before sending your written request, please check the Website, as the source code may already be published there.

  또는

  To obtain a copy of the source code being made publicly available by FooBar,
  Inc. (“FooBar”) related to software used in this FooBar product (“Product”), you
  should send your request in writing to opensourcecompliance@foobar.com.
  FooBar makes every possible effort to make the source code publicly available at http://opensource.foobar.com (“Website”) within reasonable business delays. Before sending your written request, please check the Website, as the source code may already be published there
  ```
<br>

### 2. 소스코드 패키지 준비
<br>

### 3. 배포 전 체크리스트 확인
- 변경사항을 문서화했는지 확인
- 수정된 소스코드 파일에 저작권 고지 및 고지 의무사항이 충족되어 있는지 확인
- 컴플라이언스 검증 부서의 기술 담당자가 소스코드 패키지 내용을 확인
- 제품 설명서에 모든 소스코드 공개 의무사항이 포함되어 있는지 확인
- 배포하려는 패키지가 사내 PC가 아닌 최종 사용자와 동일한 환경에서 컴파일되는지 확인
- 웹 페이지에 소스코드 받을 수 있는 방법 안내했는지 확인
- Written Offer에 소스코드를 제공받을 수 있는 방안에 대해 커버되는지 확인
- 코드 리뷰 (주석에 기업 관련 정보가 들어있지는 않는지 등)
- 라이선스 텍스트 사본이 오픈소스 패키지의 LICENSE.txt 파일로 포함되어 있는지 확인 등
<br>

### 4.	소스코드 공개
<br>

### 5. 배포 후 체크리스트 확인
- 소스코드가 성공적으로 업로드 되었는지
- 소스코드가 외부 컴퓨터에서 에러 없이 다운로드 되는지
- 소스코드가 외부 컴퓨터에서 에러 없이 컴파일과 빌드도 되는지
