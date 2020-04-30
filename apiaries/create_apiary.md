# Create an Apiary

## Check near apiaries

Before creating an apiary I have to check if there is no apiary within 500 meters.

**Request**

`GET /apiaries?near=[lat,lng]`

**Response**

Status code: 200

Body:

```json
[{
  "id": 123,
  "name": "Apiary name",
  ...
}]
```

## Create apiary

If no apiaries found or the user want create that apiary anyway.

**Request**

`POST /apiaries`

**Response with no error**

Status code: 200

Body:

```json
{
  "id": 124,
  "name": "Apiary name",
  ...
}
```

**Response if there is an apiary with the same name**

Status code: 400

Body:

```json
{
  "error": "ALREADY_EXITING",
  "message": "...",
}
```

**Response if there is an apiary with the same name**

Status code: 400

Body:

```json
{
  "error": "ALREADY_EXITING",
  "message": "...",
}
```
