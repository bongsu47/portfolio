---
description: Browser, Web Server, Application Server 로그의 역할과 확인 순서를 안내합니다.
---

# 로그

웹 서비스는 동작 과정과 오류 정보를 **로그**로 기록합니다. 문제가 발생하면 로그를 먼저 확인해 원인을 파악하세요.

### 로그 한눈에 보기

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

로그 화면은 **Browser**, **Web Server**, **Application Server** 탭으로 구성됩니다.

<table><thead><tr><th width="242.333251953125">구간</th><th>역할</th></tr></thead><tbody><tr><td>Browser</td><td>사용자가 보고 조작하는 화면의 동작을 기록합니다.</td></tr><tr><td>Web Server</td><td>요청을 받고 응답을 전달하는 과정을 기록합니다.</td></tr><tr><td>Application Server</td><td>요청을 처리하고 데이터를 조회하는 과정을 기록합니다.</td></tr></tbody></table>

#### 증상으로 로그 선택하기

| 증상                         | 확인할 로그             | MISO로 수정   |
| -------------------------- | ------------------ | ---------- |
| 화면이 열리지 않거나 버튼이 반응하지 않습니다. | Browser            | ✅ 가능       |
| 일부 사용자에게만 문제가 발생합니다.       | Browser            | ✅ 가능       |
| 접속할 수 없거나 페이지가 매우 느립니다.    | Web Server         | ❌ 담당자에게 문의 |
| 화면은 정상이나 결과가 예상과 다릅니다.     | Application Server | ❌ 담당자에게 문의 |
| 화면에 오류 메시지가 표시됩니다.         | Application Server | ❌ 담당자에게 문의 |

{% hint style="info" %}
오류가 발생하면 Web Server 로그의 상태 코드를 먼저 확인하세요. 화면이 비어 있으면 Browser 로그를 확인하세요. 상태 코드가 `500`이면 Application Server 로그를 확인하세요.
{% endhint %}

### MISO로 수정하기

{% stepper %}
{% step %}
### 오류 확인

오류가 발생하면 미리보기 화면 하단에 오류 요약이 표시됩니다.

<figure><img src="../../../.gitbook/assets/스크린샷 2026-09-15 134617 (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### 오류 열기

오류를 클릭하면 로그가 열립니다. 오류 위치로 이동하며 해당 항목이 강조됩니다.

<figure><img src="../../../.gitbook/assets/스크린샷 2026-09-15 134647.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### MISO로 수정 요청

**MISO로 수정하기**를 클릭하세요. 선택한 로그가 채팅 패널의 AI에 전달됩니다.

<figure><img src="../../../.gitbook/assets/스크린샷 2026-09-15 134853.png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

{% hint style="info" %}
MISO로 수정하기는 모든 오류를 한 번에 해결하기보다, 오류 로그를 바탕으로 원인을 확인하고 수정을 시도합니다. \
문제를 해결하려면 먼저 원인을 찾는 과정이 필요합니다. 이 기능과 함께 원인을 살펴보고 해결해보세요.
{% endhint %}
