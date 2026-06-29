---
description: MISO의 앱 만들기 메뉴에 대해서 소개합니다.
---

# 앱 만들기

MISO의 상단 메뉴 중 "앱 만들기"는 같은 조직 내에서 생성한 모든 앱을 확인할 수 있습니다.



<figure><img src="../../.gitbook/assets/image (326).png" alt="" width="375"><figcaption><p>&#x3C;앱 만들기 매뉴></p></figcaption></figure>



<figure><img src="../../.gitbook/assets/image (327).png" alt=""><figcaption><p>&#x3C;앱 만들기 → 새로 만들기></p></figcaption></figure>



## 앱 생성 <a href="#create-app" id="create-app"></a>

***

앱 생성 버튼은 MISO에 새로운 앱을 추가할 때 사용 하는 버튼으로 클릭 시, 생성할 앱 유형을 선택하는 화면으로 이동합니다.

MISO는 3가지 유형의 앱을 제공 합니다.

**에이전트**: 사용자가 원하는 동작을 간단한 프롬프트로 입력하고 도구를 지정하면, 에이전트가 자동으로 수행하는 챗봇 형태의 앱입니다.

{% include "../../.gitbook/includes/workflow-create-mode.md" %}



사용 할 앱 이름과 설명을 확인한 후, 생성을 진행하면 앱 만들기 화면에서 추가된 앱을 확인할 수 있습니다.







## 앱 가져오기 <a href="#app-import" id="app-import"></a>

***

MISO는 앱을 생성하면, .yml 형식의 파일로 앱을 제공합니다.(앱 내보내기 기능 활용)

앱  가져오기는.yml로 생성된 파일을 앱으로 등록하는 기능입니다.

{% hint style="info" %}
**YML 파일이란?**

YML 파일은 앱의 설정값이 들어 있는 파일입니다. 이 파일을 미소로 가져오면 예시 앱이 자동으로 생성됩니다.
{% endhint %}

다운받은 yml 앱 파일을 미소에 등록하는 방법은 아래와 같습니다.



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



<details>

<summary><span data-gb-custom-inline data-tag="emoji" data-code="1f916">🤖</span> <strong>[LLM 모델 선택 기준]</strong></summary>

| 모델 제공자 | 간단          | 기본               | 복잡   |
| ------ | ----------- | ---------------- | ---- |
| Claude | Haiku       | Sonnet           | Opus |
| GPT    | Nano / Mini | 표준 (ex. GPT-5.4) | Pro  |
| Gemini | Flash-Lite  | Flash            | Pro  |

{% hint style="info" %}
&#x20;모델 뒤의 숫자는 가장 높은 것이 가장 최신 것이므로, 가장 높은 숫자를 사용하시는 것을 권장합니다.
{% endhint %}



</details>



완료 시, 아래와 같이 앱이 생성됩니다.

<figure><img src="../../.gitbook/assets/image (696).png" alt=""><figcaption></figcaption></figure>
