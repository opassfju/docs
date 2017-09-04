# Fudaer 使用者相關 API

- 確認認證信件 | [Confirm Verification](#confirm-verification)
- 重新請求認證信件 | [Request Confirm Verification](#request-confirm-verification)
- 請求忘記/重設 密碼 | [Request Reset Password](#request-reset-password)
- 重設密碼 | [Reset Password](#reset-password)
- 取得使用者資訊 | [Get User Info](#get-user-info)
- 更新使用者資訊 | [Update User Info](#update-user-info)

## Confirm Verification

### 確認認證信件

```
GET /fudaers/:id/confirm_verification/:token
```

Auth : Not Required.

### Response

```json
{
  "message": "ok"
}
```

## Request Confirm Verification

### 重新請求認證信件

```
GET /fudaers/:id/request_verification
```

Auth : Not Required.

### Response

寄送認證信件至使用者信箱並回傳以下訊息

```json
{
  "message": "ok"
}
```

## Request Reset Password

### 請求忘記/重設 密碼

```
GET /fudaers/:id/request_reset_password
```

Auth : Not Required.

### Response

寄送認證信件至使用者信箱並回傳以下訊息

```json
{
  "message": "ok"
}
```

## Reset Password

### 重新設定密碼

```
POST /fudaer/reset_password
```

Auth : Required ( reset password token)


### Input

| Key | Type | Description |
| --- | --- | --- |
| `new_password` | string | 使用者新密碼 |

### Sample input

```json
{
  "new_password": "1234asdf"
}
```

### Response

```json
{
  "message": "ok"
}
```

## Get User Info

### 使用者資訊

```
GET /fudaer
```

Auth : Required ( login token)

### Response Sample

```json
{
  "email": "404111111@mail.fju.edu.tw",
  "department": "企業管理學系",
  "nickname": "新鮮小大一",
  "section": "日間部",
  "sec_major": "哲學系",
  "miner": "金融與國際企業學系",
  "program": "動態資訊視覺設計學分學程"
}
```

## Update User Info

### 更新使用者資訊

```
PATCH /fudaer
```

Auth : Required ( login token)

### Input

| Key | Type | Description |
| --- | --- | --- |
| `department` | string | 主修系所 |
| `section` | string | 部別 |
| `sec_major` | string | 第二主修系所 |
| `miner` | string | 副修 |
| `program` | string | 學程 |

### Sample input

```json
{
  "department": "0E",
  "section": "D",
  "sec_major": "03",
  "miner": "0F",
  "program": "K40"
}
```

### Response Sample

回傳更新之後的結果

```json
{
  "email": "404111111@mail.fju.edu.tw",
  "department": "企業管理學系",
  "nickname": "新鮮小大一",
  "section": "日間部",
  "sec_major": "哲學系",
  "miner": "金融與國際企業學系",
  "program": "動態資訊視覺設計學分學程"
}
```