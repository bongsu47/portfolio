---
description: 업로드한 문서를 확인하고 테스트합니다.
---

# 지식 상세 보기

### 문서 관리

<figure><img src="../../../.gitbook/assets/스크린샷 2026-08-13 130317.png" alt=""><figcaption></figcaption></figure>

* **다시 분석**: 등록한 파일을 다시 분석합니다.
* **변경 사항 동기화**: 연결한 폴더의 파일 추가·수정·삭제 내용을 반영합니다.

<figure><img src="../../../.gitbook/assets/image (863).png" alt=""><figcaption><p>업로드한 폴더에 문서 추가 혹은 삭제 후 변경 사항 동기화</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (864).png" alt=""><figcaption><p>동기화한 문서는 AI가 다시 분석합니다.</p></figcaption></figure>

{% hint style="info" %}
**변경 사항 동기화**는 폴더 자체를 동기화합니다.

MISO 내에개별 문서를 직접 추가하거나 삭제하는 기능은 없습니다. 폴더에서 변경한 내용을 동기화해 반영합니다.
{% endhint %}

#### 파일 검색과 메타데이터

파일 검색으로 등록한 문서를 찾습니다.

문서를 선택하면 다음 메타데이터를 확인하고 수정할 수 있습니다.

* **파일 분석**: 카테고리, 설명, 키워드를 확인하고 수정합니다.
* **탐색 힌트**: 질문 의도와 검색 키워드를 설정합니다. AI는 비슷한 질문에 이 정보를 사용해 파일을 선택합니다.

<figure><img src="../../../.gitbook/assets/image (865).png" alt=""><figcaption><p>원하는 문서 클릭 > 파일 분석, 탐색 힌트</p></figcaption></figure>

### 용어 사전

사내 약어와 업계 전문용어를 등록해 검색 정확도를 높입니다. 등록한 용어는 수정하거나 삭제할 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (866).png" alt=""><figcaption></figcaption></figure>

### 검색 테스트

검색 테스트로 문서가 예상대로 등록됐는지 확인합니다.

{% hint style="warning" %}
**검색하기**를 눌러야 결과를 확인할 수 있습니다. 이전 검색 결과는 저장되지 않습니다.
{% endhint %}

<figure><img src="../../../.gitbook/assets/스크린샷 2026-08-13 092933.png" alt=""><figcaption><p>&#x3C;검색 테스트></p></figcaption></figure>

### 검색 필터 태그

각 문서에 태그를 설정해 검색 결과를 필터링할 수 있습니다. 자세한 내용은 [태그 입력을 통한 검색 필터링](../undefined/knowledge-tag-setting.md)에서 확인합니다.

<figure><img src="../../../.gitbook/assets/image (867).png" alt=""><figcaption></figcaption></figure>

### 데이터 설정

지식의 기본 정보와 공유 설정을 변경합니다.

<figure><img src="../../../.gitbook/assets/스크린샷 2026-08-13 132555.png" alt=""><figcaption><p>&#x3C;지식 설정></p></figcaption></figure>

* **공유 설정**: 지식의 공유 여부를 설정합니다. [공유 · 발행 · 운영](../../undefined-4/)에서 공유 정책을 확인합니다.

### 크레딧 정책

크레딧은 AI가 답을 만들기 위해 실제로 수행한 작업량만큼 차감됩니다. 지식을 검색하고 문서를 읽어 결론을 도출하는 과정에서 여러 단계를 거치며, 단계마다 크레딧이 사용됩니다.

{% hint style="info" %}
참고할 지식이 많거나 질문이 복잡할수록 더 많은 크레딧이 사용됩니다.
{% endhint %}

#### 예시&#x20;

{% hint style="danger" %}
위에서 말했듯이 실제로 수행한 작업량이 세션마다 다를 수 있기에 해당 동작에 대한 크레딧이 꼭 맞는 것은 아닙니다.
{% endhint %}

**문서 10개 기준**

| 유형              | 크레딧       |
| --------------- | --------- |
| 지식 등록           | 0.18      |
| 지식 참조에 따른 결론 도출 | 1.18\~1.5 |

**문서 30개 기준**

| 유형              | 크레딧        |
| --------------- | ---------- |
| 지식 등록           |            |
| 지식 참조에 따른 결론 도출 | 1.50\~2.29 |
