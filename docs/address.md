# Address API Spec

## Create Address

Endpoint : POST /api/contacts/{idContact}/addresses

Request Header :

- X-API-TOKEN : Token (Mandatory)

Request body :

```json
{
  "street" : "Jalan apa",
  "city" : "Kota",
  "provice" : "provinsi",
  "country" : "Negara",
  "postalCode" : "12313"
}
```

Response body (Success) :

```json
{
  "data" : {
    "id" : "randomstring",
    "street" : "Jalan apa",
    "city" : "Kota",
    "provice" : "provinsi",
    "country" : "Negara",
    "postalCode" : "12313"
  }
}
```

Response body (Failed) :

```json
{
  "errors" : "Contact is not found"
}
```

## Update Address

Endpoint : PUT /api/contacts/{idContact}/addresses/{idAddress}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Request body :

```json
{
  "street" : "Jalan apa",
  "city" : "Kota",
  "provice" : "provinsi",
  "country" : "Negara",
  "postalCode" : "12313"
}
```

Response body (Success) :

```json
{
  "data" : {
    "id" : "randomstring",
    "street" : "Jalan apa",
    "city" : "Kota",
    "provice" : "provinsi",
    "country" : "Negara",
    "postalCode" : "12313"
  }
}
```

Response body (Failed) :

```json
{
  "errors" : "Address is not found"
}
```

## Get Address

Endpoint : GET /api/contacts/{idContact}/addresses/{idAddress}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response body (Success) :

```json
{
  "data" : {
    "id" : "randomstring",
    "street" : "Jalan apa",
    "city" : "Kota",
    "provice" : "provinsi",
    "country" : "Negara",
    "postalCode" : "12313"
  }
}
```

Response body (Failed) :

```json
{
  "errors" : "Address is not found"
}
```

## Remove Address

Endpoint : DELETE /api/contacts/{idContact}/addresses/{idAddress}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response body (Success) :

```json
{
  "data" : "OK"
}
```

Response body (Failed) :

```json
{
  "errors" : "Address is not found"
}
```

## List Address

Endpoint : GET /api/contacts/{idContact}/addresses

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response body (Success) :

```json
{
  "data" : [
    {
      "id" : "randomstring",
      "street" : "Jalan apa",
      "city" : "Kota",
      "provice" : "provinsi",
      "country" : "Negara",
      "postalCode" : "12313"
    }
  ]
}
```

Response body (Failed) :

```json
{
  "errors" : "Contact is not found"
}
```