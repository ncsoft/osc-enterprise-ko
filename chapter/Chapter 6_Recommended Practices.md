# Chapter 6. Recommended Practices
본 챕터에서는 오픈소스 컴플라이언스의 각 절차마다 권장하는 사례와 컴플라이언스에 필요한 툴들을 소개합니다.
<br>
<br>

## 오픈소스 컴플라이언스 프로세스 내의 단계 별 권장 사례
### 1. 식별 단계
- 모든 컴포넌트
- 원본 위치
- 라이선스 정보 등 식별
<br>

### 2. 소스코드 감사 단계
- 모든 소스코드 스캔
- 새로운 버전 스캔
- 릴리즈 일정보다 먼저, 자주 스캔
<br>

### 3. 이슈 해결 단계
- 개발부서와 협의
- 개발자가 수정 사용했는지 확인
- 이슈 해결 후 소스코드 다시 스캔
<br>

### 4. 아키텍처 리뷰 단계
- 오픈소스 코드
- 독점 코드
- 상용 코드
- 의존성 및 결합 방식 검토
<br>

### 5. 승인 단계
- 이전 단계들이 모두 완료되었는지 확인
- 검토 결과 기록
<br>

### 6. 고지 단계
- 모든 저작권과 라이선스 정보 포함하여 고지
- GPL이 포함되어 공개해야 하는 경우, 소스코드를 받는 방법 고지
<br>

<p align="center">
<img src="/image/chapter6/process.png"> <br> [오픈소스 컴플라이언스 프로세스]
</p>


## 툴과 자동화
### 1. 소스코드 스캔 및 라이선스 식별 툴
**상용 툴**
- Antepedia (http://www.antepedia.com/)
- Black Duck Software (Synopsys) (https://www.blackducksoftware.com/)
- Flexera Software (https://www.flexerasoftware.com/)
- FOSSA (http://fossa.io/)
- FOSSID AB (http://www.fossid.com)
-	nexB (https://www.nexb.com/)
-	Protecode (Synopsys) (http://www.protecode.com/)
-	Rogue Wave Software (https://www.roguewave.com/)
-	WhiteSource Software (https://www.whitesourcesoftware.com/)
<br>

**오픈소스 툴**
- Binary Analysis Tool (http://www.binaryanalysis.org/)
-	FOSSology (https://www.fossology.org/)
<br>

### 2. 프로젝트 관리 툴
컴플라이언스 활동을 단계 별로 관리하기 위해 사용하는 툴
- Bugzila
- Jira
<br>

### 3. BOM 관리 툴
두 가지 BOM을 비교하여 버전 관리하는 데에 사용하는 툴

> 이 툴은 제조업에서는 보편적으로 사용하지만, 오픈소스 관리 측면에서는 많이 사용되지 않는다. <br> 시중에 나와있는 툴들을 활용하여 자체적으로 개발하는 것을 권장한다.
<br>

### 4. 결합 방식 분석 툴
링킹 방식을 분석하는 것 (특히 C, C++)
- Depchecker (Linux Foundation 제공)
