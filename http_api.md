# HTTP API

Untuk membantu development dan testing, disarankan menggunakan [Postman](https://www.getpostman.com/).

Format menggunakan [hal+json](http://stateless.co/hal_specification.html) dengan `Content-Type: application/hal+json`.

## Autentikasi

Autentikasi menggunakan [JSON Web Tokens \(JWT\)](https://jwt.io/).

Setiap HTTP request ke **semua endpoint kecuali `/api/login**`**, wajib menyertakan `Authorization` header sebagai berikut:

```
Authorization: Bearer {{token}}
```



