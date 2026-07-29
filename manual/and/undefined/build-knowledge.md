---
description: 문서를 업로드해 청크·임베딩으로 지식을 구성하고 관리하는 방법을 안내합니다.
---

# 지식 구성하기

지식은 업로드한 문서를 청크로 나누고 임베딩해 LLM의 컨텍스트로 활용하는 데이터입니다.\
생성된 청크는 지식 검색과 LLM 응답 생성에 사용할 수 있습니다.

<figure><img src="../../../.gitbook/assets/스크린샷 2026-07-27 140441.png" alt=""><figcaption><p>&#x3C; 플레이그라운드 - 지식 관리 ></p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (347).png" alt=""><figcaption><p>&#x3C;지식 구성하기 화면></p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/스크린샷 2026-07-28 165729.png" alt=""><figcaption><p>&#x3C;지식 관리 → 지식 추가하기 → 데이터 업로드 하기></p></figcaption></figure>

### 지식 목록

* **지식 추가**: 지식을 만들고 문서를 업로드합니다.
* **태그**: 등록한 태그로 지식을 필터링합니다.
* **검색**: 제목으로 지식을 찾습니다.
* **삭제**: 지식을 삭제합니다. 사용하는 애플리케이션에 영향을 줄 수 있습니다.

### 데이터 추가

지식 이름을 입력하고 필요하면 설명을 추가합니다.

문서를 업로드하거나 빈 데이터로 지식을 만들 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (664).png" alt=""><figcaption></figcaption></figure>

문서 없이 만들려면 **빈 데이터로 생성**을 선택합니다.

<figure><img src="../../../.gitbook/assets/image (677).png" alt="" width="375"><figcaption></figcaption></figure>

파일을 끌어 놓거나 **찾아보기**로 문서를 업로드합니다. 업로드가 끝나면 **다음**을 선택합니다.

<figure><img src="../../../.gitbook/assets/image (666).png" alt=""><figcaption></figcaption></figure>

이어서 임베딩 옵션을 설정합니다.

### 데이터 임베딩

문서를 청크로 나누고 임베딩하는 방식을 설정합니다.

<figure><img src="../../../.gitbook/assets/스크린샷 2026-07-27 140905.png" alt=""><figcaption><p>&#x3C; 데이터 임베딩 전체 화면 ></p></figcaption></figure>

#### 청크 설정

청크는 문서를 검색 가능한 최소 단위로 나눈 결과입니다.

기본 설정을 사용하거나 필요에 맞게 조정할 수 있습니다.

<figure><img src="../../../.gitbook/assets/스크린샷 2026-07-27 140734.png" alt=""><figcaption></figcaption></figure>

* **세그먼트 식별자**: 청크를 나눌 문서 내 구분자입니다.
* **최대 청크 길이**: 청크 하나의 최대 길이입니다.
* **청크 중첩**: 인접한 청크 사이의 중복 길이입니다.

#### 품질 설정

청크 생성 방식을 설정합니다. 기본값은 **고품질 기본**입니다.

**고품질 Q\&A**를 선택하면 문답형 청크를 생성합니다.

<figure><img src="../../../.gitbook/assets/image (833).png" alt=""><figcaption></figcaption></figure>

#### 임베딩 모델

문서를 임베딩할 모델을 선택합니다.

**모델 관리**에서 `text-embedding` 태그가 있는 모델만 사용할 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (834).png" alt=""><figcaption></figcaption></figure>

#### 검색 설정

청크 검색 방식을 설정합니다.

<figure><img src="../../../.gitbook/assets/image (835).png" alt=""><figcaption></figcaption></figure>

* **유사도 검색**: 질문을 임베딩으로 변환해 의미가 비슷한 청크를 찾습니다.
* **키워드 검색**: 문서 용어와 일치하거나 유사한 키워드를 찾습니다.
* **하이브리드 검색(재랭크)**: 두 검색 결과를 결합한 뒤 재랭크 모델로 순위를 조정합니다. 재랭크 모델을 지원하는 LLM이 필요합니다.
* **하이브리드 검색(가중치)**: 두 검색 결과를 결합하고 설정한 가중치로 우선순위를 조정합니다.

### 지식 상세 보기

업로드한 문서와 임베딩 결과를 확인하고 관리합니다.

<figure><img src="../../../.gitbook/assets/image (669).png" alt=""><figcaption></figcaption></figure>

* **문서 추가**: 문서를 추가하고 임베딩합니다.
* **문서 관리**: 문서 목록, 검색 테스트, 지식 설정을 확인합니다.
* **문서 테이블**: 임베딩한 문서의 정보를 표시합니다. 애플리케이션에서 사용하려면 상태가 **사용 가능**이어야 합니다.
* **상세 정보**: 임베딩 결과의 세부 정보를 확인합니다.

<figure><img src="../../../.gitbook/assets/image (670).png" alt="" width="375"><figcaption></figcaption></figure>

* **청크 보기**: 생성된 청크를 확인하고 필요하면 수정하거나 추가합니다.

<figure><img src="../../../.gitbook/assets/image (678).png" alt=""><figcaption></figcaption></figure>

* **청크 설정**: 데이터 임베딩 화면에서 청크 설정을 다시 구성합니다.

<figure><img src="../../../.gitbook/assets/image (671).png" alt=""><figcaption></figcaption></figure>

* **아카이브**: 자주 사용하지 않는 문서를 비활성 상태로 보관합니다. 아카이브 데이터는 보관 비용이 상대적으로 낮습니다.
* **삭제**: 임베딩한 문서를 삭제합니다.

#### 검색 테스트

청크화한 데이터를 검색하고 결과를 확인합니다.

<figure><img src="../../../.gitbook/assets/image (270).png" alt=""><figcaption><p>&#x3C;검색 테스트></p></figcaption></figure>

#### 데이터 설정

지식 기본 정보, 임베딩, 검색, 공유 설정을 변경합니다.

<figure><img src="../../../.gitbook/assets/image (688).png" alt=""><figcaption><p>&#x3C;지식 설정></p></figcaption></figure>

**공유 설정**: 지식의 공유 여부를 설정합니다. [공유 · 발행 · 운영](../../undefined-2/)에서 자세한 내용을 확인하세요.
