# Contact API Spec

## Create Contact API

Endpoint : POST /api/contact/

Headers :
-Authorization : token

Request Body :

```json
{
  "first_name": "Edwan",
  "last_name": "Nidzar",
  "email": "one@one.com",
  "phone": "1231321"
}
```

Response Body Success :

```json
{
  "data": {
    "id": 1
    "first_name": "Edwan",
    "last_name": "Nidzar",
    "email": "one@one.com",
    "phone": "1231321"
  }
}
```

Response Body Error :

```json
{
  "errors": "email is not valid"
}
```

## Update Contact API

Endpoint : PUT /api/contacts/:id

Headers :
-Authorization : token

Request Body :

```json
{
  "first_name": "Edwan",
  "last_name": "Nidzar",
  "email": "one@one.com",
  "phone": "1231321"
}
```

Response Body Success :

```json
{
  "data": {
    "id": 1
    "first_name": "Edwan",
    "last_name": "Nidzar",
    "email": "one@one.com",
    "phone": "1231321"
  }
}
```

Response Body Error :

```json
{
  "errors": "email is not valid"
}
```

## Get Contact API

Endpoint : GET /api/contacts:/id

Headers :
-Authorization : token

Response Body Success :

```json
{
  "data": {
    "id": 1
    "first_name": "Edwan",
    "last_name": "Nidzar",
    "email": "one@one.com",
    "phone": "1231321"
  }
}
```

Response Body Error :

```json
{
  "errors": "contact not found"
}
```

## Search Contact API

Endpoint : GET /api/contacts

Headers :
-Authorization : token

Query Params :

- name : search by first_name or last_name, using like query, optional
- email : search by email, using like query, optional
- phone : search by phone, using like query, optional
- page : number of page, default 1
- size : size per page, default 10

Response Body Success :

```json
{
  "data": [
    {
    "id": 1
    "first_name": "Edwan",
    "last_name": "Nidzar",
    "email": "one@one.com",
    "phone": "1231321"
  },
  {
    "id": 2
    "first_name": "Edwan",
    "last_name": "Nidzar",
    "email": "one@one.com",
    "phone": "1231321"
  },
  {
    "id": 3
    "first_name": "Edwan",
    "last_name": "Nidzar",
    "email": "one@one.com",
    "phone": "1231321"
  }
  ],
  "paging": {
    "page" : 1,
    "total_page" : 3,
    "total_item" : 10
  }
}
```

Response Body Error :

## Remove Contact API

Endpoint : DELETE /api/contact/:id

Headers :
-Authorization : token

Response Body Success :

```json
{
  "data": "ok"
}
```

Response Body Error :

```json
{
  "errors": "contact not found"
}
```
