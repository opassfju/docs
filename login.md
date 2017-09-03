# Login

## 使用者登入

```
POST /login
```

Auth : Not Required.

### Input

| Key | Type | Description |
| --- | --- | --- |
| `email` | email | 必須是輔大信箱(@mail.fju.edu.tw) |
| `password` | string | 使用者密碼 |

### Sample input

```json
{
  "email": "404111111@mail.fju.edu.tw",
  "password": "1234asdf"
}
```

### Response

```json
{
  "token":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  "roles": [
  {
    "name": "fudaer"
  }
  ]
}
```