---
description: 계산, 데이터 변환, 텍스트 가공처럼 규칙 기반 처리를 실행하는 노드입니다.
---

# 코드

코드 노드는 작성한 코드로 데이터를 처리합니다.

<figure><img src="../../../../.gitbook/assets/image (658).png" alt="" width="312"><figcaption></figcaption></figure>

계산, 데이터 변환, 텍스트 가공처럼 정확한 로직이 필요할 때 사용합니다.\
정확한 계산과 규칙 기반 처리에는 코드 노드가 적합합니다.

### 역할

정의한 규칙에 따라 데이터를 처리하고 결과를 반환합니다.\
LLM의 판단보다 정확한 결과가 필요한 작업에 적합합니다.

다음과 같은 작업에 사용할 수 있습니다.

* 숫자 계산과 통계 처리
* 텍스트에서 특정 패턴 추출
* JSON, CSV 같은 형식으로 데이터 변환

{% hint style="info" %}
**코드 노드, LLM 노드, 템플릿 노드**

* **코드 노드**: 정확한 계산, 데이터 변환, 복잡한 로직에 사용합니다.
* **LLM 노드**: 자연어 처리, 요약, 분류에 사용합니다.
* **템플릿 노드**: 텍스트 조합과 형식 지정에 사용합니다.

정확한 결과에는 코드 노드를 사용하세요.\
자연어 판단에는 LLM 노드를 사용하세요.
{% endhint %}

### 설정

<figure><img src="../../../../.gitbook/assets/image (8) (1).png" alt="" width="363"><figcaption></figcaption></figure>

#### 변수 매핑

코드에서 사용할 입력 변수를 설정합니다.\
이전 노드의 결과를 연결하면 해당 변수 이름으로 사용할 수 있습니다.

**추가**를 선택해 변수를 추가합니다.\
각 변수에는 이름과 참조할 값을 설정합니다.

지원 입력 타입은 다음과 같습니다.

| 타입                      | 설명                |
| ----------------------- | ----------------- |
| 문자열 (string)            | 텍스트 값             |
| 숫자 (number)             | 정수 또는 소수          |
| 객체 (object)             | JSON 형태의 구조화된 데이터 |
| 문자열 배열 (array\[string]) | 문자열 목록            |
| 숫자 배열 (array\[number])  | 숫자 목록             |
| 객체 배열 (array\[object])  | 구조화된 데이터 목록       |

#### 프로그래밍 언어

코드 편집기 왼쪽 상단에서 **Python 3** 또는 **JavaScript**를 선택합니다.\
언어를 변경하면 해당 언어의 기본 템플릿으로 초기화됩니다.

#### 코드 작성

코드 편집기에 처리 로직을 작성합니다.\
다음 형식을 따라야 합니다.

* `main` 함수를 정의합니다.
* 입력 변수를 매개변수로 받습니다.
* 처리 결과를 객체 형태로 반환합니다.
* 반환 키는 출력 변수 이름과 같아야 합니다.

두 숫자를 곱해 결과를 반환하는 예시입니다.

```python
# Python
def main(price: int, quantity: int) -> dict:
    return {
        "total": price * quantity,
    }
```

```javascript
// JavaScript
function main({ price, quantity }) {
    return {
        total: price * quantity
    }
}
```

{% hint style="info" %}
**코드 자동 생성**

미소 AI 자동 생성으로 코드 작성을 시작할 수 있습니다.\
원하는 처리를 자연어로 설명하면 지원 형식에 맞는 코드를 생성합니다.
{% endhint %}

코드는 안전한 샌드박스 환경에서 실행합니다.

#### 출력 변수

반환할 결과의 이름과 타입을 정의합니다.\
**추가**를 선택해 출력 변수를 추가합니다.

| 출력 타입                   | 설명               |
| ----------------------- | ---------------- |
| 문자열 (string)            | 문자열 결과           |
| 숫자 (number)             | 정수 또는 소수         |
| 객체 (object)             | JSON 형태의 구조화된 결과 |
| 문자열 배열 (array\[string]) | 문자열 목록           |
| 숫자 배열 (array\[number])  | 숫자 목록            |
| 객체 배열 (array\[object])  | 구조화된 데이터 목록      |

반환값이 정의한 타입과 다르면 오류가 발생합니다.\
예를 들어 숫자 타입에 문자열을 반환하면 실패합니다.

### 실행 제한

코드는 안전한 샌드박스 환경에서 실행합니다.\
다음 제한이 적용됩니다.

| 항목         | 제한값       |
| ---------- | --------- |
| 실행 시간      | 최대 60초    |
| 문자열 배열 크기  | 최대 100개   |
| 숫자 배열 크기   | 최대 1,000개 |
| 객체 배열 크기   | 최대 100개   |
| 객체 중첩 깊이   | 최대 5단계    |
| 숫자 소수점 자릿수 | 최대 20자리   |

제한을 초과하면 오류가 발생합니다.\
필요한 데이터만 반환하세요.

### 활용 예시

#### 문자열을 배열로 변환

**사용 시점**: 쉼표로 구분한 텍스트를 배열로 변환합니다.

* **입력 변수**: `tags`(문자열) - 예: `"마케팅, 디자인, 개발"`
* **출력 변수**: `tag_list`(문자열 배열)

```python
def main(tags: str) -> dict:
    tag_list = [t.strip() for t in tags.split(",") if t.strip()]
    return {
        "tag_list": tag_list,
    }
```

**결과**: `["마케팅", "디자인", "개발"]`을 반복 노드에서 처리합니다.

#### 외부 API 호출

**사용 시점**: 외부 서비스 API에서 데이터를 가져옵니다.

* **입력 변수**: `keyword`(문자열)
* **출력 변수**: `result`(객체)
* **의존성 패키지**: `requests`

```python
import requests

def main(keyword: str) -> dict:
    response = requests.get(
        "https://api.example.com/search",
        params={"q": keyword},
        timeout=10,
    )
    return {
        "result": response.json(),
    }
```

#### LLM JSON 출력 분리

**사용 시점**: LLM이 생성한 JSON에서 각 값을 별도 변수로 분리합니다.

* **입력 변수**: `llm_output`(문자열) - 예: `'{"summary": "...", "category": "기술", "keywords": ["AI", "자동화"]}'`
* **출력 변수**: `summary`(문자열), `category`(문자열), `keywords`(문자열 배열)

```python
import json

def main(llm_output: str) -> dict:
    parsed = json.loads(llm_output)
    return {
        "summary": parsed["summary"],
        "category": parsed["category"],
        "keywords": parsed["keywords"],
    }
```

**결과**: JSON 값을 개별 변수로 분리해 이후 노드에서 사용합니다.
