---
description: 내보낸 .zip 웹사이트 설정 파일을 가져와 새 앱으로 등록합니다.
---

# 기존 앱 가져오기 - 웹사이트

MISO에서 내보낸 `.zip` 웹사이트 설정 파일을 가져와 새 앱으로 등록합니다.

{% hint style="info" %}
다른 회사, edu MISO, 다른 워크스페이스 등 **MISO에서 공유받은 앱**을 원하는 워크스페이스에 등록할 수 있습니다.
{% endhint %}

### 내보내기 후 다시 설정해야 하는 항목 확인하기

<table><thead><tr><th width="214.6666259765625">항목</th><th>이동 결과</th><th>옮긴 뒤 할 일</th></tr></thead><tbody><tr><td>앱 화면 구성, 설정값</td><td>⭕ 그대로 이동</td><td>없음</td></tr><tr><td>데이터베이스 표 구조</td><td>⭕ 그대로 이동</td><td>없음</td></tr><tr><td>연동된 앱, 지식, 도구</td><td>⚠️ 연결 대상 직접 지정 필요</td><td>가져오기 화면에서 현재 워크스페이스의 앱·지식·도구를 직접 선택</td></tr><tr><td>환경 변수</td><td>❌ 이동되지 않음</td><td>옮긴 워크스페이스에서 다시 입력</td></tr><tr><td>표에 저장된 데이터</td><td>❌ 이동되지 않음</td><td>필요한 데이터를 다시 입력</td></tr><tr><td>대화 중 첨부한 파일</td><td>❌ 이동되지 않음</td><td>원본 파일을 직접 보관 후 다시 첨부</td></tr></tbody></table>

### 기존 앱 가져오기

{% stepper %}
{% step %}
#### 앱 내보내기

기존 앱 메뉴에서 **앱 내보내기**를 통해 `.zip` 파일을 다운받습니다.

<figure><img src="../../.gitbook/assets/image (900).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (895).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
내보낸 파일을 재압축하거나 수정하면 가져올 수 없습니다.
{% endhint %}
{% endstep %}

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
#### ZIP 파일 선택하기

내려받은 `.zip` 파일을 선택한 뒤 엽니다.

<figure><img src="../../.gitbook/assets/스크린샷 2026-09-14 123644.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### 앱, 지식, 도구 재연결하기

기존 웹사이트에 연결한 앱, 지식, 도구는 자동으로 연결되지 않습니다. 현재 워크스페이스의 자원을 선택해 지식, 도구, 앱을 연결합니다.

<figure><img src="../../.gitbook/assets/image (896).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
앱을 이동하고 싶은 워크스페이스에 연동된 앱, 지식, 도구가 자동으로 생성되지 않습니다. 재연결을 위해 똑같은 형태로 이를 만들어서 연결해야합니다.
{% endhint %}
{% endstep %}

{% step %}
#### 확인하기

앱, 지식, 도구 연결 상황을 연동 관리 탭에서 확인합니다.

<figure><img src="../../.gitbook/assets/image (897).png" alt="" width="375"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### 이동되지 않는 데이터 입력하기

환경 변수, 표 데이터, 대화 중 첨부한 파일은 이동되지 않으므로 옮긴 앱에서 다시 설정합니다.
{% endstep %}
{% endstepper %}
