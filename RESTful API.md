# RESTful API 에서의 CRUD
- RESTful API 에서 CRUD 는 Create, Read, Update, Delete의 약자로, 데이터 조작 작업을 나타냅니다.
이를 HTTP 메서드와 함께 사용하는 방식으로 RESTful API에서 구현됩니다.
<br>

## Create (생성)
- HTTP Method: Post
- 설명: 새로운 리소스를 생성할 때 사용합니다. 예를 들어, 새로운 사용자 데이터를 생성할 때, 클라이언트가 서버로 POST 요청을 보내고, 서버는 해당 데이터를 데이터베이스에 저장합니다.
- 예시:

```
POST /users
{
  "name": "Eren",
  "email": "eren@example.com"
}
```
<br>

## Read (조회)
- HTTP Method: Get
- 설명: 리소스를 조회할 때 사용합니다. 서버에서 데이터나 정보를 읽어올 때 사용되며, 이 요청은 데이터베이스의 상태를 변경하지 않습니다.
- 예시:

```
Get /users/123
```
<br>

## Update (수정)
- HTTP Method: Put(전체 업데이트), PATCH(부분 업데이트)
- 설명: 기존 리소스를 수정할 때 사용합니다. PUT은 리소스를 전체적으로 업데이트하고, PATCH는 부분적으로 업데이트 합니다.
- 예시 (PUT):

```
PUT /users/123
{
  "name": "Eren",
  "email": "eren@example.com"
}
```
- 예시 (PATCH):

```
PATCH / users/123
{
  "email": "eren@example.com"
}
```
<br>

## Delete (삭제)
- HTTP Method: Delete
- 설명: 리소스를 삭제할 때 사용합니다. 서버에서 해당 리소스를 제거하는 요청을 보냅니다.
- 예시:

```
DELETE /users/123
```
<br>

## 요약
- RESTful API에서 CRUD는 HTTP 메서드를 통해 직관적이고 일관성 있게 데이터를 처리할 수 있게 해줍니다.
