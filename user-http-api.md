# User HTTP API

User adalah pengguna yang sudah registrasi dan dapat melakukan login ke aplikasi. User dapat melakukan klaim Profile ke satu atau lebih Profile. User yang sudah melakukan klaim Profile dapat melakukan perubahan data Profile.

## Mendapatkan data user yang sedang login

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
  "profiles": [
    {
      "profileId": 1234,
      "status": "ACTIVE"
    }
  ]
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
| profiles | Profile\[\] | Status setiap profile yang terhubung dengan user ini. Status: ACTIVE (terhubung), PENDING (menunggu approval moderator). |

## Link ke Profile

Request aktivasi atau menghubungkan sebuah user dengan Profile tertentu.

Link Profile seharusnya berjalan otomatis untuk user yang memiliki email atau nomor seluler tervalidasi yang persis sama dengan yang terdaftar di data Profil. Untuk melakukan request link Profile secara manual, maka akan divalidasi dulu oleh moderator.

```
POST /api/me/link
Authorization: Bearer {{token}}
Accept: application/json
```

```json
{
  "profileId": 1234
}
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
  "profiles": [
    {
      "profileId": 1234,
      "status": ACTIVE
    }
  ]
}
```
