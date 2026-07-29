---
description: 지식에 태그를 등록하고 조건으로 검색 결과를 필터링하는 방법을 안내합니다.
---

# 태그 입력을 통한 지식 검색 필터링

태그를 사용하면 지식 검색 결과를 조건에 맞게 필터링할 수 있습니다.

### 태그 등록

#### 일반 문서

**지식 관리 → 지식 추가하기 → 데이터 업로드 하기**에서 **태그 입력**을 활성화합니다.

파일을 선택한 뒤 태그 키, 타입, 값을 입력합니다. 파일 하나에 여러 태그를 등록할 수 있습니다.

* **TEXT**: 영문자, 한글, 정수를 입력할 수 있습니다.
* **DATE**: 정수만 입력할 수 있습니다.
* **NUMBER**: 정수만 입력할 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>

#### SharePoint 문서

**지식 관리 → 지식 추가하기 → 데이터 업로드 하기**에서 **태그 입력**을 활성화합니다.

SharePoint에서 파일을 선택한 뒤 태그 키, 타입, 값을 입력합니다. 입력 가능한 값은 일반 문서와 같습니다.

<figure><img src="../../../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

### 등록한 태그 확인

**지식 관리 → 태그를 등록한 지식 선택 → 검색 태그 설정**에서 등록한 태그를 확인합니다.

태그는 `{태그 키}-{태그 타입}-{태그 값}` 형식으로 표시됩니다.

예를 들어 `year-TEXT-2017`은 태그 키가 `year`이고 타입이 `TEXT`인 태그입니다.

<figure><img src="../../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

### 검색 값과 태그 매핑

#### Agent

입력 변수를 설정한 뒤, 참조할 지식의 **검색 규칙 설정**에서 변수와 메타 태그를 연결합니다.

검색 규칙은 태그 값이 조건을 충족하는 지식만 검색합니다.

<figure><img src="../../../.gitbook/assets/image (330).png" alt=""><figcaption></figcaption></figure>

**태그 값**에서 매핑할 입력 변수를 선택합니다.

* 조건을 여러 개 설정하면 모든 조건을 만족하는 지식만 검색합니다.
* 예시에서는 `year_from` 이상이며 `year_end` 이하인 `year` 태그를 검색합니다.

<figure><img src="../../../.gitbook/assets/image (331).png" alt="" width="375"><figcaption></figcaption></figure>

#### Workflow

입력 변수를 설정한 뒤, 지식 노드의 **검색 규칙 설정**에서 변수와 메타 태그를 연결합니다.

워크플로우에서는 각 지식 노드에 검색 규칙을 따로 설정합니다. 설정하지 않으면 태그 조건 없이 지식을 검색합니다.

<figure><img src="../../../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>

**태그 값**에서 매핑할 입력 변수를 선택합니다.

* 조건을 여러 개 설정하면 모든 조건을 만족하는 지식만 검색합니다.
* 예시에서는 `year`와 `fiscal` 값이 모두 일치하는 지식을 검색합니다.

<figure><img src="../../../.gitbook/assets/image (333).png" alt="" width="375"><figcaption></figcaption></figure>

### 태그 필터 검색 예시

입력 조건이 `year >= 2016` 및 `year <= 2018`이면, `year` 태그가 `2017`인 지식이 검색됩니다.

<figure><img src="../../../.gitbook/assets/image (334).png" alt="" width="375"><figcaption></figcaption></figure>

#### 검색 규칙 설정

<figure><img src="../../../.gitbook/assets/image (335).png" alt="" width="375"><figcaption></figcaption></figure>

#### 검색 태그 설정

<figure><img src="../../../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure>
