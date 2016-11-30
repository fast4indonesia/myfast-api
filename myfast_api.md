# MyFAST API

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
