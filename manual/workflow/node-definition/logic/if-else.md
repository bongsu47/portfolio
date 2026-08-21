---
description: 변수 값을 규칙과 비교해 워크플로우 실행 경로를 분기하는 노드입니다.
---

# 조건

조건 노드는 설정한 규칙에 따라 워크플로우 경로를 분기합니다.\
“만약 조건이 참이면 A, 거짓이면 B”와 같은 흐름을 구성할 수 있습니다.

<figure><img src="../../../../.gitbook/assets/image (45).png" alt="" width="221"><figcaption></figcaption></figure>

### 역할

변수 값을 검사하고 결과에 따라 다른 경로로 분기합니다.

다음과 같은 규칙을 설정할 수 있습니다.

* 메시지에 “안녕”이 포함되면 인사 응답으로 분기
* 점수가 80점 이상이면 합격 처리
* 파일이 있으면 파일 분석, 없으면 텍스트 처리

조건 노드는 명확한 규칙으로 분기합니다.\
AI 모델을 호출하지 않아 비용이 없고 결과가 일관됩니다.

### 설정

조건 노드를 선택하면 설정 패널이 열립니다.\
패널은 **IF**, **ELSE IF**, **ELSE** 분기로 구성됩니다.

<figure><img src="../../../../.gitbook/assets/image (642).png" alt="" width="330"><figcaption></figcaption></figure>

* **IF**: 가장 먼저 검사합니다. 항상 하나 존재하며 삭제할 수 없습니다.
* **ELSE IF**: IF가 거짓일 때 추가로 검사합니다. 여러 개 추가할 수 있습니다.
* **ELSE**: 모든 조건이 거짓일 때 실행합니다. 삭제할 수 없습니다.

#### 조건 추가

<figure><img src="../../../../.gitbook/assets/image (643).png" alt="" width="332"><figcaption></figcaption></figure>

1. IF 아래의 **선택한 변수를 조건 대상으로 지정합니다**를 선택합니다.
2. 변수 목록이 나타나면, 비교할 변수를 선택합니다.
3. 변수 타입에 맞는 비교 연산자가 자동으로 설정됩니다.
4. 필요하면 드롭다운에서 연산자를 변경합니다.
5. 비교 값을 입력합니다. `/`로 다른 노드의 변수를 사용할 수 있습니다.

{% hint style="info" %}
**값 입력란이 없는 연산자**

`비어 있음`, `비어 있지 않음`, `null임`, `null이 아님`, `존재`, `존재하지 않음`은 비교 값이 필요 없습니다.\
이 연산자를 선택하면 값 입력란이 표시되지 않습니다.
{% endhint %}

#### 여러 조건 조합

하나의 IF 또는 ELSE IF에 여러 조건을 추가할 수 있습니다.

* **IF 분기**: 오른쪽의 `+`를 선택합니다.

<figure><img src="../../../../.gitbook/assets/image (644).png" alt="" width="331"><figcaption></figcaption></figure>

* **ELSE IF 분기**: `···` 메뉴에서 **조건 추가**를 선택합니다.

<figure><img src="../../../../.gitbook/assets/image (646).png" alt="" width="331"><figcaption></figcaption></figure>

조건이 두 개 이상이면 **그리고**와 **또는**을 선택할 수 있습니다.

| 조합            | 의미            | 예시                                    |
| ------------- | ------------- | ------------------------------------- |
| **그리고** (AND) | 모든 조건이 참이어야 함 | 점수 ≥ 80 **그리고** 출석 ≥ 90 → 둘 다 만족해야 참  |
| **또는** (OR)   | 하나라도 참이면 됨    | VIP 회원 **또는** 포인트 ≥ 1000 → 하나만 만족해도 참 |

조건이 하나면 조합 옵션이 표시되지 않습니다.

#### ELSE IF 추가

<figure><img src="../../../../.gitbook/assets/image (647).png" alt="" width="330"><figcaption></figcaption></figure>

패널 하단의 **+ ELSE IF 추가**를 선택하면 새 분기가 추가됩니다.\
각 ELSE IF에는 독립적인 조건과 조합 방식을 설정할 수 있습니다.

IF와 같은 방식으로 변수를 선택하고 조건을 추가합니다.

#### 삭제

* **조건 삭제**: 조건 오른쪽의 **휴지통**을 선택합니다.
* **ELSE IF 삭제**: 분기 오른쪽의 `···`에서 **분기 삭제**를 선택합니다.

IF와 ELSE는 삭제할 수 없습니다.

#### 검사 순서

조건은 위에서 아래로 검사합니다.

1. IF가 참이면 IF 경로로 이동합니다.
2. IF가 거짓이면 ELSE IF를 순서대로 검사합니다.
3. 처음으로 참인 ELSE IF 경로로 이동합니다.
4. 모두 거짓이면 ELSE 경로로 이동합니다.

{% hint style="warning" %}
**조건 순서**

처음으로 참인 조건의 경로로 이동합니다.\
나머지 조건은 검사하지 않습니다.

예를 들어 `점수 ≥ 60`을 `점수 ≥ 90`보다 위에 둡니다.\
점수가 95여도 첫 조건에 먼저 일치합니다.\
구체적인 조건을 위에, 일반적인 조건을 아래에 배치하세요.
{% endhint %}

#### 비교 연산자

변수 타입에 맞는 연산자가 자동으로 설정됩니다.\
드롭다운에서 변경할 수 있습니다.

<table><thead><tr><th width="159.46484375">연산자</th><th width="95.75390625" align="center">텍스트</th><th width="82.8984375" align="center">숫자</th><th width="80.0625" align="center">배열</th><th width="99.0859375" align="center">파일</th><th>설명</th></tr></thead><tbody><tr><td>포함 / 포함하지 않음</td><td align="center">O</td><td align="center"></td><td align="center">O</td><td align="center"></td><td>특정 값이 들어있는지</td></tr><tr><td>시작 / 끝</td><td align="center">O</td><td align="center"></td><td align="center"></td><td align="center"></td><td>특정 텍스트로 시작하거나 끝나는지</td></tr><tr><td>이다 / 아니다</td><td align="center">O</td><td align="center"></td><td align="center"></td><td align="center"></td><td>정확히 일치하는지</td></tr><tr><td>= / ≠ / > / &#x3C; / ≥ / ≤</td><td align="center"></td><td align="center">O</td><td align="center"></td><td align="center"></td><td>숫자 크기 비교</td></tr><tr><td>존재 / 존재하지 않음</td><td align="center"></td><td align="center"></td><td align="center"></td><td align="center">O</td><td>파일이 있는지</td></tr><tr><td>비어 있음 / 비어 있지 않음</td><td align="center">O</td><td align="center">O</td><td align="center">O</td><td align="center"></td><td>값이 빈 상태인지</td></tr><tr><td>null임 / null이 아님</td><td align="center">O</td><td align="center">O</td><td align="center">O</td><td align="center">O</td><td>변수 자체가 존재하는지</td></tr></tbody></table>

{% hint style="info" %}
**`포함`과 `이다`의 차이** — `포함`은 텍스트에 값이 있으면 참입니다. `이다`는 텍스트가 정확히 일치해야 참입니다.

**`비어 있음`과 `null임`의 차이** — `비어 있음`은 값이 빈 상태입니다. `null임`은 변수 자체가 없는 상태입니다. 이전 노드 실행 여부에는 `null임`을 사용하세요.
{% endhint %}

#### 파일 세부 조건

`sys.files` 같은 파일 배열을 선택하면 **하위 변수 선택**이 표시됩니다.\
`name`, `extension`, `size`, `type`, `mime_type`으로 세부 조건을 설정할 수 있습니다.

예: **하위 변수 선택** → **type** → 이미지, 문서, 오디오, 비디오\
예: **하위 변수 선택** → **extension** → `pdf`, `xlsx`

#### 의도 분류 노드와 비교

|        | 조건 노드          | 의도 분류 노드           |
| ------ | -------------- | ------------------ |
| 분기 기준  | 값을 규칙으로 비교     | AI가 텍스트의 의미를 판단    |
| 비용     | 없음             | AI 모델 호출 비용 발생     |
| 속도     | 즉시 처리          | 모델 호출 시간 필요        |
| 적합한 상황 | "이 값이 무엇인지" 확인 | "이 질문이 어떤 유형인지" 파악 |

명확한 값 비교에는 조건 노드를 사용하세요.\
다양한 자연어 표현의 의도를 분류해야 하면 의도 분류 노드를 사용하세요.

### 활용 예제

{% content-ref url="../../../../study/miso/lesson1/level2.md" %}
[level2.md](../../../../study/miso/lesson1/level2.md)
{% endcontent-ref %}
