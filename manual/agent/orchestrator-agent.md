---
description: 여러 서브 에이전트를 조합해 복잡한 요청을 처리하는 Orchestrator Agent의 구성 방법을 안내합니다.
---

# Orchestrator Agent

## Orchestrator Agent란

Orchestrator Agent는 여러 서브 에이전트를 도구로 호출하는 상위 에이전트입니다.

사용자 요청을 분석한 뒤 서브 에이전트에게 작업을 위임하고 그 결과를 종합해 최종 답변을 생성합니다.

<figure><img src="../../.gitbook/assets/image (878).png" alt=""><figcaption></figcaption></figure>

### 구성 요소

| 구성 요소                  | 역할                             |
| ---------------------- | ------------------------------ |
| **Orchestrator Agent** | 사용자와 대화하고 작업 위임과 결과 종합을 담당합니다. |
| **서브 에이전트**            | 특정 도메인 또는 작업을 처리합니다.           |

## 사용 시점

단일 에이전트의 역할이 과도하게 넓어질 때 사용합니다.

#### 컨텍스트를 분리해야 할 때

하위 작업에서 대량의 정보를 다루지만, 최종 답변에는 일부만 필요할 때 적합합니다. 서브 에이전트가 작업별 컨텍스트를 분리합니다.

#### 여러 영역을 함께 조사할 때

서로 독립적인 조사 작업을 나눠 처리할 수 있습니다. 병렬 실행의 주된 이점은 속도보다 탐색 범위입니다.

#### 역할과 도구를 분리해야 할 때

도구가 많거나 도메인별 지시문이 충돌하면 전문 에이전트로 분리합니다. 각 서브 에이전트는 맡은 역할에 맞는 도구와 지시문만 사용합니다.

### Workflow와 비교

Orchestrator Agent는 요청에 따라 도구와 실행 순서를 판단합니다. 같은 요청도 실행 과정이 달라질 수 있습니다. 실행 순서와 결과 형식을 통제해야 한다면 워크플로우를 사용합니다.

<figure><img src="../../.gitbook/assets/image (879).png" alt=""><figcaption></figcaption></figure>

#### Workflow · 단일 에이전트 · Orchestrator Agent 선택표

| 상황                     | 권장                     |
| ---------------------- | ---------------------- |
| 실행 순서와 결과 형식이 고정되어야 함  | **워크플로우**              |
| 요청이 다양하지만 도구가 많지 않음    | **단일 에이전트**            |
| 도구가 많거나 도메인별 역할이 분명함   | **Orchestrator Agent** |
| 대량의 하위 결과를 요약해 답변해야 함  | **Orchestrator Agent** |
| 독립적인 여러 영역을 폭넓게 조사해야 함 | **Orchestrator Agent** |

#### 단일 에이전트를 벗어날 시점 신호

* 하위 작업의 정보량이 많아 답변 품질이 떨어질 때
* 도구가 15\~20개를 넘어 선택이 어려워질 때
* 여러 출처의 조사가 서로 독립적일 때

## 사용 방법

먼저 서브 에이전트를 도구로 등록하고 관리자 승인을 받습니다. 자세한 절차는 [에이전트 도구 등록](add-as-tool.md)에서 확인합니다.

{% stepper %}
{% step %}
### Orchestrator Agent 만들기

<figure><img src="../../.gitbook/assets/image (873).png" alt=""><figcaption></figcaption></figure>

에이전트 앱을 새로 만듭니다. 이 앱이 사용자 요청을 받고 서브 에이전트를 호출합니다.
{% endstep %}

{% step %}
### 서브 에이전트 추가

<figure><img src="../../.gitbook/assets/스크린샷 2026-08-14 154202.png" alt=""><figcaption></figcaption></figure>

**도구 설정**에서 **편집**을 선택합니다. 서브 에이전트로 사용할 에이전트를 추가합니다.

{% hint style="info" %}
에이전트 도구를 추가하면 프롬프트 영역에 **Orchestrator**가 표시됩니다.
{% endhint %}
{% endstep %}

{% step %}
### 입력 변수 설정

<figure><img src="../../.gitbook/assets/image (875).png" alt=""><figcaption></figcaption></figure>

서브 에이전트에 항상 전달할 값이 있다면 도구 설정 토글 옆의 **입력 변수**를 선택해 값을 입력합니다.
{% endstep %}

{% step %}
### 프롬프트 작성

<figure><img src="../../.gitbook/assets/image (876).png" alt=""><figcaption></figcaption></figure>

@ 멘션으로 서브 에이전트, 지식, 도구를 참조합니다. 각 항목의 역할과 사용할 조건을 프롬프트에 작성합니다.

{% hint style="info" %}
어떤 요청을 누구에게 위임할지 구체적으로 작성합니다. 역할이 겹치지 않도록 서브 에이전트의 담당 범위를 구분합니다. 자세한 사항은 [orchestrator-agent.md](../../study/prompt/orchestrator-agent.md "mention")을 참고합니다.
{% endhint %}
{% endstep %}

{% step %}
### 테스트 및 확인

<figure><img src="../../.gitbook/assets/image (877).png" alt=""><figcaption></figcaption></figure>

테스트 요청으로 서브 에이전트가 의도한 조건에서 호출되는지 확인합니다. 앱 목록에 Orchestrator Agent 표시가 나타나는지도 확인합니다.
{% endstep %}
{% endstepper %}

{% include "../../.gitbook/includes/orchestrator-....md" %}
