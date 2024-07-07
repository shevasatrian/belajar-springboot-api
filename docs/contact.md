# Contact API Spec

## Create Contact

Endpoint : POST api/contacts

Request Header :

- X-API-TOKEN : Token (Mandatory)

Request Body :

```json
{
  "firstName" : "Sheva",
  "lastName" : "Satrian",
  "email" : "sheva@example.com",
  "phone" : "081271965757"
}
```

Response Body (Success) :

```json
{
  "data" : {
    "id" : "random string",
    "firstName" : "Sheva",
    "lastName" : "Satrian",
    "email" : "sheva@example.com",
    "phone" : "081271965757"
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "Email format invalid, phone format invalid, ..."
}
```

## Update Contact

Endpoint : PUT /api/contacts/{idContact}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Request Body :

```json
{
  "firstName" : "Sheva",
  "lastName" : "Satrian",
  "email" : "sheva@example.com",
  "phone" : "081271965757"
}
```

Response Body (Success) :

```json
{
  "data" : {
    "id" : "random string",
    "firstName" : "Sheva",
    "lastName" : "Satrian",
    "email" : "sheva@example.com",
    "phone" : "081271965757"
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "Email format invalid, phone format invalid, ..."
}
```

## Get Contact

Endpoint : GET /api/contacts/{idContact}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data" : {
    "id" : "random string",
    "firstName" : "Sheva",
    "lastName" : "Satrian",
    "email" : "sheva@example.com",
    "phone" : "081271965757"
  }
}
```

Response Body (Failed, 404) :

```json
{
  "errors" : "Contact is not found"
}
```

## Search Contact

Endpoint : GET /api/contacts

Query Param :

- name : String, contact first name or last name, using like query, optional
- phone : String, contact phone, using like query, optional
- email : String, contact email, using like query, optional
- page : Integer, start from 0, default 0
- size : Integer, default 10

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data" : [
    {
      "id" : "random string",
      "firstName" : "Sheva",
      "lastName" : "Satrian",
      "email" : "sheva@example.com",
      "phone" : "081271965757"
    }
  ],
  "paging" : {
    "currentPage" : 0,
    "totalPage" : 10,
    "size" : 10
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "Unauthorized"
}
```

## Remove Contact

Endpoint : DELETE /api/contacts/{idContact}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data" : "OK"
}
```

Response Body (Failed) :

```json
{
  "errors" : "Contact is not found"
}
```