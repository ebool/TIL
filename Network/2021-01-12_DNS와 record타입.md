aws를 할때 매번 보던 내용인데, 그럴때마다 그냥 대충 지나갔다.  
이번 TIL을 하면서 한번 정리해 본다.  
 
## DNS
Domain name system.  
모든 웹사이트의 주소는 ip로 이루어져 있다.  
컴퓨터들은 문제가 없겠으나 인간은 ip를 외우기 힘들지.. 그래서 나온게 DNS

|ip|domain|
|---|---|
|12.123.123.132|xangle.io|
|23.143.82.122|coinjab.com|
|123.133.182.21|coinjab.com|

DNS서버는 문자열과 ip주소 쌍을 저장했다가 요청으로 온 문자열에 맞는 ip를 리턴해준다.  

이 테이블의 저장된 하나의 행을 Record라고 부른다.
이 Record의 저장 타입에 따라 A Record와 CAME으로 구분한다.

사실 레코드 타입의 종류는 엄청 많다. 자세한건 [여기](https://en.wikipedia.org/wiki/List_of_DNS_record_types)  

## A Record
도메인 주소와 ip가 직접 매핑된 타입이다.

## CNAME
Canonical Name.
도메인 주소를 또 다른 도메인 주소로 매핑 시킨다.

---
다음은 예시이다.

|name|type|value
|---|---|---|
|dev.coinjab.com|CNAME|coinjab.com
|coinjab.com|A|23.143.82.122



