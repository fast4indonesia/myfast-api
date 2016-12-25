# User HTTP API

```
GET /api/me
Authorization: Bearer {{token}}
Accept: application/json
```

Response:

```json
{
  "name": "Yusuf Habibur Rahman",
  "email": "yusuf.h.rahman@gmail.com",
  "emailValidated": true,
  "emails": [
    {
      "email": "yusuf.h.rahman@gmail.com",
      "validated": true
    }
  ],
  "validatedEmails": ["yusuf.h.rahman@gmail.com"],
  "mobileNumber": "+628...",
  "mobileNumberValidated": true,
  "mobileNumbers": [
    {
      "phoneNumber": "+628...",
      "vaidated": true
    }
  ],
  "profileIds": [354, 1734]
}
```

| Field | Type | Description |
| :--- | :--- | :--- |
| name | string | Nama pengguna. |
| email | string | Email utama. |
| emailValidated | boolean | Status validasi email utama. |
| emails | Email\[\] | Semua email beserta status validasinya. |
| mobileNumber | string\[\] | Nomor seluler utama. |
| mobileNumberValidated | boolean | Status validasi nomor seluler utama. |
| mobileNumbers | PhoneNumber\[\] | Semua nomor seluler beserta status validasinya. |
| profileIds | int\[\] | Daftar profile yang terhubung dengan user ini. |



