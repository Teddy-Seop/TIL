# HTTP Status Code
------------
## 100 ~ 199 : 정보 확인
|상태코드|이름|의미|
|---|---|---|
|100|Continue|요청의 시작 부분 일부가 받아들여졌으며 클라이언트는 나머지를 계속 이어서 보내야함을 의미|
|101|Switcing Protocol|요청자가 서버에 프로토콜 전환을 요청했으며 서버에서 이를 승인하는 중을 의미|

## 200 ~ 299 : 통신 성공
|상태코드|이름|의미|
|---|---|---|
|200|OK|요청 성공(GET)|
|201|Create|생성 성공(POST)|
|202|Accepted|요청 접수했지만 아직 처리하지 않음|
|204|No Content|요청 성공, 돌려줄 `resource`없음|
|206|Partial Content|지정된 범위만큼 요청 성공|

## 300 ~ 399 : 리다이렉트
|상태코드|이름|의미|
|---|---|---|
|300|Multiple Chice|요청 URI에 리소스와 함께 리턴|
|301|Permanently Move|요청된 리소스가 영구적으로 새로운 URI로 이동|
|302|Temporarily Move|요청된 리소스가 임시적으로 새로운 URI로 이동|
|304|Not Modified|요청된 리소스를 재전송할 필요 없음|

#### 301/302의 차이
- 검색엔진이 크롤링하는 페이지의 차이
- ex) A페이지에서 B페이지로 리다이렉트 될 때 `301`은 B페이지의 대한 수집을 하고 `302`는 A페이지에 대해서 수집

## 400 ~ 499 : 클라이언트 오류
|상태코드|이름|의미|
|---|---|---|
|400|Bad Request|클라이언트가 올바르지 못한 요청을 보냄|
|401|Unauthorized|인증 오류|
|403|Forbidden|권한 오류|
|404|Not Found|요청 URI가 존재하지 않음|
|405|Method Not Allowed|잘못된 Method 호출|
|406|Not Acceptable|요청에 대한 적절한 컨텐츠가 없음|
|408|Request Timeout|요청 대기시간 초과|
|409|Conflict|요청에 대한 충돌 발생|

#### 401/403 차이
- `401`은 허가되지 않음을 의미
- '403'은 금지됨을 의미
- ex) `401`은 익명의 사용자, `403`은 로그인은 했으나 권한이 없는 사용자

## 500 ~ 599 : 서버 오류
|상태코드|이름|의미|
|---|---|---|
|500|Internal Server Error|서버 내부 오류|
|501|Not Implemented|서버가 지원하지 않는 Method를 사용하여 요청|
|502|Bad Gateway|게이트웨이 오류|
|503|Service Unvaliable|서비스 이용 불가|
|504|Gateway Timeout|게이트웨이 시간 초과|
