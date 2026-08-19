---
description: 청크·임베딩으로 지식을 구성하는 방법을 안내합니다.
---

# 청크·임베딩 이해하기

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
