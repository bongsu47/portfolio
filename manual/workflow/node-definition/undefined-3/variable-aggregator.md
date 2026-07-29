---
description: 조건 분기나 의도 분류 이후 여러 경로의 변수 중 실제로 값이 있는 결과를 하나로 모아 다음 노드에 전달하는 노드입니다.
---

# 변수 집계기

변수 집계기 노드는 여러 경로의 변수 값을 하나로 모읍니다.

조건 또는 의도 분류 뒤에 경로를 하나로 합칠 때 사용합니다.

<figure><img src="../../../../.gitbook/assets/image (648).png" alt="" width="306"><figcaption></figcaption></figure>

### 역할

조건 노드나 의도 분류 노드는 워크플로우를 여러 경로로 분기합니다.\
실제로 실행한 경로만 값을 반환합니다.

<figure><img src="../../../../.gitbook/assets/image (9) (1).png" alt="" width="375"><figcaption></figcaption></figure>

변수 집계기는 여러 경로에서 값이 있는 변수를 선택합니다.

다음과 같은 작업에 사용할 수 있습니다.

* 조건 분기 뒤 실행한 경로의 LLM 결과를 답변 노드에 전달합니다.
* 의도 분류 뒤 실제 분류된 경로의 결과를 가져옵니다.

최종 답변 생성이나 로그 기록처럼 공통 처리가 필요할 때 사용하세요.

### 설정

1. 분기된 경로 뒤에 변수 집계기를 추가합니다.
2. 각 경로의 마지막 노드를 변수 집계기에 연결합니다.
3. **입력 변수 설정**에서 각 경로의 출력 변수를 추가합니다.

<figure><img src="../../../../.gitbook/assets/image (10) (1).png" alt="" width="563"><figcaption></figcaption></figure>

### 출력 변수

| 변수       | 설명       |
| -------- | -------- |
| `output` | 수집된 변수 값 |

### 활용 예시

{% content-ref url="../../../../study/miso/lesson1/level3.md" %}
[level3.md](../../../../study/miso/lesson1/level3.md)
{% endcontent-ref %}
