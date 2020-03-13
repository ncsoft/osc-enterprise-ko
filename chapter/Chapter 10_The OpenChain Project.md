# Chapter 10. The OpenChain Project
본 챕터에서는 OpenChain 프로젝트에 대해 설명합니다.
<br>
<br>

## 비즈니스 관점에서의 컴플라이언스
많은 회사들이 오픈소스 사용을 지지하지만, 오픈소스 라이선스를 준수하는 것은 어려워함 <br> 대부분의 컴플라이언스 이슈는 여러 소프트웨어와 하드웨어가 결합되면서 생기는데, 공급망을 모두 추적하기가 힘들어짐
<br>
기업이 가지고 있는 도메인 지식과, 오픈소스를 개발에 얼마나 활용하는지에 따라 오픈소스 컴플라이언스는 도전이 될 수 있음

(예시)
```
작은 부품을 개발하는 회사는 오픈소스 개발방법론이나 오픈소스 라이선스에 대해 익숙하지 않을 수 있고,
이러한 환경에서 작은 실수가 발생하면 컴플라이언스 문제로 이어진다.

이러한 문제를 해결하려면 공급망에서 오픈소스 컴플라이언스 문제를 해결해야 하지만,
공급망은 보통 전세계 여러 기업에 걸쳐 있기 때문에 추적하기 어려운 상황이 많음
```

<br>

## OpenChain Project
### 1. OpenChain Project 소개
OpenChain Project는 리눅스 재단에서 주도하여 2016년 10월에 시작된 프로젝트
- 현재 OpenChain Project는 라이선스 준수를 위한 산업 표준을 제정하고 있음
-	웹사이트: https://www.OpenChainproject.org/

> 프로젝트의 기본 아이디어는 “효과적인 오픈소스 관리를 위해 어떤 오픈소스를 활용하고 있는지 관리하자”이며, 그 목표는 현재도 유지 중이다.
<br>

### 2. OpenChain Project의 세 가지 분야
**Specification**
- 규모에 관계없이 조직이 오픈소스 컴플라이언스를 해결할 수 있도록 지원함
- OpenChain Specification의 목표는 Conformant를 갖는 것
- Conformant을 가진 조직은 웹사이트와 홍보 매체에 광고할 수 있고, 협력사와 고객사에 그들의 오픈소스 컴플라이언스를 신뢰하도록 도울 수 있음
- https://www.openchainproject.org/spec 에서 확인할 수 있음

**Conformance**
- 조직이 이러한 Specification을 준수하는 데 도움이 되는 준수 방법

**Curriculum**
- 기본적인 오픈소스 프로세스 및 모범 사례를 제공하는 커리큘럼
-	참고할 수 있는 프로세스, 정책, 교육자료 등을 제공
<br>

## 세 가지 분야
### 1. 주요 요구사항 제공
오픈소스 컴플라이언스 프로그램에 대한 핵심 요구사항들을 5개의 섹션으로 구분하였으며, 총 3가지 목표가 수립되어 있음

(예시) Goal 1의 1.1 항목
```
Goal 1: Know Your FOSS Responsibilities
1.1 A written FOSS policy exists that governs FOSS license compliance
of the Supplied Software distribution. The policy must be internally
communicated.

Verification Material(s):
1.1.1 A documented FOSS policy.
1.1.2 A documented procedure that makes Software Staff aware of the
existence of the FOSS policy (e.g., via training, internal wiki, or other practical communication method).

Rationale:
To ensure steps are taken to create, record and make Software Staff aware of the existence of a FOSS policy. Although no requirements are provided here on what should be included in the policy, other sections may impose requirements on the policy.
```

각 섹션에는 요구사항을 충족했음을 보장하기 위한 검증 자료 및 근거들이 수반되어야 함
<br>

### 2. 주요 프로세스에 대한 적합성 검증 방법
Specification은 핵심 요구사항을 설명하고 준수되었는지 확인하는 기준을 제공하지만, 그 자체만으로는 완전한 해결책이 되지 못함 <br> 온라인에서 제공하는 자체 인증 설문지를 통해 적합성을 검토해야 함

(예시)
```
1.a: Do you have rules that govern FOSS license compliance of the
Supplied Software distribution?
1.b: Are these rules internally communicated?
1.c: Are these rules documented?
1.d: Is your Software Staff aware of the rules that govern FOSS license compliance of the Supplied Software distribution?
1.e: Do you document, how you make your Software Staff aware of the existing procedures that govern FOSS license compliance of the Supplied Software distribution?
1.f: Do you make your software staff aware of the existence of the FOSS policy using at least one of the following methods?
```

 > 위 대답들에 대해 YES라고 대답할 수 있다면,  OpenChain Specification을 준수할 수 있다고 할 수 있다.

- 온라인 적합성 검토 링크: https://www.openchainproject.org/conformance
<br>

### 3. 교육 자료를 통한 적합성 지원
컴플라이언스 프로세스, 정책 및 기타 교육 자료를 제공하고 있으며, 다양한 규모의 조직들이 컴플라이언스를 구축하기 위한 일반적인 예시를 알려줌

(예시)
```
1. What is Intellectual Property?
2. Introduction to FOSS Licenses
3. Introduction to FOSS Compliance
4. Key Software Concepts for FOSS Review
5. Running a FOSS Review
6. End to End Compliance Management (Example Process)
7. Avoiding Compliance Pitfalls
8. Developer Guidelines
```

- 커리큘럼 링크: https://www.openchainproject.org/curriculum (Curriculum 자료는 가능한한 많이 활용될 수 있도록 CC-0 라이선스 하에 배포되고 있음)
<br>


## 여러 분야에서의 채택 장려
OpenChain Project는 다양한 시장 분야에서 오픈소스 컴플라이언스를 일관적으로 준수하기 위해 여러가지의 접근 방식을 고려하고 있음
- 14개 플래티넘 회원들이 OpenChain Project를 지원하고 있음 (Adobe, ARM, Cisco, Comcast, GitHub, Harman, Hitachi, Qualcomm, Siemens, Sony, Toyota, Western Digital, Wind River)
- 메일링 리스트를 통해 아이디어를 공유하고, 조직간 신뢰를 쌓고 있음
- OpenChain Specification은 온라인 또는 오프라인으로 Conformance 양식을 제출 받고 있음

> OpenChain Project Quick Start Quide 링크: https://www.openchainproject.org/quick-start
<br>

## OpenChain Project에 참여하기
- 메일링 리스트에 참여하기
-	매월 진행되는 컨퍼런스 콜이나 정기 회의에 참석하기

> 오픈소스에 관련된 프로젝트인만큼 OpenChain Project의 진입 장벽이 높지 않으므로 OpenChain Project 메일링 리스트에 가입하여 많은 커뮤니티에 참여해보는 것을 권함

- OpenChain Project Community 링크: https://www.openchainproject.org/community
