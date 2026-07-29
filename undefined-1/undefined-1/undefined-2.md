# 뉴스 스크래핑 워크플로우

<figure><img src="../../.gitbook/assets/image (721).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" icon="bell-ring" %}
**\[Must Do!]**

* [ ] &#x20;네이버 뉴스 도구 세팅 : 내장 도구 활용을 위한 세팅이 꼭 필요합니다.
{% endhint %}



### 0. Overview

특정 키워드와 관련된 뉴스 기사를 검색하는 앱입니다.

1. 여러 개의 키워드를 동시에 검색할 수 있습니다.
2. 기본으로 검색에 포함할 키워드를 사전에 설정할 수 있습니다.
3. `네이버 뉴스 검색` 도구를 활용하여 검색을 진행합니다.
4. 템플릿은 **파르나스 호텔**에 적용된 예시입니다. 1) 기본 키워드 세팅, 2) 프롬프트 내 카테고리 구분, 3) 프롬프트 내 요약/분석 방향성 등을 통해 앱 활용 예시를 이해해볼 수 있습니다.



작업 흐름을 명시적으로 구성하기 위해 워크플로우 방식으로 앱을 제작합니다.

{% hint style="info" %}
워크플로우에 관한 설명은 아래의 매뉴얼 문서를 참고합니다.

[workflow](../../manual/workflow/ "mention")
{% endhint %}

\
**에이전트 VS 워크플로우**

<table><thead><tr><th width="161.296875">특징</th><th>에이전트</th><th>워크플로우</th></tr></thead><tbody><tr><td>동작 방식</td><td>LLM이 상황에 따라 스스로 판단해 행동하는 자율성 존재</td><td>미리 설계된 순서대로만 순차적 진행</td></tr><tr><td>도구/지식 활용</td><td>LLM이 필요시 자율적으로 호출하여 활용</td><td>설계 시 노드에서 명시적으로 활용</td></tr><tr><td>적합한 작업</td><td><ul><li>비정형 질의가 잦은 경우</li><li>AI의 상황 판단 능력이 필요한 경우</li></ul></td><td><ul><li>정형화된 반복 작업</li><li>자동화 파이프라인 설계</li></ul></td></tr></tbody></table>

### 1. 뉴스 스크랩핑 노드 구조

<table><thead><tr><th width="166.09375">노드명</th><th width="308.60546875">기능</th><th width="83.9609375">검토<select><option value="p0wmfzH05Gpb" label="권장" color="blue"></option><option value="4De9UJ8TP1ow" label="필수" color="blue"></option></select></th><th>비고</th></tr></thead><tbody><tr><td>시작</td><td>사용자의 키워드 입력을 받는다.</td><td></td><td></td></tr><tr><td>키워드 설정</td><td>사전 설정 키워드를 설정한다</td><td><span data-option="p0wmfzH05Gpb">권장</span></td><td></td></tr><tr><td>입력값 전처리</td><td>API 입력 인자 형태로 바꿔준다.</td><td></td><td></td></tr><tr><td>반복</td><td>(아래 작업을 병렬 처리해줌)</td><td></td><td></td></tr><tr><td>ㄴ 네이버 뉴스 검색</td><td>ㄴ 키워드를 가지고 네이버 뉴스 검색을 진행한다</td><td><span data-option="4De9UJ8TP1ow">필수</span></td><td>네이버 검색 API 설정이 필요합니다</td></tr><tr><td>중복 제거</td><td>검색된 뉴스 기사 중 중복을 제거한다</td><td></td><td></td></tr><tr><td>뉴스 분석/요약 LLM</td><td>사용자가 원하는 방식으로 뉴스 검색 결과를 요약/분석 한다</td><td><span data-option="p0wmfzH05Gpb">권장</span></td><td></td></tr><tr><td>종료</td><td>결과물을 반환한다</td><td></td><td></td></tr></tbody></table>

### 2. 노드 자세히 들여다보기

<figure><img src="../../.gitbook/assets/image (722).png" alt=""><figcaption></figcaption></figure>

각 노드별 설명은 아래와 같습니다.



#### **a. 시작**

사용자가 입력한 키워드를 `keyword` 변수에 저장합니다

#### **b. 키워드 설정**

<div align="left"><figure><img src="../../.gitbook/assets/image (723).png" alt="" width="563"><figcaption></figcaption></figure></div>

노드 내에 템플릿 변수를 활용하여 뉴스 검색 시에 포함할 키워드를 사전에 설정해놓을 수 있습니다.

{% hint style="info" %}
`{{ keyword }}` 에는 **\[시작]** 노드에서 받은 `keyword` 변수가 들어가게 됩니다. **고로 삭제하시면 안됩니다!**

→ 1) 사전 설정한 키워드, 2) 사용자가 추가로 입력한 키워드 를 대상으로 뉴스 검색을 시작합니다.
{% endhint %}

#### **c. 입력값 전처리**

네이버 뉴스 검색 노드에서 요구하는 입력값의 형태로 변환하기 위해 코드 블록을 활용합니다.

{% hint style="info" %}
**코드 블럭을 활용하는 이유?**

정형화된 작업은 LLM 노드를 통해 처리하는 것보다 코드를 통해 처리했을 때 시간과 비용 측면에서 이점이 큽니다.

하고자 하는 작업의 복잡성과, 고정성을 고려해서 코드블럭을 활용하시는 것을 추천드립니다 🙂
{% endhint %}

#### **d. 반복**

{% hint style="info" %}
`반복` 노드에 대한 자세한 설명은 다음 문서를 참조해주세요.

[iteration.md](../../manual/workflow/node-definition/undefined-2/iteration.md "mention")
{% endhint %}

키워드 목록을 전달 받아 `네이버 뉴스 검색` 도구를 반복 활용하여 검색을 진행합니다.

이때, 시간 단축을 위해 **병렬적으로** 검색을 진행합니다.

현재는 병렬 모드 값이 10으로 설정되어 있기 때문에, 한번에 10개씩 키워드 검색이 이뤄지게 됩니다.

<figure><img src="../../.gitbook/assets/image (724).png" alt=""><figcaption></figcaption></figure>

<details>

<summary>Q: 반복 노드 속에서 작동할 노드 추가하는 법?</summary>

일반적으로 노드를 추가할 때는 마우스 우클릭에서 나오는 토글 중 `노드 추가`를 활용하지만, \
반복 노드에서는 `+ 버튼`을 활용해서 추가해야 합니다.

<figure><img src="../../.gitbook/assets/image (725).png" alt=""><figcaption></figcaption></figure>

</details>



**d-1. 네이버 뉴스 검색**

{% hint style="info" %}
✅ `네이버 뉴스 도구`를 활용하기 위해서는 [네이버 개발자 센터](https://developers.naver.com/apps/#/register)에서 API 발급이 최초 1회 필요합니다.
{% endhint %}

<details>

<summary>API 발급 방법</summary>

1.  **애플리케이션 등록**

    <figure><img src="../../.gitbook/assets/image (726).png" alt=""><figcaption></figcaption></figure>

    네이버 아이디로 로그인 한 뒤, **애플리케이션 등록**을 진행해줍니다.

    \
    **사용 API**는 `검색` 을 선택해주시고,

    **비로그인 오픈 API 서비스 환경**의 경우 저희는 WEB에서 활용하기 때문에 `WEB 설정`을 선택한 뒤, \
    URL은 [**http://naver.com**](http://naver.com) 으로 등록합니다.<br>
2.  **API 정보 확인하기**

    <figure><img src="../../.gitbook/assets/image (727).png" alt=""><figcaption></figcaption></figure>

    이후 내 애플리케이션 화면에서 애플리케이션 정보 섹션의 `Client ID` 와 `Client Secret` 값을 확인합니다.

</details>

<details>

<summary>네이버 뉴스 도구 활성화 방법</summary>

도구 활성화 이전에는 앱 화면에서 아래와 같이 오류 메시지가 뜨는 것을 확인할 수 있습니다.

<div align="left"><figure><img src="../../.gitbook/assets/image (728).png" alt="" width="563"><figcaption></figcaption></figure></div>



네이버 뉴스 검색 도구를 클릭해줍니다.

<figure><img src="../../.gitbook/assets/image (729).png" alt=""><figcaption></figcaption></figure>

위 사진처럼 `인증 추가`가 뜨는 것을 확인할 수 있습니다.

인증 추가 버튼을 누르면 아래처럼 인증 설정 창이 뜹니다.

<div align="left"><figure><img src="../../.gitbook/assets/image (730).png" alt="" width="563"><figcaption></figcaption></figure></div>

아까 네이버 개발자 센터에서 발급받았던 `Client ID`와 `Client Secret` 정보를 기입해주고 저장해주면 도구 활성화가 완료됩니다!

</details>

<figure><img src="../../.gitbook/assets/image (731).png" alt=""><figcaption></figcaption></figure>

네이버 뉴스 도구의 **검색어**는 위 사진 처럼 `반복 노드의 item` 으로 설정합니다.

이는 우리가 설정한 여러개의 키워드를 병렬적으로 검색할 수 있도록 _키워드 1개씩 나누어서_ 네이버 뉴스 검색 도구에 전달해준다는 것을 의미합니다.

<figure><img src="../../.gitbook/assets/image (733).png" alt=""><figcaption></figcaption></figure>

#### **e. 중복 제거**

검색된 뉴스 결과물 중에서 중복된 기사는 코드 블럭을 통해서 제거해줍니다.

#### **f. 뉴스 분석/요약 LLM**

여기까지 처리된 데이터는 JSON 형식으로, 뉴스 기사 원본 내용이 컴퓨터 친화적인 언어로 적혀져 있는 상태입니다.

이제 LLM 노드를 활용해서 사용자가 원하는 형식으로 변환하고, 내용을 분석하는 과정을 거칩니다.



현재 템플릿 LLM 노드에 기본 값으로 쓰여진 프롬프트의 핵심 작업 내용은 다음과 같습니다.

```jsx
<Task>
입력된 네이버 뉴스 검색 결과 JSON 데이터를 처리하여 다음을 수행합니다:
1. 중복 뉴스 제거 (동일 URL, 제목 유사도 80% 이상, 동일 사건)
2. 카테고리 분류 (parnas, competitor, industry)
3. 각 뉴스 요약 생성 (2~3문장)
4. 키워드 추출 (3~5개)
5. 인사이트 도출
```

입력으로 들어온 네이버 뉴스 검색 결과를 LLM에게 그대로 전달한 뒤, 원하는 방식으로 가공하여 핵심 내용을 뽑아내어 결과물로 전달할 수 있습니다.

→ _**프롬프트 수정을 통해서 원하는 요약 방식, 출력 방식 등은 자유롭게 변경할 수 있습니다.**_



{% hint style="warning" icon="triangle-exclamation" %}
**\[프롬프트 수정 시 유의사항]**

가끔, 프롬프트를 수정한 이후에 결과가 예상치 못하게 나오는 경우가 있습니다.

뉴스 스크랩핑 앱의 경우를 예시로 보자면, 프롬프트 수정 과정에서 Date\_Filter\_Rule 영역이 최근 1주일 내의 기사만 추려내는 역할을 하게 수정됐습니다.

키워드마다 최근 기사가 없을 수도 있기에 결과가 아래처럼 빈 값으로 나올 수 있는 것입니다.

<img src="../../.gitbook/assets/image (734).png" alt="" data-size="original"><br>

그렇기에 프롬프트는 작성 이후, 본인이 의도하지 않은 실행 조건이 첨가되지 않았는지 검토하는 습관이 꼭 필요합니다.
{% endhint %}



### 3. 최종 사용자들이 보는 화면

#### 1. 질문

사용자가 검색하고자 하는 키워드를 쉼표로 구분하여 입력합니다.

<figure><img src="../../.gitbook/assets/image (735).png" alt=""><figcaption></figcaption></figure>

#### **2. 답변**

<figure><img src="../../.gitbook/assets/image (736).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (737).png" alt=""><figcaption></figcaption></figure>

프롬프트에 설정한 것 처럼 각 기사의 내용 요약과, 하단에는 기사에서 알아낼 수 있는 인사이트를 정리해서 반환하는 것을 알 수 있습니다.
