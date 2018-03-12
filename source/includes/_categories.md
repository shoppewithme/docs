# Categories

## Get All Categories

```shell
curl "https://api.shoppewith.me/1.1/categories"
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "data": [{
    "id": 1,
    "title": "Dress",
    "user": 7,
    "image": "path/to/image.jpg",
    "price": 65.97
  },
  {
    "id": 2,
    "title": "Shoes",
    "user": 7,
    "image": "path/to/image.jpg",
    "price": 100
  }],
  "page": 1,
  "count": 10,
  "pages": 100
}
```

This endpoint retrieves all categories in a paginated list.

### HTTP Request

`GET /categories`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
options_available | false | Returns categories with optional list of available options for each category.

## Create New Category

```shell
curl "https://api.shoppewith.me/1.1/categories"
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "title": "Shoes",
  "user": 7,
  "image": "path/to/image.jpg",
  "price": 100
}
```

This endpoint creates a new category and returns it.

### HTTP Request

`POST /categories`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------

## Get a Specific Category

```shell
curl "https://api.shoppewith.me/1.1/categories/2"
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "title": "Shoes",
  "user": 7,
  "image": "path/to/image.jpg",
  "price": 100
}
```

This endpoint retrieves a specific category.

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

### HTTP Request

`GET /categories/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the category to retrieve

## Delete a Specific Category

```shell
curl "https://api.shoppewith.me/1.1/categories/2"
  -X DELETE
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific category.

### HTTP Request

`DELETE https://api.shoppewith.me/1.1/categories/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the category to delete
