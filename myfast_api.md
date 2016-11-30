# MyFAST API

Disarankan menggunakan [Postman](https://www.getpostman.com/).

## Mencari Anggota berdasarkan Nama

```
GET /api/members/findAllByNameTerm?q=yusuf
```

Hasilnya adalah 

```json
{
  "_embedded": {
    "members": [
      {
        "name": "Yusuf Habibur Rahman"
      }
    ]
  }
}
```
