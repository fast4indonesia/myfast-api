# Tentang HTTP API

Untuk membantu development dan testing, disarankan menggunakan [Postman](https://www.getpostman.com/).

Format menggunakan [hal+json](http://stateless.co/hal_specification.html) dengan `Content-Type: application/hal+json`.

## Autentikasi

Autentikasi menggunakan [JSON Web Tokens \(JWT\)](https://jwt.io/).

Setiap HTTP request ke **semua endpoint kecuali \`/api/login**`**, wajib menyertakan`Authorization\` header sebagai berikut:

```
Authorization: Bearer {{token}}
```

Saat login, JWT token yang dihasilkan oleh server memiliki satu property yaitu **`sub` **dengan **ID user**.

```
sub: {{userId}}
```

## Error

Setiap error harus dikembalikan dengan format `Content-Type: application/json` dengan struktur sebagai berikut:

```json
{
  "timestamp": "2016-12-24T10:48:37.583+0000",
  "status": 403,
  "error": "Forbidden",
  "message":"Access is denied",
  "path": "/api/profiles"
}
```
