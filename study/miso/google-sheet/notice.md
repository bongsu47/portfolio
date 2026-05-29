# \[필수] Google Sheet 도구 사전준비

미소에서는 **워크스페이스 내에서 같은 도구의 연동 정보를 함께 공유**합니다. 예를 들어 관리자가 Google Sheets 도구를 활성화했다면, 해당 도구에 연결된 **계정 정보와 접근 권한이 설정되어 있어야 다른 사용자도 동일한 도구를 사용할 수 있습니다.** 즉, 개인이 따로 계정을 연결하는 방식이 아니라 **워크스페이스 차원에서 하나의 연동을 공유하는 구조**입니다.

또한 회사의 보안 정책에 따라 **외부 서비스 연동이 제한된 환경에서는 Google Sheets 도구 사용이 불가능한 경우도 있습니다.** 실습을 진행하기 전에 이러한 환경 제약이 있을 수 있다는 점도 참고해 주세요.

이제 실습을 위해 **Google Sheets를 설정하고, 필요한 정보를 미리 확인하는 과정**을 차근차근 진행해 보겠습니다.

***

### STEP 1. Google Sheet 도구 활성화 확인하기

1. 플레이그라운드 - 도구모음 - Google Sheet 항목이 활성화 상태인지 확인합니다.

<figure><img src="../../../.gitbook/assets/image (514).png" alt="" width="563"><figcaption></figcaption></figure>

2-1. 활성화 상태라면 해당 워크스페이스 관리자에게 등록된 키에 포함된 `client_email(서비스계정)` 을 요청합니다.

* 관리자라면 사전에 계정 생성 및 사용 방법을 공지하는 것이 좋습니다. 이 메뉴얼을 참고하시기 바랍니다.

2-2. 만약 비활성화 상태이고 도구를 직접 등록할 수 있다면, 아래 문서를 통해 키를 발급해주세요.

{% content-ref url="setting.md" %}
[setting.md](setting.md)
{% endcontent-ref %}

***

### STEP 2. Google Sheet 서비스 계정 확인하기

미소에 등록한 Google Sheet 키(JSON 파일)에서 `client_email` 항목에 있는 이메일 주소를 복사합니다.

{% hint style="info" %}
#### 서비스 계정이란?

MISO에서 도구를 통해 내 시트에 접근하기 위해 사용하는 전용 이메일 계정을 ‘Service 계정’이라고 합니다.

**Service 계정은 사람이 사용하는 계정이 아니라, MISO가 자동으로 시트에 접근해 데이터를 읽거나 추가하기 위한 자동화용 계정(로봇 계정)입니다.**

따라서 Google Sheet에서 다른 사용자에게 문서를 공유하듯이, Service 계정 이메일을 시트에 추가하고 ‘편집자’ 권한을 부여해야 합니다. 이렇게 권한을 부여하면 MISO가 해당 시트에 접근하여 데이터를 읽거나 새로운 데이터를 추가할 수 있습니다.

Service 계정 이메일은 Google Sheet 도구를 등록할 때 사용한 **키 파일(JSON)**&#xC5D0;서 확인할 수 있습니다.\
아래 예시처럼 **`client_email` 항목에 있는 이메일 주소가 바로 Service 계정 이메일**입니다.<br>

{% code fullWidth="false" %}
```
{
  "type": "service_account",
  "project_id": "***",
  "private_key_id": "***",
  "private_key": "-----BEGIN PRIVATE KEY-----\n***\n-----END PRIVATE KEY-----",
  "client_email": "miso-2025@***.iam.gserviceaccount.com",  
  "client_id": "***",
  "auth_uri": "https://accounts.google.com/o/oauth2/auth",
  "token_uri": "https://oauth2.googleapis.com/token",
  "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
  "client_x509_cert_url": "https://www.googleapis.com/robot/v1/metadata/x509/***",
  "universe_domain": "googleapis.com"
}
```
{% endcode %}
{% endhint %}

***

### STEP 3. 실습용 Google Sheet 설정하기

1. [실습용 Google Sheet 주소 (클릭)](https://docs.google.com/spreadsheets/d/1_Bc7DcA4VD4uoN29w8AU2x4rRWJbZ8vZSMRPYFGN0kQ/edit?usp=sharing) 에 접속합니다.
2. 좌측 상단의 파일 - 사본 만들기를 클릭하여 시트를 복사합니다.

<figure><img src="../../../.gitbook/assets/Clipboard-20260309-033351-884.gif" alt="" width="563"><figcaption></figcaption></figure>

3. 공유를 클릭하여 STEP 2에서 복사한 `client_email(서비스계정)` 에게 편집자 권한을 부여합니다.

<figure><img src="../../../.gitbook/assets/Clipboard-20260309-034404-684.gif" alt="" width="563"><figcaption></figcaption></figure>

3. 공유 버튼을 다시 클릭하여 권한 부여가 정상적으로 되었는지 확인합니다.

<figure><img src="../../../.gitbook/assets/image (509).png" alt="" width="375"><figcaption></figcaption></figure>



여기까지 설정이 완료되었다면, 미소에서 Google Sheets를 활용하기 위한 모든 준비가 끝났습니다.

이제 실제 도구에서 어떻게 활용하는지 예제를 통해 하나씩 살펴보겠습니다.
