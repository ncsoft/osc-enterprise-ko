# Chapter 11. Software Package Data Exchange (SPDX)
본 챕터에서는 SPDX(Software Package Data Exchange)에 대해 설명합니다.
<br>
<br>

## SPDX 소개
소프트웨어를 정확하게 식별하기 위해 정보를 정확하게 전달하기 위한 공통의 언어를 가지고 있어야 하며, 이를 위해 제정된 소프트웨어 표준
<br>

### 1. SPDX 라이선스 목록
-	SPDX 라이선스 목록 식별자는 SPDX 문서, 소스 파일 등에서 라이선스와 예외를 쉽고 효율적으로 식별할 수 있도록 하는 것
-	최신 버전 SPDX 라이선스 목록은 [GitHub](https://github.com/spdx/license-list-data)을 통해 받는 것을 권장함

<p align="center">
<img src="/image/chapter11/spdx.png" width="600">
</p>

### 2. SPDX License ID
- 2013년에 오픈소스 프로젝트인 U-boot(임베디드 시스템에서 사용되는 부트 로더)에서 소스코드 파일마다 라이선스 목록 식별자가 사용되도록 채택되었음
-	SPDX Project는 이러한 접근법을 관심있게 보았고 2.1 버전부터 프로젝트의 소스코드마다 SPDX ID를 넣는 구문을 공식 채택하였음

    (예시)
    ```
    // SPDX-License-Identifier: MIT
    /* SPDX-License-Identifier: MIT OR Apache-2.0 */
    # SPDX-License-Identifier: GPL-2.0-or-later
    ````

<br>

### 3. SPDX Specification이 만들어진 배경
- 세계의 많은 개발자들이 동일한 오픈소스 패키지를 사용하고 있지만, 소스코드를 분석하여 협업을 하거나 분석 결과를 공유할 수 있는 기반이 없었음
- 따라서 많은 개발자들이 동일한 작업을 중복으로 수행하고 있었음
- 시간 절약과 데이터 정확도 향상을 위해 소프트웨어 패키지와 관련된 구성 요소, 라이선스, 보안 정보, 저작권 등을 통신하기 위한 공통 언어로 SDPX를 제정하였음
- SPDX 프로젝트는 Linux 재단에서 주도하는 프로젝트이며, 이 프로젝트에 참여하는 기여자들과 기술 및 법률 전문가들이 협력하여 소프트웨어 공급망의 다양한 이해관계자들이 충족할 수 있도록 SDPX 표준이 점차 발전되고 있음
<br>

### 4. SPDX 문서
SPDX Specification은 SPDX Document를 만들기 위해 필수적인 필드들에 대해 설명함

**SPDX 문서 구성요소** <br>
<p align="center">
<img src="/image/chapter11/spdx-docu.png">
</p>

- Document Creation Information <br> 버전 넘버, 라이선스, 저작권 등 툴로 처리하기 위해 필요한 정보들을 표시 (각 SPDX 파일에 하나의 인스턴스는 반드시 필요함) <br>
<br>
  (예시)
  ```
  SPDXVersion: SPDX-2.1
  DataLicense: CC0-1.0
  SPDXID: SPDXRef-DOCUMENT
  DocumentName: SPDX document for Time version 1.7
  DocumentNamespace: http://spdx.org/documents/d3e9fef0-00a0-4b39-bb28-ff3dc75c7200
  LicenseListVersion: 2.5
  Creator: Tool: Source Auditor Open Source Console
  Creator: Organization: Source Auditor Inc.
  Created: 2018-09-26T11:44:51Z
  ```

-	Package Information <br> 제품, 컨테이너, 구성요소, 업스트림 프로젝트, *.tar 파일의 내용 등 패키지 정보 기입 <br>
<br>
    (예시)
    ```
    PackageName: GNU Time
    SPDXID: SPDXRef-1
    PackageVersion: 1.7
    PackageFileName: time-1.7.tar.gz
    PackageSupplier: Organization: GNU
    PackageOriginator: Organization: GNU
    PackageDownloadLocation: ftp://ftp.gnu.org/gnu/time/
    PackageVerificationCode: dd5cf0b17bfef4284c6c22471b277de7beac407c
    PackageChecksum: SHA1: dde0c28c7426960736933f3e763320680356cc6a
    PackageLicenseConcluded: GPL-2.0+
    PackageLicenseInfoFromFiles: GPL-2.0+
    PackageLicenseInfoFromFiles: MIT
    PackageLicenseInfoFromFiles: GPL-2.0
    PackageLicenseDeclared: GPL-2.0+
    PackageCopyrightText: <text>Copyright (C) 1990, 91, 92, 93, 96 Free Software Foundation, Inc.</text>
    PackageSummary: <text>The ‘time’ command runs another program,
    then displays information about the resources used by that program, collected by the system while the program was running.</text>
    PackageDescription: <text>The ‘time’ command runs another program,
    then displays information about the resources used by that program,
    collected by the system while the program was running.
    You can select which information is reported and the format in which it is shown,
    or have `time’ save the information in a file instead of displaying it on the screen.</text>
    ```

-	File Information <br> 파일 이름, 라이선스, 저작권 등을 포함한 파일의 메타 데이터 기입 <br>
<br>
    (예시)
    ```
    FileName: ./time.c
    SPDXID: SPDXRef-4
    FileType: SOURCE
    FileChecksum: SHA1: 712d7f9dfde674283596ae2088550e3ff23ae1ba
    LicenseConcluded: GPL-2.0+
    LicenseInfoInFile: NOASSERTION
    FileCopyrightText: <text>Copyright Free Software Foundation, Inc</text>
    ```

- Snippet Information <br> 다른 원본 소스코드에서 가져온 스니펫인 경우 기입 <br>
<br>

  (예시)
  ```
  SnippetSPDXID: SPDXRef-5
  SnippetFromFileSPDXID: SPDXRef-2
  SnippetByteRange: 889:9002
  SnippetLineRange: 24:245
  SnippetLicenseConcluded: Apache-2.0
  LicenseInfoInSnippet: BSD-2-Clause-FreeBSD
  SnippetCopyrightText: <text>Copyright 2001-2016 The Apache Software Foundation</text>
  SnippetComment: <text> This snippet should have a related package with an external referenced,
  however, the maven-plugin only supports external references for the main package </text>
  SnippetName: Apache Commons Math v. 3.6.1
  ```

-	Information <br> 기타 정보 기입 <br>
<br>
    (예시)
    ```
    LicenseID: LicenseRef-FaustProprietary
    ExtractedText: <text>FAUST, INC. PROPRIETARY LICENSE:
    FAUST, INC. grants you a non-exclusive right to use, modify, and distribute the file provided that (a) you distribute all copies and/or modifications of this file, whether in source or binary form, under the same license, and (b) you hereby irrevocably transfer and assign the ownership of your soul to Faust, Inc. In the event the fair market value of your soul is
    less than $100 US, you agree to compensate Faust, Inc. for the difference. Copyright (C) 2016 Faust Inc. All, and I mean ALL, rights are reserved.</text>
    LicenseName: Faust (really) Proprietary License
    LicenseComment: <text>This license was extracted from the file
    InsufficientKarmaException</text>
    ```

- Relationships <br> SPDX 문서와 패키지 정보, 파일 정보 간 관계를 설명 <br>
<br>
    (예시)
    ```
    Relationship: SPDXRef-2 PREREQUISITE_FOR SPDXRef-1
    RelationshipComment: <text>The package foo.tgz is a pre-requisite for building the executable bar.</text>
    ```
<br>

### 5. SPDX 문서를 생성할 수 있는 툴들
- FOSSology: https://github.com/fossology/fossology
- ScanCode: https://github.com/nexB/scancode-toolkit
-	FOSSID: http://fossid.com/services/
-	Blackduck Hub: https://www.blackducksoftware.com/solutions/open-source-license-compliance
-	Source Auditor: http://sourceauditor.com/blog/source-auditor-supports-spdx-2/
-	Protocode: http://www.protecode.com/license-compliance-is-evolving-with-spdx/
<br>

### 6.	SPDX 문서를 Import 할 수 있는 툴들
-	SPDXTools: https://github.com/spdx/tools
-	FOSSology: https://github.com/fossology/fossology/releases/tag/3.2.0
<br>

### 7.	SPDX 관련 링크
-	SPDX 공식 홈페이지: http://www.spdx.org
-	SPDX Specification: https://spdx.github.io/spdx-spec/
-	SPDX License List: https://spdx.org/licenses/
-	SPDX 기술 워크그룹: https://spdx.org/WorkgroupTechnical
