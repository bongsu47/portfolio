---
description: 웹사이트 에디터의 화면 구성과 제작, 발행, 운영 흐름을 안내합니다.
---

# 웹사이트 이해하기

### 에디터 화면 구성

웹사이트 에디터는 **채팅 패널**과 **메인 워크벤치**로 구성됩니다.

<figure><img src="../../.gitbook/assets/image (755).png" alt=""><figcaption></figcaption></figure>

#### 채팅 패널

왼쪽 패널에서 AI와 대화하며 웹사이트를 제작합니다.

상단에는 앱 이름과 뒤로 가기 버튼이 있습니다. 중앙에는 대화 기록이 표시됩니다.

메시지 입력창의 **+**&#xB97C; 선택하면 추가 기능을 사용할 수 있습니다.

<table><thead><tr><th width="124.57421875">메뉴</th><th width="422.515625">설명</th></tr></thead><tbody><tr><td><strong>파일 첨부</strong></td><td>참고 이미지나 문서를 첨부합니다.</td></tr><tr><td><strong>연동 관리</strong></td><td>MISO 앱, 도구, 모델, 지식, MCP를 연결합니다.</td></tr><tr><td><strong>요구사항</strong></td><td>제품 요구사항 및 디자인 가이드라인을 정의합니다.</td></tr><tr><td><strong>환경 변수</strong></td><td>API 키 등 환경변수를 설정합니다.</td></tr></tbody></table>

#### 메인 워크벤치

<table><thead><tr><th width="124.12109375">탭</th><th width="414.71484375">설명</th></tr></thead><tbody><tr><td><strong>Preview</strong></td><td>제작 중인 웹사이트의 실시간 미리보기를 확인합니다.</td></tr><tr><td><strong>Code</strong></td><td>파일 트리와 코드 에디터를 통해 소스코드를 직접 편집합니다.</td></tr><tr><td><strong>Database</strong></td><td>데이터베이스 테이블을 생성하고 편집합니다.</td></tr></tbody></table>

### 제작 흐름

웹사이트는 다음 순서로 제작하고 운영합니다.

<table><thead><tr><th width="156.25">단계</th><th width="395.640625">내용</th></tr></thead><tbody><tr><td><strong>1. 앱 생성</strong></td><td>웹사이트 유형 선택 → 이름 입력 → 에디터 진입</td></tr><tr><td><strong>2. 웹사이트 제작</strong></td><td>AI 대화(Chat)로 웹사이트 생성/수정</td></tr><tr><td>↳ Preview 탭</td><td>실시간 미리보기</td></tr><tr><td>↳ Code 탭</td><td>소스코드 직접 편집</td></tr><tr><td>↳ Database 탭</td><td>데이터 관리</td></tr><tr><td><strong>3. 요구사항 정의</strong></td><td>요구사항/디자인 문서 작성 (선택)</td></tr><tr><td><strong>4. 연동 관리</strong></td><td>앱, 도구, 모델, 지식, MCP 연결 (필요시)</td></tr><tr><td><strong>5. 환경변수 설정</strong></td><td>API 키 등 민감 정보 등록 (필요시)</td></tr><tr><td><strong>6. 발행하기</strong></td><td>접근 권한(공유) 설정 → 배포 실행 → 라이브 URL 생성</td></tr><tr><td><strong>7. 운영/분석</strong></td><td>대시보드에서 방문 통계, 세션, 성능 지표 확인</td></tr></tbody></table>

#### 1. 앱 만들기

1. 상단 메뉴에서 **앱 만들기**를 선택합니다.
2. 앱 유형에서 **웹사이트**를 선택합니다.
3. 기본 정보를 입력한 뒤 **다음**을 선택합니다.

<table><thead><tr><th width="102.26953125">입력 항목</th><th width="101.59765625">필수 여부</th><th width="320.40625">설명</th></tr></thead><tbody><tr><td><strong>이름</strong></td><td>필수</td><td>앱 이름을 입력합니다. (최대 50자)</td></tr><tr><td><strong>소개</strong></td><td>선택</td><td>앱의 목적을 간단히 소개합니다. (최대 180자)</td></tr></tbody></table>

{% hint style="info" %}
처음 에디터를 열면 환경 설정에 약 1\~2분이 걸릴 수 있습니다.
{% endhint %}

**첫 진입 온보딩**

첫 진입 시 온보딩 캐러셀이 자동으로 표시됩니다.

채팅, 셀렉터, 발행 기능을 안내합니다. 준비가 끝나면 자동으로 사라집니다.

**에디터 접근 권한**

생성자와 편집 권한을 가진 사용자만 에디터에서 작업할 수 있습니다.

편집 권한이 없으면 웹사이트를 읽기 전용으로 확인할 수 있습니다.

#### 2. 웹사이트 제작

왼쪽 **채팅 패널**에서 AI와 대화합니다.

1. **메시지 입력창**에 만들 웹사이트를 설명합니다.
2. 필요하면 요구사항을 정의하고 연동을 추가합니다.
3. **Preview**에서 생성 결과를 실시간으로 확인합니다.
4. 수정이 필요하면 채팅으로 추가 요청을 보냅니다.

{% hint style="info" %}
#### 메시지 전송과 중단

* **대기 메시지 취소**: 메시지 앞의 \*\*✕\*\*를 선택합니다.
* **생성 중단**: AI가 작업 중일 때 `ESC`를 두 번 누릅니다.
{% endhint %}

#### 3. 버전 관리

주소 표시줄 오른쪽의 **버전 관리**에서 변경 이력을 확인합니다.

특정 버전을 선택해 해당 상태로 복원할 수 있습니다.

**버전 정보**

<table><thead><tr><th width="145.9296875">항목</th><th width="392.5078125">설명</th></tr></thead><tbody><tr><td><strong>버전명(레이블)</strong></td><td>사용자가 지정한 버전명 또는 자동 생성된 이름</td></tr><tr><td><strong>메모</strong></td><td>버전에 대한 메모 (선택사항)</td></tr><tr><td><strong>시간</strong></td><td>저장/발행/수정 시각</td></tr><tr><td><strong>기반 버전</strong></td><td>Draft인 경우, 어떤 버전을 기반으로 작업 중인지 표시</td></tr></tbody></table>

**버전 복원**

1. 버전 목록에서 복원할 버전을 선택합니다.
2. **선택 버전 불러오기**를 선택합니다.

**버전 생성 시점**

<table><thead><tr><th width="134.9921875">시점</th><th width="92.1484375">방식</th><th width="411.51171875">설명</th></tr></thead><tbody><tr><td><strong>코드 변경 시</strong></td><td>자동저장</td><td>AI가 코드를 수정하면 자동으로 저장 버전이 생성됩니다.</td></tr><tr><td><strong>발행 시</strong></td><td>배포</td><td>발행하면 해당 시점의 버전이 "운영중" 상태로 표시됩니다.</td></tr></tbody></table>

**Undo와 Redo**

채팅 입력창 위의 **버전 스트립**에서 변경 사항을 되돌리거나 다시 적용할 수 있습니다.

* **Undo**: 이전 변경 사항으로 되돌립니다.
* **Redo**: 되돌린 변경 사항을 다시 적용합니다.

{% hint style="warning" %}
Undo 후 새로 변경하면 이후 변경 이력은 대체됩니다.
{% endhint %}

#### 4. 크레딧 사용량

에디터 상단의 주소 표시줄에서 크레딧 사용량을 확인할 수 있습니다.

* **이 앱 사용량**: 현재 웹사이트 앱의 누적 크레딧입니다.
* **잔여 크레딧**: 워크스페이스에 남은 크레딧입니다.
* AI 작업이 끝날 때마다 사용량이 갱신됩니다.

수신 메시지 하단의 토글에서 작업별 토큰과 크레딧 사용량을 확인할 수 있습니다.
