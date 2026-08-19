---
description: 다른 곳에서 내보낸 .yml 앱 설정 파일을 불러와 앱으로 등록합니다.
---

# 기존 앱 가져오기

MISO에서 내보낸 `.yml` 앱 설정 파일을 가져와 새 앱으로 등록합니다.

{% hint style="info" %}
#### YML 파일이란?

YML 파일에는 앱 설정값이 포함됩니다. 파일을 MISO로 가져오면 앱이 생성됩니다.
{% endhint %}

### 기존 앱 가져오기

{% stepper %}
{% step %}
#### 앱 리스트 열기

MISO 메인에서 **플레이그라운드 → 앱 리스트**를 선택합니다.
{% endstep %}

{% step %}
#### 가져오기 메뉴 열기

**앱 만들기 → 기존 앱 가져오기**를 선택합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2026-07-28 163510.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### YML 파일 선택하기

내려받은 `.yml` 파일을 선택한 뒤 엽니다.

<figure><img src="../../.gitbook/assets/스크린샷 2026-07-28 163836.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### LLM 모델 선택하기

기본 모델이 설정되지 않은 경우 조직에서 사용하는 LLM 모델을 선택합니다.

<figure><img src="../../.gitbook/assets/image (695).png" alt=""><figcaption></figcaption></figure>

<details>

<summary><span data-gb-custom-inline data-tag="emoji" data-code="1f916">🤖</span> <strong>[LLM 모델 선택 기준]</strong></summary>

* **Claude:** 간단한 작업에는 Haiku, 기본 작업에는 Sonnet, 복잡한 작업에는 Opus를 선택합니다.
* **GPT:** 간단한 작업에는 Nano 또는 Mini, 기본 작업에는 표준 모델(예: GPT-5.4), 복잡한 작업에는 Pro를 선택합니다.
* **Gemini:** 간단한 작업에는 Flash-Lite, 기본 작업에는 Flash, 복잡한 작업에는 Pro를 선택합니다.

{% hint style="info" %}
모델 이름 뒤의 숫자가 높을수록 최신 버전입니다. 가장 높은 숫자의 모델 사용을 권장합니다.
{% endhint %}

</details>
{% endstep %}
{% endstepper %}

### 가져오기 완료

가져오기가 완료되면 앱이 생성됩니다.

<figure><img src="../../.gitbook/assets/스크린샷 2026-07-28 164132.png" alt=""><figcaption></figcaption></figure>
