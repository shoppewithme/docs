# Item Options

## Get All Options

```shell
curl "https://api.shoppewith.me/1.1/options"
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "data": [{
    "id": 1,
    "title": "Green",
    "group": <OptionGroup>,
    "user": 7,
  },
  {
    "id": 1,
    "title": "Floral",
    "group": <OptionGroup>,
    "user": 7,
  }],
  "page": 1,
  "count": 10,
  "pages": 100
}
```

This endpoint retrieves all options in a paginated list.

### HTTP Request

`GET /options`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------

## Create New Option

```shell
curl "https://api.shoppewith.me/1.1/options"
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "id": 1,
  "title": "Floral",
  "group": <OptionGroup>,
  "user": 7,
}
```

This endpoint creates a new option and returns it.

### HTTP Request

`POST /options`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------

## Get a Specific Option

```shell
curl "https://api.shoppewith.me/1.1/options/2"
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "id": 1,
  "title": "Floral",
  "group": <OptionGroup>,
  "user": 7,
}
```

This endpoint retrieves a specific option.

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

### HTTP Request

`GET /options/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the option to retrieve

## Delete a Specific Option

```shell
curl "https://api.shoppewith.me/1.1/options/2"
  -X DELETE
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific option.

### HTTP Request

`DELETE https://api.shoppewith.me/1.1/options/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the option to delete
