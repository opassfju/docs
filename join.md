# Join

## 使用者註冊

```
POST /join
```

Auth : Not Required.

### Input

| Key | Type | Description |
| --- | --- | --- |
| `email` | email | 必須是輔大信箱才能註冊(@mail.fju.edu.tw) |
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
  "message": "ok"
}
```