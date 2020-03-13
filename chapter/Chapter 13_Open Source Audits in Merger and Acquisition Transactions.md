# Chapter 13. Open Source Audits in Merger and Acquisition Transactions
본 챕터에서는 인수 합병 거래에서 오픈 소스 감사 프로세스의 개요를 제공하고, 기업 거래에 대해 어떻게 더 잘 준비할 것인지에 대한 권고사항을 제시합니다.
<br>
<br>

## 소스코드 통합 시
<p align="center">
<img src="/image/chapter13/integration.png" width="600">
</p>

- 전체 오픈소스 코드나 부분 코드를 복사하여 독점 코드 내에 통합하여 사용
- 오픈소스 라이선스는 회사의 법적 책임과 코드 특성에 영향을 미칠 수 있는 다양한 의무를 수반하므로, 기업은 오픈소스 코드의 모든 통합과 사용을 추적 및 승인해야 함
<br>

## 소스코드 링킹 시
<p align="center">
<img src="/image/chapter13/linking.png" width="600">
</p>

- linking은 오픈소스 라이브러리를 사용하는 가장 일반적인 방식
-	결합된 코드는 별도의 디렉토리 또는 파일에 있을 가능성이 높기 때문에 탐지하는 것이 쉬울 수도 있음
<br>

> 소프트웨어 개발에 그래픽 프레임워크, 게임 엔진, SDK 등이 사용되어 개발 산출물에 일부가 포함될 수 있다. 정적으로 결합된다면 해당 부분의 라이선스도 확인해야 한다.

## 소스코드 수정 시
<p align="center">
<img src="/image/chapter13/modify.png" width="600">
</p>

- 오픈소스 컴포넌트에 새로운 코드를 추가/수정/삭제하는 것
<br>

## 오픈소스 감사
### 1. 오픈소스 감사를 왜 수행해야 하는가?
-	오픈소스 라이선스 의무사항으로 인해 M&A 기업의 사업 방향성과 틀어질 수 있음
-	이러한 리스크는 일찍 확인해야 하기 때문에 오픈소스 감사가 필요함
<br>

### 2. 오픈소스 감사를 위임해야 하는가?
- 오픈소스 감사 주체는 기업별, 인수 목적별, 소스코드 크기에 따라 다를 수 있음
- 예를 들어, 소규모 인수인 경우 일부 기업은 대상 회사에서 제공한 오픈소스 사용 BOM만 검토하는 것을 선호할 수도 있음
<br>

### 3. 감사 범위를 정하는 방법
소스코드 크기, 라인 수, 파일 수, 확장자 등을 미리 파악하여 감사 범위를 지정
<br>

### 4. 감사 방법
**전통적인 감사 방법** <br> 모든 소스코드에 접근하여 감사 시행 <br>
<p align="center">
<img src="/image/chapter13/traditional-audit.png" width="900">
</p>

**블라인드 감사 방법** <br>	감사자가 소스코드에 접근하지 않고 원격으로 감사
> 이 방식은 FOSSID에서 최초로 개발하였음

<p align="center">
<img src="/image/chapter13/blind-audit.png" width="900">
</p>

**DIY 감사 방법** <br> 감사 대상 회사에서 직접 수행 <br>
<p align="center">
<img src="/image/chapter13/diy-audit.png" width="900">
</p>
<br>

### 5. 보안과 버전 관리
보안 이슈가 있다면 전체 소프트웨어의 보안이 문제가 될 수 있기 때문에 보안 감사도 진행해야 함
<br>

### 6. 사전 및 사후 인수 규제
인수 회사는 대상 기업이 어떻게 오픈소스를 사용하고 관리하였는지, 의무사항을 얼마나 성공적으로 이행해 왔는지 명확하게 파악해야 함
<br>

### 7. 인수 대상 회사에서의 감사 준비
-	본인의 소스코드에 어떤 오픈소스가 포함되어 있는지 알아야 함
-	컴플라이언스에 적극적으로 참여해야 함
- 오픈소스를 보안취약점이 개선된 최신 소프트웨어 버전을 사용해야 함
- www.openchainproject.org/conformance) 사이트에서 현재의 컴플라이언스 준수 상태를 체크하는 것을 권장함
<br>

### 8. 인수 회사에서의 감사 준비
-	당사의 요구사항에 적합한 감사 방식을 선택해야 함
-	가장 우선적으로 어떤 것을 고려하고 확인해야 하는지 정리해야 함
- 감사를 진행하면서 대상 기업에게 확인해야 하는 질문들을 사전에 정리해야 함
  -	대상 또는 인수 회사의 IP에 리스크가 될 만한 라이선스와 소스코드를 사용하였는가?
  -	대상 기업에서 오픈소스 컴플라이언스가 충분히 진행되고 있는가?
  -	대상 기업에서 오픈소스 컴포넌트의 보안 취약점을 추적 관리하고 있는가?
  -	제품을 출시할 때 오픈소스 라이선스 의무사항을 준수하기 위해 고지문을 제공하고 있는가?
  -	대상 기업의 컴플라이언스 프로세스는 론칭 일정에 맞추기 위해 속도가 부합한가?
  -	대상 기업은 내부/외부 요청에 대해 적시에 소스코드 공개를 대응할 수 있는 절차를 갖추고 있는가?
-	라이선스 정책에 대해 기업간 충돌이 있다면 양사가 논의하여 합의 방안을 도출해야 함
-	인수 기업이 대상 기업에게 공식 컴플라이언스 정책과 프로세스를 수립하도록 도와주어야 함 (주로 대규모 기업이 작은 스타트업을 인수할 때)