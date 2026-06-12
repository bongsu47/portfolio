---
icon: linux
---

# \[1] 기본앱 세팅

기본앱 세팅은 다음의 2가지 목적을 가지고 있습니다.

1. **전사 관점에서 미소에 쉽게 온보딩**
   * 기본 앱을 통해 “어떤 앱들을 만들어서 어떤 문제들을 해결/자동화 할 수 있는지” 예시를 보여드리고자 합니다.
2. **MISO 앱 활용에 대한 튜토리얼**
   * 앱을 만들 수 있는 2가지 방법, 1) 워크플로우, 2) 에이전트 제작 예시를 설명합니다.
   * MISO에서 제공하는 `도구`를 활용하는 방법과, 자체 보유 데이터를 MISO에 `지식`으로 등록해 활용하는 예시를 다루며, MISO를 활용하는 다양한 방식을 안내하고자 합니다.

{% hint style="info" %}
학습하기 매뉴얼 만으로는 MISO의 활용 흐름을 체감하기 어려운 부분이 있어, 실제 동작하는 앱을 통해 활용 시나리오를 직접 경험해보실 수 있도록 기본앱을 세팅합니다.
{% endhint %}

***

### 1단계: 앱 등록하기

{% hint style="info" %}
MISO에서 _이미 만들어놓은_ 예시 앱을 등록해 봅니다.

* [ ] &#x20;← 1단계에서 앱 4개를 모두 MISO에 등록한 뒤, 2단계로 넘어가시는 것을 권장합니다.
{% endhint %}

**\[준비물]**

* 기본으로 제공하는 앱들의 `yml` 파일과 `첨부 파일`을 다운로드 합니다.

<table><thead><tr><th>앱 이름</th><th data-type="files">yml 파일</th><th data-type="files">첨부 파일</th></tr></thead><tbody><tr><td>법령 검색 에이전트</td><td><a href="../../.gitbook/assets/[템플릿] 법령 검색 에이전트.yml">[템플릿] 법령 검색 에이전트.yml</a></td><td></td></tr><tr><td>사내 규정 에이전트</td><td><a href="../../.gitbook/assets/[템플릿] 사내 규정 에이전트.yml">[템플릿] 사내 규정 에이전트.yml</a></td><td><a href="../../.gitbook/assets/[템플릿] GS 사내규정집.csv">[템플릿] GS 사내규정집.csv</a></td></tr><tr><td>뉴스 스크래핑 워크플로우</td><td><a href="../../.gitbook/assets/[템플릿]뉴스 스크래핑 워크플로우 (반복노드 버전).yml">[템플릿]뉴스 스크래핑 워크플로우 (반복노드 버전).yml</a></td><td></td></tr><tr><td>PDF 요약 분석</td><td><a href="../../.gitbook/assets/[템플릿] PDF 요약 분석.yml">[템플릿] PDF 요약 분석.yml</a></td><td><a href="../../.gitbook/assets/[템플릿] 산업보건법.pdf">[템플릿] 산업보건법.pdf</a></td></tr></tbody></table>

다운받은 yml 앱 파일을 MISO에 등록하는 방법은 아래와 같습니다.



1.  **미소 메인 → \[플레이그라운드 - 앱 리스트] 클릭**

    <figure><img src="../../.gitbook/assets/image (693).png" alt=""><figcaption></figcaption></figure>


2.  **워크스페이스 선택 → 앱 만들기 → 기존 앱 가져오기 클릭**

    <figure><img src="../../.gitbook/assets/image (691).png" alt=""><figcaption></figcaption></figure>

    * 우상단에서 워크스페이스 선택
    * 앱 만들기 → 기존 앱 가져오기 클릭


3.  **다운받은 `yml` 파일 선택 → 열기**

    <figure><img src="../../.gitbook/assets/image (694).png" alt=""><figcaption></figcaption></figure>


4.  **(선택) LLM 모델 선택하기**<br>

    <figure><img src="../../.gitbook/assets/image (695).png" alt=""><figcaption></figcaption></figure>



    회사별로 사용하는 LLM 모델이 상이하기에, 기본 옵션으로 설정해놓은 모델이 없을 수 있습니다.

    이에 각 회사에서 사용하는 모델에 맞게 선택해주시면 됩니다.



:robot: **\[LLM 모델 선택 기준]**

| 모델 제공자 | 간단          | 기본               | 복잡   |
| ------ | ----------- | ---------------- | ---- |
| Claude | Haiku       | Sonnet           | Opus |
| GPT    | Nano / Mini | 표준 (ex. GPT-5.4) | Pro  |
| Gemini | Flash-Lite  | Flash            | Pro  |

\*\* 모델 뒤의 숫자는 가장 높은 것이 가장 최신 것이므로, 가장 높은 숫자를 사용하시는 것을 권장합니다.



완료 시, 아래와 같이 앱이 생성됩니다.

<figure><img src="../../.gitbook/assets/image (696).png" alt=""><figcaption></figcaption></figure>



{% hint style="warning" %}
**\[유의사항]**

* 현 상태는 아직 `발행되지 않은 앱`, 즉 **개인 계정**에서만 사용 가능한 앱 상태입니다. \
  조직 전체에서 활용하기 위한 방법은 **3단계:** [앱 공유 범위 설정](https://app.notion.com/p/c98f800bd1c18273a3d7016c22948e9e?pvs=21) 에서 진행합니다!
* 다운받은 첨부 파일은 **2단계**, 각 앱에 대한 상세 설명에서 적용하도록 하겠습니다.
{% endhint %}



1. 현 상태는 아직 `발행되지 않은 앱`, 즉 **개인 계정**에서만 사용 가능한 앱 상태입니다. \
   조직 전체에서 활용하기 위한 방법은 **3단계:** [앱 공유 범위 설정](./#id-3-admin) 에서 진행합니다!
2. 다운받은 첨부 파일은 다음 섹션, 각 앱에 대한 상세 설명에서 적용하도록 하겠습니다.

***

### 2단계: 앱 살펴보기

<table><thead><tr><th width="160.9921875" data-type="content-ref">앱 이름</th><th width="192.82421875">키워드<select multiple><option value="emfjYG0GPS6m" label="에이전트" color="blue"></option><option value="gmn0PgPJCsbX" label="도구" color="blue"></option><option value="05zPhlpZtZk9" label="지식 등록" color="blue"></option><option value="HFTudXsOPFzI" label="워크플로우" color="blue"></option><option value="FuntPdsLR9sw" label="파일 업로드" color="blue"></option></select></th><th>특징</th></tr></thead><tbody><tr><td><a href="undefined.md">undefined.md</a></td><td><span data-option="emfjYG0GPS6m">에이전트, </span><span data-option="gmn0PgPJCsbX">도구</span></td><td>1단계: 에이전트로 앱을 생성하는 방법을 익힙니다.<br>2단계: 도구를 활용하는 법을 익힙니다.</td></tr><tr><td><a href="undefined-1.md">undefined-1.md</a></td><td><span data-option="emfjYG0GPS6m">에이전트, </span><span data-option="05zPhlpZtZk9">지식 등록</span></td><td>3단계: MISO에 지식을 등록하고 활용하는 법을 익힙니다.</td></tr><tr><td><a href="undefined-2.md">undefined-2.md</a></td><td><span data-option="HFTudXsOPFzI">워크플로우, </span><span data-option="gmn0PgPJCsbX">도구</span></td><td>4단계: 워크플로우로 앱을 생성하는 방법을 익힙니다.</td></tr><tr><td><a href="pdf.md">pdf.md</a></td><td><span data-option="HFTudXsOPFzI">워크플로우, </span><span data-option="FuntPdsLR9sw">파일 업로드</span></td><td>5단계: 파일을 직접 업로드하여 활용하는 방법을 익힙니다.</td></tr></tbody></table>

***

### 3단계: 앱 공유 범위 설정 (Admin)

{% hint style="info" %}
해당 단계에서는 앱 공유 범위 설정이 진행되기 때문에, **MISO Admin 계정**이 필요합니다.
{% endhint %}

> 쇼케이스에 내가 만든 앱을 등록하기 위해서는 앱의 `공유 범위`를 **전체 워크스페이스**로 변경해야 합니다.



1. **앱 발행하기**

우선 개인이 만든 앱을 모두가 볼 수 있도록 `발행` 작업을 진행합니다.

발행할 앱을 클릭해서 들어갑니다.

<figure><img src="../../.gitbook/assets/image (697).png" alt=""><figcaption></figcaption></figure>

우상단에서 `저장하기` 를 누른 뒤 → `발행하기` 를 클릭합니다.

<div align="left"><figure><img src="../../.gitbook/assets/image (698).png" alt="" width="375"><figcaption></figcaption></figure></div>

버전명과 수정사항을 입력하고 (기본 값 그대로 사용하셔도 무방합니다.)

`발행하기` 버튼을 눌러줍니다.



2. **앱 배포하기 (개인 앱 리스트 → 조직 앱 리스트)**

이후 관리자에게 앱을 전체 공개 할 수 있도록 요청을 보냅니다.

<figure><img src="../../.gitbook/assets/image (699).png" alt=""><figcaption></figcaption></figure>

우상단 구역에서 `공유` 를 찾은 뒤 클릭합니다.

<figure><img src="../../.gitbook/assets/image (700).png" alt=""><figcaption></figcaption></figure>

**공유 설정** 탭에서 모든 `워크스페이스 공개` 를 선택합니다.

그리고 `저장`을 누르면 아래와 같은 화면이 나옵니다.

<div><figure><img src="../../.gitbook/assets/image (701).png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/image (702).png" alt=""><figcaption></figcaption></figure></div>

모두 `확인`을 눌러주신 후 `승인 요청`을 보냅니다.



{% hint style="danger" %}
**여기서부터는 Admin 계정에서 진행합니다.**
{% endhint %}

3. **승인 요청**

Admin 계정에서 방금 승인 요청한 앱을 조직에서 모두 활용 가능하도록 설정해줍니다.

우선 Admin 계정으로 접속합니다.

이후, 아래와 같이 \[자산 - 승인 요청] 탭에 들어가 주면,

방금 공유를 시도한 앱이 권한 요청 목록에 표시됩니다.

<figure><img src="../../.gitbook/assets/image (703).png" alt=""><figcaption></figcaption></figure>

<div align="left"><figure><img src="../../.gitbook/assets/image (704).png" alt="" width="375"><figcaption></figcaption></figure></div>

해당 앱을 클릭하신 뒤, 모두 확인을 눌러주고, 승인해줍니다.
