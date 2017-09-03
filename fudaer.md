# Fudaer 使用者相關 API

- 確認認證信件 | [Confirm Verification](#confirm-verification)
- 重新請求認證信件 | [Request Confirm Verification](#request-confirm-verification)
- 請求忘記/重設 密碼 | [Request Reset Password](#request-reset-password)
- 重設密碼 | [Reset Password](#reset-password)
- 取得使用者資訊 | [Get User Info](#get-user-info)
- 更新使用者資訊 | [Patch User Info](#patch-user-info)

## Confirm Verification

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
