---
description: 완성한 웹사이트를 실제 URL로 배포하고 보안 점검·버전을 관리하는 방법을 안내합니다.
---

# 웹사이트 발행하기

웹사이트 제작이 끝나면 화면 오른쪽 위의 **발행하기**를 선택해 라이브 URL로 배포합니다.

<div align="center"><figure><img src="../../../.gitbook/assets/image (764).png" alt="" width="370"><figcaption></figcaption></figure></div>

{% hint style="warning" %}
발행한 웹사이트는 운영 기간 동안 하루 30크레딧이 차감됩니다.

발행 당일 철회해도 해당 일자의 크레딧은 차감됩니다.
{% endhint %}

### 발행 절차

1. **발행하기**를 선택합니다.
2. 필요하면 발행 사유를 입력합니다.
3. **발행 승인 요청**을 선택합니다.
4. 배포가 끝나면 라이브 URL을 복사해 공유합니다.

새 버전이 필요하면 최신 작업 버전으로 발행을 요청합니다. 운영을 중단하려면 발행 철회를 요청합니다.

<img src="../../../.gitbook/assets/image (765).png" alt="" data-size="original">

### 코드 보안 점검

발행을 요청하면 생성한 코드에 자동 보안 점검이 실행됩니다.

잠재적 취약점과 경고는 발행 단계에서 표시됩니다. 발행 팝업의 **돋보기**에서 세부 내용을 확인할 수 있습니다.

<div align="left"><figure><img src="../../../.gitbook/assets/image (766).png" alt="" width="373"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (767).png" alt="" width="375"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="157.1328125">점검 작업</th><th width="127.3359375">라이브러리</th><th>점검 항목 및 의도</th></tr></thead><tbody><tr><td><strong>코드 안전성 점검</strong></td><td>Opengrep</td><td>만들어진 웹사이트 코드에 <strong>위험한 동작</strong>(허가되지 않은 명령 실행, 검증 없이 외부 내용을 화면에 띄우기, 외부로 데이터를 몰래 보내기 등)이 들어 있는지 확인합니다. → 사이트 <strong>방문자가 악성 코드에 노출되거나 정보가 새는 것</strong>을 막기 위함.</td></tr><tr><td><strong>비밀정보 노출 점검</strong></td><td>Gitleaks</td><td>API 키·비밀번호·토큰처럼 <strong>외부에 알려지면 안 되는 정보</strong>가 코드에 그대로 들어가 있는지 확인합니다. → 노출된 키가 <strong>도용·오용되는 것</strong>을 막기 위함.</td></tr><tr><td><strong>취약 라이브러리 점검</strong></td><td>OSV Scanner</td><td>사이트가 가져다 쓰는 <strong>외부 부품(라이브러리)</strong> 중 <strong>보안 결함이 알려진 버전</strong>이 섞여 있는지 확인합니다. → 이미 공개된 취약점을 통한 <strong>공격을 예방</strong>하기 위함.</td></tr></tbody></table>

#### 취약점이 발견되면

1. 검출 항목에서 위치와 권장 조치를 확인합니다.
2. AI에 수정을 요청하거나 **Code** 탭에서 직접 수정합니다.
3. 새 버전을 발행하면 변경된 코드로 다시 점검합니다.

{% hint style="info" %}
보안 점검 결과는 발행 요청을 차단하지 않습니다. 결과는 참고 정보로 제공됩니다.
{% endhint %}

### 발행 진행 상태

배포는 다음 단계를 거쳐 진행됩니다.

<table><thead><tr><th width="129.5390625">단계</th><th width="248.421875">설명</th></tr></thead><tbody><tr><td><strong>Preparing</strong></td><td>배포를 준비합니다.</td></tr><tr><td><strong>Installing</strong></td><td>의존성 패키지를 설치합니다.</td></tr><tr><td><strong>Building</strong></td><td>웹사이트를 빌드합니다.</td></tr><tr><td><strong>Finalizing</strong></td><td>배포를 마무리합니다.</td></tr></tbody></table>

{% hint style="info" %}
이미 발행한 웹사이트는 수정 후 **새 버전 배포**를 선택하세요. 변경 사항이 라이브 URL에 반영됩니다.
{% endhint %}

### 발행 상태

발행 팝업은 현재 상태에 따라 다른 화면과 작업을 표시합니다.

<table><thead><tr><th width="172.4453125">상태</th><th>설명</th></tr></thead><tbody><tr><td><strong>최초 발행</strong></td><td>아직 발행되지 않은 상태입니다. 접근 권한을 설정하고 배포를 시작합니다.</td></tr><tr><td><strong>승인 대기</strong></td><td>승인이 필요한 공개 범위로 요청되어 관리자 승인을 기다리는 상태입니다.</td></tr><tr><td><strong>승인 완료(배포 대기)</strong></td><td>승인이 완료되어 발행만 하면 되는 상태입니다.</td></tr><tr><td><strong>운영 중</strong></td><td>라이브 URL이 활성화된 상태입니다. 새 버전 발행 또는 철회를 요청할 수 있습니다.</td></tr><tr><td><strong>일시 정지</strong></td><td>발행이 일시 정지된 상태입니다.</td></tr><tr><td><strong>철회 대기</strong></td><td>발행 철회를 요청하여 처리를 기다리는 상태입니다.</td></tr></tbody></table>

### 접근 권한

웹사이트의 공유 범위와 사용자, 편집자 권한을 설정할 수 있습니다.

[앱 공유하기](../share/undefined.md)에서 권한별 기능을 확인하세요.

<table><thead><tr><th width="184.921875">권한</th><th width="342.39453125">설명</th></tr></thead><tbody><tr><td><strong>비공개</strong></td><td>본인만 접근할 수 있습니다.</td></tr><tr><td><strong>현재 워크스페이스 공개</strong></td><td>현재 워크스페이스의 멤버만 접근할 수 있습니다.</td></tr><tr><td><strong>모든 워크스페이스 공개</strong></td><td>모든 워크스페이스의 멤버가 접근할 수 있습니다.</td></tr><tr><td><strong>외부 공개</strong></td><td>누구나 URL을 통해 접근할 수 있습니다.</td></tr><tr><td><strong>부분 공개</strong></td><td>지정한 멤버만 접근할 수 있습니다.</td></tr></tbody></table>

{% hint style="warning" %}
**모든 워크스페이스 공개**, **외부 공개**, **부분 공개**는 승인 요청이 필요합니다.

공유 범위를 설정하고 **저장**하면 관리자에게 승인 요청이 전달됩니다. 승인 전에는 이전 공유 범위가 유지됩니다.
{% endhint %}

### 발행 철회

운영 중인 웹사이트를 비공개 상태로 되돌릴 수 있습니다.

1. 발행 팝업에서 **발행 철회 요청**을 선택합니다.
2. 안내 문구와 철회 사유를 입력합니다.
3. 요청이 처리되면 라이브 URL 접근이 중단됩니다.

{% hint style="info" %}
관리자가 워크스페이스의 발행 승인을 면제하면 승인 대기 없이 바로 배포됩니다.
{% endhint %}
