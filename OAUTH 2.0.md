## OAuth 2.0(Open Authorization 2.0, OAuth2)

- 인증을 위한 개방형 표준 프로토콜
- 이 프로토콜에서는 Third-Party 프로그램에게 리소스 소유자를 대신하여 리소스 서버에서 제공하는 자원에 대한 접근 권한을 위임하는 방식을 제공
- 구글, 페이스북, 카카오, 네이버 등에서 제공하는 간편 로그인 기능도 OAuth2 프로토콜 기반의 사용자 인증 기능을 제공

### 1. OAuth 2.0 주요 용어

|용어|설명|
|--|--|
|Authentication|인증, 접근 자격이 있는지 검증하는 단계|
|Authorization|인가, 자원에 접근할 권한을 부여. 인가가 완료되면 리소스 접근 권한이 담긴 Access Token이 클라이언트에게 부여|
|Access Token|리소스 서버에게서 리소스 소유자의 보호된 자원을 획득할 때 사용되는 만료 기간이 있는 Token|
|Refresh Token|Access Token 만료시 이를 갱신하기 위한 용도로 사용하는 Token. Refresh Token은 일반적으로 Access Token보다 만료 기간이 길다|

### 2. OAuth 2.0의 4가지 역할

|역할|설명|
|--|--|
|Resource Owner|리소스 소유자 또는 사용자. 보호된 자원에 접근할 수 있는 자격을 부여해 주는 주체. OAuth2 프로토콜 흐름에서 클라이언트를 인증(Authorize)하는 역할을 수행. 인증이 완료되면 권한 획득 자격(Authorization Grant)을 클라이언트에게 부여. 개념적으로는 리소스 소유자가 자격을 부여하는 것이지만 일반적으로 권한 서버가 리소스 소유자와 클라이언트 사이에서 중개 역할을 수행.|
|Client|보호된 자원을 사용하려고 접근 요청을 하는 애플리케이션|
|Resource Server|사용자의 보호된 자원을 호스팅하는 서버|
|Authorization Server|권한 서버. 인증/인가를 수행하는 서버로 클라이언트의 접근 자격을 확인하고 Access Token을 발급하여 권한을 부여하는 역할을 수행


![image](https://user-images.githubusercontent.com/98144690/167751967-efcdfafd-28c6-458d-ba4f-7ee4f4eb99f0.png)
<이미지 출처 : https://minholee93.tistory.com/entry/OAuth20-OAuth20-%EA%B0%9C%EC%9A%94>

권한 부여 방식은 출처 블로그 참조
<츌처 : https://blog.naver.com/mds_datasecurity/22218294354>
