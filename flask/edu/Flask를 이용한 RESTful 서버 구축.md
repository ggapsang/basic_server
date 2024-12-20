## 왜 Flask 같은 프레임워크를 배워야 하는가

- 기본 HTTP 서버에서는 모든 요청을 단순히 하나의 GET 메서드에서 처리해야 한다. 하지만 Flask에서는 URL 경로마다 별도의 함수를 지정할 수 있다

- Flask에서는 `@app.route` 데코레이터를 통해 **GET, POST, PUT, DELETE** 같은 여러 HTTP 메서드를 쉽게 처리할 수 있다
	- 예를 들어, 클라이언트가 데이터를 추가하려면 `POST` 요청을, 데이터를 업데이트하려면 `PUT` 요청을 보내는 식으로 처리하게 된다. **Flask는 각 메서드별로 코드를 분리**해 구현할 수 있어 요청별로 분기 처리할 필요가 줄어든다.
 - **폼 데이터와 JSON 데이터를 쉽게 처리**
	 - 기본 HTTP 서버에서는 클라이언트에서 보내는 JSON 데이터나 폼 데이터를 **수작업으로 처리해야 하는 번거로움**이 있다.
	- Flask는 **요청 데이터를 자동으로 분석**해주며, `request.form`, `request.json` 등으로 데이터를 쉽게 가져올 수 있다.
- **에러 핸들링과 응답 커스터마이징이 간편**
	- 기본 HTTP 서버에서는 모든 에러나 예외를 직접 처리해야 하지만, Flask는 404 Not Found, 500 Internal Server Error 등의 에러를 **자동으로 관리**해준다. 필요한 경우 이를 커스터마이징하기도 쉬워진다.
	- 또한 응답을 JSON 형태나 HTML 형태로 손쉽게 커스터마이징할 수 있다.
- **확장성과 플러그인 기능**
	- -Flask는 데이터베이스 연동, 인증, 세션 관리 같은 기능을 플러그인이나 라이브러리를 통해 쉽게 추가할 수 있다.
	- 프로젝트가 복잡해질수록 Flask 같은 프레임워크를 사용하는 것이 효율적이다