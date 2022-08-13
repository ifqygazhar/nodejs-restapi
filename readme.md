## Test API

1. Show todolist

```
GET http://localhost:3000
Content-Type: application/json
Accept: application/json
```

Response (Status: OK)

```
HTTP/1.1 200 OK
Content-Type: application/json
Date: Sat, 13 Aug 2022 10:11:29 GMT
Connection: close
Transfer-Encoding: chunked

{
  "code": 200,
  "status": "OK",
  "data": [
    {
      "id": 0,
      "value": "menulis"
    },
    {
      "id": 1,
      "value": "membaca"
    },
    {
      "id": 2,
      "value": "mengoding"
    }
  ]
}
```

2. Create todolist

```
POST http://localhost:3000
Content-Type: application/json
Accept: application/json
```

Request Body

```
{
     "todo": "new todo"
}
```

Response Body (Status CREATE)

```
HTTP/1.1 201 OK
Content-Type: application/json
Date: Sat, 13 Aug 2022 10:12:26 GMT
Connection: close
Transfer-Encoding: chunked

{
  "code": 201,
  "status": "CREATE",
  "data": [
    {
      "id": 0,
      "value": "menulis"
    },
    {
      "id": 1,
      "value": "membaca"
    },
    {
      "id": 2,
      "value": "mengoding"
    },
    {
      "id": 3,
      "value": "new todo"
    }
  ]
}
```

2. Update todolist

```
PUT http://localhost:3000
Content-Type: application/json
Accept: application/json
```

Request Body

```
{
    "id": 1,
    "todo": "update todo"
}
```

Response Body (Status OK)

```
HTTP/1.1 200 OK
Content-Type: application/json
Date: Sat, 13 Aug 2022 10:43:57 GMT
Connection: close
Transfer-Encoding: chunked

{
  "code": 200,
  "status": "OK",
  "data": [
    {
      "id": 0,
      "value": "menulis"
    },
    {
      "id": 1,
      "value": "update todo"
    },
    {
      "id": 2,
      "value": "mengoding"
    },
    {
      "id": 3,
      "value": "new todo"
    }
  ]
}
```

3. Delete todolist

```
DELETE http://localhost:3000
Content-Type: application/json
Accept: application/json
```

Request Body

```
{
    "id": 0
}
```

Response Body (Status OK)

```
HTTP/1.1 200 OK
Content-Type: application/json
Date: Sat, 13 Aug 2022 10:45:21 GMT
Connection: close
Transfer-Encoding: chunked

{
  "code": 200,
  "status": "OK",
  "data": [
    {
      "id": 0,
      "value": "update todo"
    },
    {
      "id": 1,
      "value": "mengoding"
    },
    {
      "id": 2,
      "value": "new todo"
    }
  ]
}
```

## Error response

```
HTTP/1.1 200 OK
Content-Type: application/json
Date: Sat, 13 Aug 2022 10:46:42 GMT
Connection: close
Transfer-Encoding: chunked

{
  "code": 404,
  "status": false,
  "message": "not found"
}
```
