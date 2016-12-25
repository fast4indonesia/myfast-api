# Authentication HTTP API

## Login

Request:

```
POST api/login
Accept: application/json
```

```json
{
  "email": "test@example.com"
  "password": "password"
}
```

Response:

```json
{
  "accessToken": "..."
}
```
