# AWS RDS

#### 도구 활성화

* RDS 접근 가능한 DB 사용자 계정과 DB 사용자 비밀번호를 입력합니다.

<figure><img src="../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>



#### 앱에서 활용

* 입력 변수
  * **Query**: AWS RDS 서버에 전송하는 SQL 정보 입력
* 도구 설정
  * **DB 유형**: RDS의 DB 유형을 설정( MySQL과 PostgreSQL 중 택 1)
  * DB Host: 데이터베이스 서버 Host 정보 입력
  * DB Port: 데이터베이스 서버 Port 정보 입력
  * DB Name: 데이터베이스 서버 이름 정보 입력

<figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

#### &#x20;출력 결과

* 기본적으로 text 형태로 응답합니다. LLM의 프롬프트나 코드 등 다른 노드를 이용하여 사용합니다.

<figure><img src="../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>



추후 JSON 배열 형태의 출력도 제공 예정에 있습니다.
