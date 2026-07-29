---
description: 채팅 입력창의 + 메뉴에서 연동, 요구사항, 환경 변수를 설정하는 방법을 안내합니다.
---

# 플러스(+) 버튼

### 연동 관리

메시지 입력창의 **+ → 연동 관리**를 선택하면 프로젝트 설정 창이 열립니다.

웹사이트에서 사용할 MISO 앱, 도구, 모델, 지식, MCP를 연결할 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (826).png" alt=""><figcaption></figcaption></figure>

#### 연동 항목

상단 필터에서 카테고리별 연동 항목을 확인할 수 있습니다.

<table><thead><tr><th width="81.40625">필터</th><th>설명</th></tr></thead><tbody><tr><td><strong>전체</strong></td><td>모든 연동 항목을 표시합니다.</td></tr><tr><td><strong>앱</strong></td><td>챗플로우, 워크플로우, 에이전트 등 다른 MISO 앱을 연결합니다.</td></tr><tr><td><strong>도구</strong></td><td>API 도구와 빌트인 도구를 연결합니다.</td></tr><tr><td><strong>모델</strong></td><td>OpenAI, Claude 등 LLM 모델을 연결합니다.</td></tr><tr><td><strong>지식</strong></td><td>데이터셋을 연결해 지식 검색 결과를 웹사이트에서 활용합니다.</td></tr><tr><td><strong>MCP</strong></td><td>MCP(Model Context Protocol) 연동을 설정합니다.</td></tr></tbody></table>

지식을 연결하면 전용 API 토큰이 자동 발급됩니다. API 접근을 활성화할 권한이 있는 지식 편집자 이상이 필요합니다.

#### 연동 추가와 제거

1. 검색하거나 필터를 선택해 항목을 찾습니다.
2. 항목을 선택해 연동을 추가합니다.
3. 다시 선택하거나 ✕를 선택해 연동을 제거합니다.

연동한 항목은 채팅 입력창 위의 스트립에 표시됩니다. AI에 해당 앱이나 도구 사용을 요청하세요.

{% hint style="info" %}
연동 항목은 제공업체별로 그룹화됩니다. 섹션 헤더를 선택해 접거나 펼칠 수 있습니다.
{% endhint %}

### 요구사항

메시지 입력창의 **+ → 요구사항**을 선택하면 프로젝트 설정 창이 열립니다.

웹사이트의 기능 요구사항과 디자인 가이드라인을 문서로 관리할 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (824).png" alt=""><figcaption></figcaption></figure>

#### 문서 유형

<table><thead><tr><th width="127.23046875">탭</th><th width="355.953125">설명</th></tr></thead><tbody><tr><td><strong>제품 요구사항</strong></td><td>제품의 기능과 요구사항을 정의합니다.</td></tr><tr><td><strong>디자인</strong></td><td>시각 디자인 및 인터랙션 가이드라인을 설명합니다.</td></tr></tbody></table>

#### 사용 방법

1. **+ 추가**를 선택해 문서를 만듭니다.
2. 파일명과 내용을 입력한 뒤 **저장**을 선택합니다.
3. AI는 저장한 문서를 웹사이트 제작 시 참고합니다.

{% hint style="info" %}
복잡한 프로젝트는 요구사항을 미리 정의하세요. AI가 대화 맥락을 더 정확히 이해합니다.
{% endhint %}

### 환경 변수

메시지 입력창의 **+ → 환경 변수**를 선택하면 프로젝트 설정 창이 열립니다.

웹사이트에서 사용하는 API 키와 시크릿을 안전하게 관리할 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (827).png" alt=""><figcaption></figcaption></figure>

#### 사용 방법

1. **+ 행 추가**를 선택합니다.
2. **Key**와 **Value**를 입력합니다.
3. 민감한 값은 **Is Secret**을 활성화합니다.
4. **저장**을 선택합니다.

{% hint style="info" %}
변수명에 `KEY`, `SECRET`, `TOKEN`, `PASSWORD`, `CREDENTIAL`, `AUTH`가 포함되면 자동으로 시크릿으로 설정됩니다.

환경 변수를 저장하면 개발 서버가 자동으로 다시 시작됩니다.
{% endhint %}
