---
description: 발행한 웹사이트의 방문 통계와 성능 지표를 확인하는 대시보드입니다.
---

# 웹사이트 사용 현황 대시보드

<figure><img src="../../../.gitbook/assets/image (828).png" alt=""><figcaption></figcaption></figure>

발행한 웹사이트의 방문 통계와 성능 지표를 확인합니다.

웹사이트 앱에서 **사용 현황** 아이콘을 선택하세요.

### 대시보드 탭

<figure><img src="../../../.gitbook/assets/image (842).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="150.34765625">탭</th><th width="442.17578125">설명</th></tr></thead><tbody><tr><td><strong>사용현황 모니터링</strong></td><td>방문자 수, 세션, 페이지뷰 등 핵심 지표를 시각화합니다.</td></tr><tr><td><strong>로그</strong></td><td>일별 API 호출, 페이지뷰, 응답 시간 등 상세 로그를 확인합니다.</td></tr><tr><td><strong>개발 로그</strong></td><td>빌드 및 배포 과정의 작업 이력을 확인합니다.</td></tr></tbody></table>

#### 날짜 범위

오른쪽 상단의 **날짜 범위**에서 조회 기간을 설정합니다. 기본값은 최근 7일입니다.

### 사용 현황 모니터링

웹사이트의 핵심 사용 지표를 확인합니다.

<figure><img src="../../../.gitbook/assets/image (830).png" alt=""><figcaption></figcaption></figure>

#### 개요 지표

<table><thead><tr><th width="210.73046875">지표</th><th width="343.7564697265625">설명</th></tr></thead><tbody><tr><td><strong>페이지 뷰</strong></td><td>선택 기간 내 총 페이지 뷰 수</td></tr><tr><td><strong>순 방문자</strong></td><td>선택 기간의 고유 방문자 수</td></tr><tr><td><strong>API 호출</strong></td><td>선택 기간의 총 API 호출 수</td></tr><tr><td><strong>오류율</strong></td><td>API 호출 중 오류가 발생한 비율</td></tr><tr><td><strong>운영크레딧(기간)</strong></td><td>선택 기간 내 운영 크레딧 (일수 x 30)</td></tr><tr><td><strong>운영일수</strong></td><td>선택 기간 내 운영일수</td></tr><tr><td><strong>누적 호스팅 크레딧 (전체)</strong></td><td>총 운영 크레딧</td></tr></tbody></table>

#### 차트와 표

<table><thead><tr><th width="247.22784423828125">차트 또는 표</th><th width="133.13671875">유형</th><th width="339.37109375">설명</th></tr></thead><tbody><tr><td><strong>일별 운영 크레딧</strong></td><td>꺾은선 그래프</td><td>일별 운영 크레딧을 표시합니다.</td></tr><tr><td><strong>일별 API 호출 · 오류 추이</strong></td><td>꺾은선 그래프</td><td>API 호출과 오류 추이를 표시합니다.</td></tr><tr><td><strong>API 응답 시간 P50/P95</strong></td><td>꺾은선 그래프</td><td>P50과 P95 응답 시간을 표시합니다.</td></tr><tr><td><strong>일별 페이지 뷰 · 순 방문자 추이</strong></td><td>꺾은선 그래프</td><td>페이지 뷰와 순 방문자 추이를 표시합니다.</td></tr><tr><td><strong>DAU / MAU 추이</strong></td><td>꺾은선 그래프</td><td>일간 및 월간 활성 사용자 추이를 표시합니다.</td></tr><tr><td><strong>시간대별 트래픽 분포</strong></td><td>막대 그래프</td><td>시간대별 방문 트래픽을 표시합니다.</td></tr><tr><td><strong>인기 페이지 TOP 20</strong></td><td>표</td><td>방문이 많은 페이지를 표시합니다.</td></tr><tr><td><strong>유입 경로 TOP 20</strong></td><td>표</td><td>주요 유입 경로를 표시합니다.</td></tr></tbody></table>

{% hint style="info" %}
**P50**은 전체 요청의 50%가 처리되는 시간입니다. 일반적인 응답 속도를 나타냅니다.

**P95**는 전체 요청의 95%가 처리되는 시간입니다. 높은 부하에서의 응답 지연을 파악할 수 있습니다.
{% endhint %}

### 로그

일별 API 호출, 페이지뷰, 응답 시간 등 상세 운영 데이터를 확인합니다.

<figure><img src="../../../.gitbook/assets/image (829).png" alt=""><figcaption></figcaption></figure>

### 개발 로그

웹사이트 제작 과정의 대화와 AI 작업 이력을 확인합니다.

<figure><img src="../../../.gitbook/assets/image (831).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="210.73046875">항목</th><th width="457.08984375">설명</th></tr></thead><tbody><tr><td><strong>에이전트 세션</strong></td><td>세션 기본 정보와 총 토큰, 크레딧 사용량을 확인합니다.</td></tr><tr><td><strong>대화 로그</strong></td><td>사용자와 AI의 대화 이력을 확인합니다.</td></tr><tr><td><strong>런타임 상태</strong></td><td>작업의 런타임 상태를 확인합니다.</td></tr><tr><td><strong>런타임 테이블</strong></td><td>작업의 런타임 정보를 확인합니다.</td></tr></tbody></table>

{% hint style="info" %}
런타임은 프로그램이 실행되어 동작하는 상태입니다.
{% endhint %}

{% hint style="info" %}
대시보드 데이터는 퍼스트파티 분석으로 수집합니다.

외부 분석 도구 없이 방문자 행동을 분석합니다. 개인정보(PII)는 저장하지 않습니다.
{% endhint %}
