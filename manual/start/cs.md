---
description: 미소를 사용하며 발생하는 궁금한 점을 바로 묻거나, 불편·오류·개선 요청을 접수할 수 있는 도우미입니다.
---

# 미소 CS봇

#### CS봇 열기

화면 오른쪽 아래의 **미소 캐릭터 버튼**을 선택하면 CS봇 창이 열립니다.

캐릭터는 지금 보고 있는 화면에 따라 모습이 바뀝니다. 워크플로우에서는 블록을 쌓고, 에이전트에서는 로봇과 함께, 지식에서는 책장 옆에서 맞이합니다.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FWekRDsviPVGYf88oMDle%2Fcharacters.png?alt=media&#x26;token=3b08bb2c-2d39-41a5-8b6a-a0951a4eec6d" alt="" width="520"><figcaption><p>화면마다 바뀌는 미소 캐릭터</p></figcaption></figure></div>

* 버튼은 드래그해서 원하는 위치로 옮길 수 있습니다. 옮긴 위치는 이 브라우저에 저장됩니다.
* 창 위쪽 제목 부분을 드래그하면 창도 옮길 수 있습니다. **Esc** 키를 누르면 창이 닫힙니다.
* CS봇은 로그인한 MISO 화면 어디에서나 사용할 수 있습니다.

창 위쪽의 버튼은 다음과 같습니다.

| 버튼                  | 하는 일                         |
| ------------------- | ---------------------------- |
| **+ 새 대화**          | 지금 대화를 마치고 새 대화를 시작합니다.      |
| **이전 대화** (시계 아이콘)  | 지난 대화 목록을 열어 이어서 질문합니다.      |
| **문의내역** (클립보드 아이콘) | 내가 등록한 이슈와 처리 상태를 확인합니다.     |
| **닫기**              | 창을 닫습니다. 대화 내용은 그대로 남아 있습니다. |

#### 질문하기

{% stepper %}
{% step %}
**질문 입력하기**

**질문하기** 탭에 궁금한 내용을 입력하고 **Enter**를 누르거나 전송 버튼을 선택합니다.

처음 화면의 **추천 질문**을 선택하면 바로 물어볼 수 있습니다. 추천 질문은 지금 보고 있는 화면에 맞춰 달라집니다.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FKq32SpsVIrGWYgxXG0CS%2F01-welcome-workflow.png?alt=media&#x26;token=643275d7-d507-4bb5-aa47-b01a97593201" alt="" width="375"><figcaption><p>워크플로우 편집 화면에서 연 첫 화면</p></figcaption></figure></div>
{% endstep %}

{% step %}
**답을 찾는 과정 확인하기**

답을 만드는 동안 **생각 중** 아래에 지금 무엇을 확인하고 있는지 보여 줍니다.

답이 끝나면 **○초 생각했어요**로 접힙니다. 선택하면 화면과 문서를 어떤 순서로 확인했는지 단계별로 볼 수 있습니다.

답변을 기다리는 동안에는 전송 버튼이 정지 버튼으로 바뀝니다. 답변 표시를 멈추고 싶을 때 선택하세요.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2Fn19xrNrDMy1WCV3f2EMH%2F04-answer-steps.png?alt=media&#x26;token=3dbb7d26-fcc9-42ae-8128-5021eeea4470" alt="" width="375"><figcaption><p>'○초 생각했어요'를 선택하면 답을 찾은 과정이 펼쳐집니다</p></figcaption></figure></div>
{% endstep %}

{% step %}
**답변 활용하고 이어서 묻기**

답변 아래의 복사 버튼으로 답변을 복사할 수 있습니다. 코드는 코드 블록의 **복사** 버튼으로 바로 복사합니다.

추가로 궁금한 점은 이어서 질문하세요. CS봇이 앞에서 나눈 대화를 기억하고 답합니다.

답변이 도움이 됐다면 👍, 아쉬웠다면 👎를 눌러 알려 주세요. 답변 품질을 높이는 데 반영됩니다.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
평소 말하듯 짧게 물어봐도 괜찮습니다. 예) "각 노드가 하는 일을 알려줘", "실행이 멈추는 원인을 찾아줘", "문서를 올렸는데 검색이 안 돼요", "워크플로우와 에이전트는 뭐가 달라?"
{% endhint %}

#### 지금 보고 있는 화면을 함께 봐요

워크플로우·에이전트 편집 화면이나 지식 화면에서 질문하면, CS봇이 화면의 구성(노드와 연결, 설정 값 등)을 함께 보고 답합니다. 화면을 따로 설명하거나 캡처하지 않아도 됩니다.

* 첫 화면 위쪽에 지금 보고 있는 앱 이름이 표시됩니다.
* 대화 중에 다른 화면으로 옮기면 대화 안에 구분선이 생깁니다. 구분선 아래부터는 새 화면을 기준으로 답합니다.
* 비밀번호나 API 키 같은 값은 CS봇에 보내지 않습니다.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2Fbithajqiu2lA3dlgHGSK%2F15-divider.png?alt=media&#x26;token=c14e98a2-56fc-49f7-9290-03a12b25e65a" alt="" width="375"><figcaption><p>다른 화면으로 옮기면 구분선으로 알려 줍니다</p></figcaption></figure></div>

화면별로 이런 질문을 해 보세요.

| 화면      | 질문 예시                                                    |
| ------- | -------------------------------------------------------- |
| 워크플로우   | "이 워크플로우가 어떻게 동작하는지 설명해줘", "이 앱을 더 안정적으로 만들려면 뭘 고쳐야 해?"  |
| 에이전트    | "시스템 프롬프트를 더 명확하게 다듬어줘", "도구가 호출되지 않는 이유가 뭐야?"           |
| 지식      | "문서를 올렸는데 검색이 안 돼요", "청크 크기는 어떻게 정해?"                    |
| 그 밖의 화면 | "만들고 싶은 앱을 처음부터 같이 설계해줘", "노션, 구글 시트 같은 외부 도구를 연결하고 싶어요" |

#### 화면 캡처 첨부하기

오류 메시지나 화면을 캡처해 함께 보내면 더 정확하게 답할 수 있습니다.

* 입력창 왼쪽 아래의 이미지 버튼을 선택하거나, 캡처한 이미지를 입력창에 붙여넣거나(Ctrl+V / ⌘+V) 끌어다 놓습니다.
* 질문 하나에 최대 3장, 한 장에 10MB까지 첨부할 수 있습니다. (PNG, JPG, WebP, GIF)
* 질문 없이 이미지만 보내도 됩니다.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FQb5Y2Hnqsk1EhpU1YohQ%2F05-attach-composer.png?alt=media&#x26;token=a886145a-32bc-46a0-8e11-dc697c656541" alt="" width="375"><figcaption><p>오류 화면을 캡처해 질문과 함께 보내기</p></figcaption></figure></div>

#### 오류 원인 찾기

앱 편집 화면에서 "실행하면 오류가 나요"처럼 물어보면, CS봇이 내 최근 실행 기록을 확인해 원인을 함께 찾습니다.

답변은 **어떤 오류인가요 → 무슨 뜻인가요 → 왜 생겼나요 → 어떻게 고치나요** 순서로 안내합니다. 답변 아래의 **확인한 실행 기록**에서 실제로 확인한 실행 번호와 오류 문구를 볼 수 있습니다.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2F7GRNZnzcMvrtNmWndHKD%2Fpair-error.png?alt=media&#x26;token=fd989f5d-5355-4e73-82e7-0e2265eb8e16" alt="" width="700"><figcaption><p>왼쪽: 오류의 뜻과 원인 · 오른쪽: 해결 방법과 확인한 실행 기록</p></figcaption></figure></div>

{% hint style="info" %}
특정 실행이 궁금하다면 실행 번호를 함께 적어 주세요. 예) "실행 #4가 왜 실패했어?"
{% endhint %}

#### 내 계정 정보 물어보기

내 권한, 크레딧, 사용할 수 있는 모델, 워크스페이스의 도구, 접근할 수 있는 에이전트는 CS봇이 바로 조회해서 알려 줍니다.

"내 지식 중에 인사 관련된 게 있어?", "내 앱 중에 주문 관련된 거 있어?"처럼 내가 만든 앱과 지식에서 찾아 달라고 할 수도 있습니다.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2F8pPeHmJiKPI0p9laeTWS%2Fr-R1-1.png?alt=media&#x26;token=02a0670e-b073-40dc-a7ce-027e5a726d92" alt="" width="375"><figcaption><p>내가 만든 지식 중에서 질문에 맞는 항목을 골라 줍니다</p></figcaption></figure></div>

{% hint style="info" %}
지금 로그인한 계정으로 볼 수 있는 정보만 조회합니다. 다른 사람의 정보는 조회하지 않습니다.
{% endhint %}

#### 이슈 등록하기

질문으로 해결되지 않는 오류나 개선 요청은 이슈로 접수합니다. 대화에서 초안을 받아 등록하거나, **이슈등록** 탭에서 직접 작성할 수 있습니다.

**대화에서 이슈 초안 받기**

CS봇이 직접 해결하기 어려운 문제라고 판단하면 답변 아래에 **이슈등록 초안**을 보여 줍니다. "편집하다가 노드가 사라졌어요. 신고해줘"처럼 직접 요청해도 됩니다.

**확인하고 등록하기**를 선택하면 이슈등록 탭에 유형·제목·내용이 채워진 채로 열립니다. 대화에서 확인하지 못한 내용은 '(입력 필요)'로 표시되니 채워서 등록해 주세요.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FGJYiFrJQkMbgG3PxkIU5%2Fpair-issue.png?alt=media&#x26;token=b90217bb-8b07-41bc-8c8f-8b1e2f1fdbd9" alt="" width="700"><figcaption><p>왼쪽: 답변 아래에 붙는 이슈등록 초안 · 오른쪽: 내용이 채워진 이슈등록 탭</p></figcaption></figure></div>

{% hint style="warning" %}
CS봇이 대신 등록하지는 않습니다. 내용을 확인한 뒤 **등록**을 직접 선택해야 접수됩니다.
{% endhint %}

**직접 작성하기**

{% stepper %}
{% step %}
**유형 선택하기**

**버그 및 오류**, **UX 개선**, **기능 추가** 중 유형을 선택합니다.
{% endstep %}

{% step %}
**이슈 작성하기**

제목과 내용을 입력합니다. 재현 단계와 기대 동작을 함께 적으면 더 빠르게 확인할 수 있습니다.

이슈 하나에는 한 가지 내용만 적어 주세요. 여러 문제는 각각 등록하면 진행 상황을 확인하기 쉽습니다.
{% endstep %}

{% step %}
**첨부하고 등록하기**

필요하면 이미지를 최대 3장(한 장에 10MB)까지 첨부하고 **등록**을 선택합니다.

등록하면 지금 보고 있는 화면의 캡처와 주소가 자동으로 함께 기록되어, 문제를 빠르게 확인하는 데 도움이 됩니다. CS봇 창과 비밀번호 입력란은 캡처에 담기지 않습니다. 등록한 이슈는 MISO 운영팀에 전달됩니다.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2Frkcajf6WoNxYj8Rbz069%2F11-issue-tab.png?alt=media&#x26;token=3ada3bcf-c0af-4cc0-a052-275e93aa94b7" alt="" width="375"><figcaption><p>이슈등록 탭</p></figcaption></figure></div>
{% endstep %}
{% endstepper %}

**처리 상태 확인하기**

창 위쪽의 **문의내역** 버튼을 선택하면 내가 등록한 이슈를 최신순으로 볼 수 있습니다. 상태는 **접수됨** 또는 **완료**로 표시되고, 항목을 선택하면 등록한 내용을 다시 확인할 수 있습니다. 담당팀이 이슈를 검토한 뒤 처리하며, 처리에는 시간이 걸릴 수 있습니다.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FqjdDwMQgc1uynCbl0Ohn%2Fpair-inbox.png?alt=media&#x26;token=30409d7d-1c47-4802-a416-0db46fb13a50" alt="" width="700"><figcaption><p>왼쪽: 내 문의내역 · 오른쪽: 문의 상세</p></figcaption></figure></div>

#### 이전 대화 이어 하기

창 위쪽의 **이전 대화** 버튼을 선택하면 최근 대화 30개를 볼 수 있습니다. 대화를 선택하면 그 대화가 다시 열리고, 이어서 질문할 수 있습니다.

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FikQFVaEwkAZS45vCdXMe%2Fuploads%2FAKrU3F9l2oXgl6XfumjZ%2F14-history.png?alt=media&#x26;token=e24542c5-5342-462a-8902-5d900c20ca78" alt="" width="375"><figcaption><p>이전 대화 목록</p></figcaption></figure></div>

#### 알아 두면 좋아요

* CS봇은 MISO 사용법을 안내하고 문제의 원인을 함께 찾습니다. 앱을 직접 수정·저장·실행하지는 않으니, 안내에 따라 직접 바꿔 주세요.
* 정식 출시된 기능을 기준으로 안내합니다. 관리자가 켜야 하는 기능은 고객사 관리자나 MISO 담당자에게 문의해 주세요.
* 비밀번호, API 키, 개인정보 같은 민감한 정보는 질문이나 이슈에 넣지 마세요.
* 질문은 한 번에 8,000자까지 입력할 수 있습니다.
