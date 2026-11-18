---
description: Google Sheets API를 활성화하고 Google Sheet 도구를 활성화하는 방법을 설명합니다.
---

# \[참고] Google Sheet 도구 키 발급 및 설정하기

### STEP 1. Google Sheets API 활성화

1. **GCP 사이트에 접속:**

* Google Cloud Console([https://console.cloud.google.com](https://console.cloud.google.com/))에 접속 후 로그인합니다.
  * **52g.team 과 같은 회사 계정은 계정 생성이 차단될 수 있습니다.**
* 기존 프로젝트를 선택하거나 새 프로젝트를 생성합니다.

<figure><img src="https://3745052963-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2F4miUlVESpd0km7u4ir5m%2Fimage.png?alt=media&#x26;token=13bdfc3f-6173-46b9-be05-e210b57e3cf1" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="https://3745052963-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FJkyjSbIoZzzRHHgBR7oc%2Fimage.png?alt=media&#x26;token=61c16d23-6cb6-42c6-a7e5-3d2a280a5790" alt="" width="486"><figcaption></figcaption></figure>

2. **API 활성화:**

* 좌측 메뉴에서 **API 및 서비스 > 라이브러리**로 이동합니다.

<figure><img src="https://3745052963-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FxHoyiMtYUn5hfLLrN5T1%2Fimage.png?alt=media&#x26;token=335d0d42-548a-4904-9f3e-7d7481c8931e" alt="" width="563"><figcaption></figcaption></figure>

* 검색창에 "Google Sheets API"를 입력하고 **사용 설정**을 클릭합니다.

<figure><img src="https://3745052963-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FQEWF3IkL2BFp8m7bKOL2%2Fimage.png?alt=media&#x26;token=837d4aaa-8bac-410a-9bb9-d5c20b1e2d7c" alt="" width="227"><figcaption></figcaption></figure>

### STEP 2. 서비스 계정 생성

1.  **서비스 계정 메뉴로 이동:**

    * 좌측 메뉴에서 **IAM 및 관리자 > 서비스 계정**으로 이동합니다.

    <figure><img src="https://3745052963-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FFkHYH46TwOhFxV2reQEu%2Fimage.png?alt=media&#x26;token=ab6f823f-eb00-4400-ae0d-4a95306ddc13" alt="" width="375"><figcaption></figcaption></figure>
2.  **서비스 계정 생성:**

    * **서비스 계정 만들기**를 클릭하고 서비스 계정 이름을 입력하여 생성합니다.

    <figure><img src="https://3745052963-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FEzfF5ZiP6Y3X0R11GLyt%2Fimage.png?alt=media&#x26;token=4dbadfce-81c5-41e0-88ce-0186dc059a12" alt="" width="327"><figcaption></figcaption></figure>

### STEP 3. JSON 키 발급

1.  **키 생성:**

    * 생성된 서비스 계정을 클릭한 후 **키** **관리**으로 이동합니다.
    * 아래 사진의 이메일 부분은 추후 이 도구를 사용하는 사용자에게 필요한 정보입니다. 복사 후 공지하기 바랍니다.

    <figure><img src="https://3745052963-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2F4eGvbSXsbLZazfXJtQy2%2Fimage.png?alt=media&#x26;token=683f2c36-5a4b-4bdc-8967-88cf32c8aa80" alt=""><figcaption></figcaption></figure>

    * **키 추가 > 새 키 만들기**를 선택하고 **JSON** 형식을 선택합니다.

    <figure><img src="https://3745052963-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FdRborZZOe0YlxSboWwxf%2Fimage.png?alt=media&#x26;token=d8c60c6c-3e67-4803-95a3-c1ca8965379a" alt="" width="563"><figcaption></figcaption></figure>
2. **JSON 파일:**
   * JSON 파일이 자동으로 다운로드되며, 이 파일이 API 인증에 필요한 **서비스 계정 키**입니다.
   * 해당 JSON 파일을 열어서 복사합니다. (안열리는 경우 텍스트 파일(메모장)으로 열기)

### STEP 4. MISO 도구 등록

1.  MISO 플레이그라운드 왼쪽 메뉴의 **도구**에서 **Google Sheets**를 검색한 뒤, **GCP Service Account JSON Key** 칸에 복사한 JSON 키를 붙여넣고 **저장**을 클릭합니다.

    <figure><img src="../../../.gitbook/assets/GS_key_v2.webp" alt=""><figcaption></figcaption></figure>
2. 활성화 상태를 확인합니다.

{% hint style="warning" %}
### '사용자 권한이 부족합니다. 관리자에게 문의해주세요.' 오류가 발생해요.

MISO에서 도구 등록은 해당 워크스페이스의 관리자 권한을 가진 사용자만 가능합니다.

도구 등록이 필요한 경우, 워크스페이스 관리자에게 문의하여 등록을 요청해 주세요.
{% endhint %}
