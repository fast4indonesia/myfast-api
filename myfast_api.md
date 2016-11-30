# MyFAST API

Disarankan menggunakan [Postman](https://www.getpostman.com/).

Format menggunakan [hal+json](http://stateless.co/hal_specification.html) dengan `Content-Type: application/hal+json`.

## Mencari Anggota berdasarkan Nama

```
GET /api/members/search/findAllByNameTerm?q=yusuf
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
  },
  "_links": {
    "first": {
      "href": "https://my.fast.or.id/api/members/search/findAllByName?q=yusuf&page=0&size=10"
    },
    "self": {
      "href": "https://my.fast.or.id/api/members/search/findAllByName?q=yusuf&size=10"
    },
    "next": {
      "href": "https://my.fast.or.id/api/members/search/findAllByName?q=yusuf&page=1&size=10"
    },
    "last": {
      "href": "https://my.fast.or.id/api/members/search/findAllByName?q=yusuf&page=9&size=10"
    }
  },
  "page": {
    "size": 10,
    "totalElements": 91,
    "totalPages": 10,
    "number": 0
  }}
```
