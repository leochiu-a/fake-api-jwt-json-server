# JSONServer + JWT Auth

一個假的 REST API，使用 json-server，並且有 JWT 驗證的功能。

## Install

```bash
yarn
yarn start-auth
```

## How to login/register?

以下為註冊與登入的 endpoints:

```
POST http://localhost:8000/auth/login
POST http://localhost:8000/auth/register
```

在註冊與登入時，使用以下格式的資料:

```
{
  "email": "nilson@email.com",
  "password":"nilson"
}
```

在註冊或登入成功後，API 會反回一組 `access_token`:

```
{
   "access_token": "<ACCESS_TOKEN>"
}
```

在請求 `/products` 資料時，必須在 header 加入以下資訊才能通過 JWT 驗證:

```
Authorization: Bearer <ACCESS_TOKEN>
```
