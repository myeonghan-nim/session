# session

## 세션

세션은 서버-클라이언트 환경에서 클라이언트와 서버 간의 통신 상태를 유지하기 위한 정보 저장 단위를 의미.
일반적으로 클라이언트와 서버는 HTTP 프로토콜을 사용해서 통신하는데 HTTP는 기본적으로 무상태(stateless) 프로토콜로 클라이언트의 요청과 요청 사이에 서버가 그 상태를 저장하지 않음.
그러나 사용자 인증, 장바구니 유지 같은 기능을 위해서 클라이언트의 상태를 유지해야 할 때 세션을 사용.

## 세션의 주요 특징

1. 클라이언트와 서버 간 상태 유지: 세션은 서버가 클라이언트와 상호작용 상태를 기억(예시, 사용자가 로그인하면 그 세션 안에서 로그인 상태가 유지).
2. 서버에 데이터 저장: 세션 데이터는 보통 서버 측에 저장되고 클라이언트는 세션 식별자(Session ID)만 가지고 있고 이를 통해 서버에서 저장된 데이터를 참조.
3. 세션 ID: 클라이언트와 서버 간 요청이 오갈 때 세션을 구분하기 위해 사용되는 고유 값으로 보통 쿠키에 저장되거나 URL에 포함되서 전달.
4. 수명: 세션은 일반적으로 유효 기간이 있어서 클라이언트가 지정된 시간 동안 서버와 상호작용하지 않으면 만료.

## 세션이 사용되는 예시

1. 로그인 상태 유지: 사용자가 로그인하면 서버는 사용자 정보를 세션에 저장하고 클라이언트는 세션 ID를 통해 서버의 데이터를 참조.
2. 장바구니 기능: 사용자가 장바구니에 상품을 추가할 때 해당 데이터는 세션에 저장돼서 다른 페이지를 방문해도 유지.
3. 사용자 환경 설정: 사용자가 다크 모드나 특정 레이아웃을 선택했다면 세션을 통해 이런 설정을 기억.

## 세션과 쿠키의 차이

- 세션(Session): 서버에 데이터를 저장하고 클라이언트는 세션 ID만 소유.
- 쿠키(Cookie): 데이터를 클라이언트의 브라우저에 저장하여 클라이언트가 데이터를 소유.

다만, 둘은 함께 사용되는 경우가 많음(예시, 세션 ID를 쿠키에 저장해서 클라이언트와 서버가 통신할 때 세션을 식별)
