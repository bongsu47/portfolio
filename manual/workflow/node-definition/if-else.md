---
description: >-
  입력된 변수와 내용을 바탕으로 LLM이 조건을 판단해 워크플로우의 실행 경로를 나누는 노드입니다. 상황에 따라 서로 다른 흐름으로 자연스럽게
  분기할 수 있습니다.
---

# 조건

조건 노드는 설정한 조건에 따라 워크플로우의 흐름을 나누는 노드입니다.\
"만약 \~라면 A를, 아니라면 B를 실행하라"와 같은 분기 처리를 할 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (45).png" alt="" width="221"><figcaption></figcaption></figure>

***

## 어떤 역할을 하나요?

조건 노드는 변수의 값을 검사하여, 결과에 따라 서로 다른 경로로 분기합니다.

예를 들어,

* 사용자의 메시지가 "안녕"을 포함하면 → 인사 응답으로 분기
* 점수가 80점 이상이면 → 합격 처리, 아니면 → 불합격 처리
* 파일이 첨부되었으면 → 파일 분석으로 이동, 아니면 → 텍스트 처리로 이동

의도 분류 노드가 AI의 판단에 의존한다면, 조건 노드는 **명확한 규칙**에 따라 분기합니다.\
AI 모델을 호출하지 않으므로 비용이 없고, 결과가 항상 일관됩니다.

***

## 설정 방법

조건 노드를 클릭하면 설정 패널이 열립니다.\
패널은 **IF**, **ELSE IF**, **ELSE** 세 종류의 분기로 구성됩니다.

<figure><img src="../../../.gitbook/assets/image (642).png" alt="" width="330"><figcaption></figcaption></figure>

* **IF**: 가장 먼저 검사되는 조건입니다. 항상 하나 존재하며 삭제할 수 없습니다.
* **ELSE IF**: IF가 거짓일 때 추가로 검사할 조건입니다. 여러 개 추가할 수 있습니다.
* **ELSE**: 위의 모든 조건이 거짓일 때 실행되는 기본 경로입니다. 항상 존재하며 삭제할 수 없습니다.

***

### 조건 추가하기

<figure><img src="../../../.gitbook/assets/image (643).png" alt="" width="332"><figcaption></figcaption></figure>

1. IF 아래에 있는 **선택한 변수를 조건 대상으로 지정합니다** 버튼을 클릭합니다.
2. 변수 목록이 나타나면, 비교할 변수를 선택합니다.
3. 변수를 선택하면 조건이 추가되고, 변수 타입에 맞는 비교 연산자가 자동으로 설정됩니다.
4. 필요하면 연산자 드롭다운을 클릭하여 다른 연산자로 변경할 수 있습니다.
5. 연산자 아래에 값 입력란이 나타나면, 비교할 값을 입력합니다. 값 입력란에 `/`를 입력하면 다른 노드의 변수를 값으로 사용할 수도 있습니다.

{% hint style="info" %}
#### 값 입력란이 안 보이는 경우

"비어 있음", "비어 있지 않음", "null임", "null이 아님", "존재", "존재하지 않음" 연산자는 비교할 값이 필요 없습니다.\
이 연산자들을 선택하면 값 입력란이 나타나지 않는 것이 정상입니다.
{% endhint %}

***

### 같은 분기에 조건 여러 개 추가하기 (그리고 / 또는)

하나의 IF나 ELSE IF에 조건을 여러 개 추가할 수 있습니다.

* **IF 분기**: 오른쪽의 `+` 버튼을 클릭합니다.

<figure><img src="../../../.gitbook/assets/image (644).png" alt="" width="331"><figcaption></figcaption></figure>

* **ELSE IF 분기**: 오른쪽의 `···` 메뉴에서 **조건 추가**를 선택합니다.

<figure><img src="../../../.gitbook/assets/image (646).png" alt="" width="331"><figcaption></figcaption></figure>

조건이 2개 이상이 되면, 분기 제목 오른쪽에 **그리고** / **또는** 탭이 나타납니다.\
탭을 클릭하여 조건 조합 방식을 선택합니다.

| 조합            | 의미            | 예시                                    |
| ------------- | ------------- | ------------------------------------- |
| **그리고** (AND) | 모든 조건이 참이어야 함 | 점수 ≥ 80 **그리고** 출석 ≥ 90 → 둘 다 만족해야 참  |
| **또는** (OR)   | 하나라도 참이면 됨    | VIP 회원 **또는** 포인트 ≥ 1000 → 하나만 만족해도 참 |

조건이 1개뿐이면 그리고/또는 탭은 나타나지 않습니다.

***

### ELSE IF 추가하기

<figure><img src="../../../.gitbook/assets/image (647).png" alt="" width="330"><figcaption></figcaption></figure>

패널 하단의 **+ ELSE IF 추가** 버튼을 클릭하면 새로운 분기가 추가됩니다.\
ELSE IF는 여러 개 추가할 수 있으며, 각 ELSE IF마다 독립적으로 조건과 그리고/또는을 설정합니다.

ELSE IF가 추가되면 IF와 동일한 방법으로 **선택한 변수를 조건 대상으로 지정합니다** 버튼을 클릭하여 조건을 추가합니다.

***

### 삭제하기

* **조건 삭제**: 해당 조건 오른쪽의 **휴지통** 아이콘을 클릭합니다.
* **ELSE IF 분기 삭제**: 해당 분기 오른쪽의 `···` 메뉴에서 **분기 삭제**를 선택합니다.

IF와 ELSE는 삭제할 수 없습니다.

***

### 검사 순서

조건은 **위에서 아래로** 순서대로 검사됩니다.

1. **IF** 조건을 먼저 검사 → 참이면 IF 경로로 이동, 나머지는 검사하지 않음
2. IF가 거짓이면 → **ELSE IF** 조건을 위에서부터 차례대로 검사
3. 처음으로 참이 되는 ELSE IF의 경로로 이동
4. 모든 조건이 거짓이면 → **ELSE** 경로로 이동

{% hint style="warning" %}
#### 조건 순서가 중요합니다

가장 먼저 참이 되는 조건의 경로로 이동하고, 나머지 조건은 검사하지 않습니다.

예를 들어, "점수 ≥ 60"을 "점수 ≥ 90"보다 위에 배치하면, 점수가 95여도 "점수 ≥ 60" 조건에 먼저 걸려서 의도한 경로가 아닌 곳으로 이동합니다.\
**더 구체적인(좁은) 조건을 위에**, **더 일반적인(넓은) 조건을 아래에** 배치하세요.
{% endhint %}

***

### 비교 연산자

변수를 선택하면 타입에 맞는 연산자가 자동으로 설정됩니다. 드롭다운을 클릭하여 변경할 수 있습니다.

<table><thead><tr><th width="159.46484375">연산자</th><th width="95.75390625" align="center">텍스트</th><th width="82.8984375" align="center">숫자</th><th width="80.0625" align="center">배열</th><th width="99.0859375" align="center">파일</th><th>설명</th></tr></thead><tbody><tr><td>포함 / 포함하지 않음</td><td align="center">O</td><td align="center"></td><td align="center">O</td><td align="center"></td><td>특정 값이 들어있는지</td></tr><tr><td>시작 / 끝</td><td align="center">O</td><td align="center"></td><td align="center"></td><td align="center"></td><td>특정 텍스트로 시작하거나 끝나는지</td></tr><tr><td>이다 / 아니다</td><td align="center">O</td><td align="center"></td><td align="center"></td><td align="center"></td><td>정확히 일치하는지</td></tr><tr><td>= / ≠ / > / &#x3C; / ≥ / ≤</td><td align="center"></td><td align="center">O</td><td align="center"></td><td align="center"></td><td>숫자 크기 비교</td></tr><tr><td>존재 / 존재하지 않음</td><td align="center"></td><td align="center"></td><td align="center"></td><td align="center">O</td><td>파일이 있는지</td></tr><tr><td>비어 있음 / 비어 있지 않음</td><td align="center">O</td><td align="center">O</td><td align="center">O</td><td align="center"></td><td>값이 빈 상태인지</td></tr><tr><td>null임 / null이 아님</td><td align="center">O</td><td align="center">O</td><td align="center">O</td><td align="center">O</td><td>변수 자체가 존재하는지</td></tr></tbody></table>

{% hint style="info" %}
**"포함"과 "이다"의 차이** — "포함"은 텍스트 안에 해당 단어가 들어있으면 참이고, "이다"는 텍스트가 정확히 일치해야 참입니다.

**"비어 있음"과 "null임"의 차이** — "비어 있음"은 변수는 있지만 값이 빈 상태(빈 텍스트, 빈 배열)이고, "null임"은 변수 자체가 없는 상태입니다. 보통은 "비어 있음"으로 충분하고, 이전 노드의 실행 여부를 확인할 때 "null임"을 사용합니다.
{% endhint %}

### 파일의 세부 조건

`sys.files`처럼 파일 배열 변수를 선택하면 **하위 변수 선택** 버튼이 나타납니다.\
파일의 세부 속성(name, extension, size, type, mime\_type)을 선택하여 더 구체적인 조건을 만들 수 있습니다.

예: **하위 변수 선택** → **type** → 이미지/문서/오디오/비디오 중 선택\
예: **하위 변수 선택** → **extension** → "pdf", "xlsx" 등으로 비교

***

#### 의도 분류 노드와 어떤 걸 써야 하나요?

|        | 조건 노드          | 의도 분류 노드           |
| ------ | -------------- | ------------------ |
| 분기 기준  | 값을 규칙으로 비교     | AI가 텍스트의 의미를 판단    |
| 비용     | 없음             | AI 모델 호출 비용 발생     |
| 속도     | 즉시 처리          | 모델 호출 시간 필요        |
| 적합한 상황 | "이 값이 무엇인지" 확인 | "이 질문이 어떤 유형인지" 파악 |

명확한 값 비교가 가능하면 조건 노드를 사용하는 것이 비용과 속도 면에서 유리합니다.\
"연차 며칠 남았어?", "휴가 쓰고 싶은데"처럼 같은 의도를 다양하게 표현하는 자연어를 분류해야 한다면 의도 분류 노드를 사용하세요.

## 활용 예제

{% content-ref url="../../../study/miso/lesson1/level2.md" %}
[level2.md](../../../study/miso/lesson1/level2.md)
{% endcontent-ref %}
