# User API Spec

## Registrer User API

Endpoint : POST /api/users

Request Body :

```json
{
  "username": "edwan",
  "password": "edwan",
  "name": "Edwan Nidzar"
}
```

Respond Body Success :

```json
{
  "data": {
    "username": "edwan",
    "name": "Edwan Nidzar"
  }
}
```

Respond Body Error :

```json
{
  "errors": "username already registered"
}
```

## Login User API

Endpoint : POST /api/users/login

Request Body :

```json
{
  "username": "edwan",
  "password": "edwan"
}
```

Respond Body Success :

```json
{
  "data": {
    "token": "unique-token"
  }
}
```

Respond Body Error :

```json
{
  "errors": "username or password wrong!"
}
```

## Update User API

Endpoint : PATCH /api/users/current

Headers :

- Authorization : token

Request Body :

```json
{
  "name": "Edwan Nidzar Baru", // optional
  "password": "edwan baru" // optional
}
```

Respond Body Success :

```json
{
  "data": {
    "name": "Edwan Nidzar Baru",
    "password": "edwan baru"
  }
}
```

Respond Body Error :

```json
{
  "errors": "name max length 100"
}
```

## Get User API

Endpoint : GET /api/users/current

Headers :

- Authorization : token

Respond Body Success :

```json
{
  "data": {
    "username": "edwan",
    "password": "edwan",
    "name": "Edwan Nidzar"
  }
}
```

Respond Body Error :

```json
{
  "errors": "unauthorized"
}
```

## Logout User API

Endpoint : DELETE /api/users/current

Headers :

- Authorization : token

Respond Body Success :

```json
{
  "data": "OK"
}
```

Respond Body Error :

```json
{
  "errors": "unauthorized"
}
```
