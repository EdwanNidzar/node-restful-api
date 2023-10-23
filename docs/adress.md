# Addres API Spec

## Create Addres API

Endpoint : POST /api/contacts/:contactId/addresses

Headers :
-Authorization : token

Request Body :

```json
{
  "street": "Jalan Apa",
  "city": "Banjarmasin",
  "province": "Kalsel",
  "country": "Indonesia",
  "postal_code": "70274"
}
```

Response Body Success :

```json
{
  "data": {
    "id": "1",
    "street": "Jalan Apa",
    "city": "Banjarmasin",
    "province": "Kalsel",
    "country": "Indonesia",
    "postal_code": "70274"
  }
}
```

Response Body Error :

```json
{
  "errors": "all field are required"
}
```

## Update Addres API

Endpoint : PUT /api/contacts/:contactId/addresses/:addressId

Headers :
-Authorization : token

Request Body :

```json
{
  "street": "Jalan Apa",
  "city": "Banjarmasin",
  "province": "Kalsel",
  "country": "Indonesia",
  "postal_code": "70274"
}
```

Response Body Success :

```json
{
  "data": {
    "id": "1",
    "street": "Jalan Apa",
    "city": "Banjarmasin",
    "province": "Kalsel",
    "country": "Indonesia",
    "postal_code": "70274"
  }
}
```

Response Body Error :

```json
{
  "errors": "all field are required"
}
```

## Get Addres API

Endpoint : GET /api/contacts/:contactsId/addresses/:addressId

Headers :
-Authorization : token

Response Body Success :

```json
{
  "data": {
    "id": "1",
    "street": "Jalan Apa",
    "city": "Banjarmasin",
    "province": "Kalsel",
    "country": "Indonesia",
    "postal_code": "70274"
  }
}
```

Response Body Error :

```json
{
  "errors": "contact is not found"
}
```

## List Addres API

Endpoint : GET /api/contacts/:contactId/addresses

Headers :
-Authorization : token

Response Body Success :

```json
{
  "data": [
    {
      "id": "1",
      "street": "Jalan Apa",
      "city": "Banjarmasin",
      "province": "Kalsel",
      "country": "Indonesia",
      "postal_code": "70274"
    },
    {
      "id": "2",
      "street": "Jalan Apa",
      "city": "Banjarmasin",
      "province": "Kalsel",
      "country": "Indonesia",
      "postal_code": "70274"
    }
  ]
}
```

Response Body Error :

```json
{
  "errors": "contact is not found"
}
```

## Remove Addres API

Endpoint : DELETE /api/contacts/:contactId/addresses/:addressID

Headers :
-Authorization : token

Response Body Success :

```json
{
  "data": "OK"
}
```

Response Body Error :

```json
{
  "errors": "address is not found"
}
```
