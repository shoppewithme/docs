# Items

## Get All Items

```shell
curl "https://api.shoppewith.me/1.1/items"
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "data": [{
    "id": 1,
    "title": "Dress",
    "description": "What a gorgeous dress!",
    "categories": [<Category>,...],
    "options": [<Option>,...],
    "available": true,
    "user": 7,
    "image": "path/to/image.jpg",
    "image_medium": "path/to/image.jpg",
    "image_small": "path/to/image.jpg",
    "image_thumb": "path/to/image.jpg",
    "quantity": 1,
    "price": 65.97
  },
  {
    "id": 2,
    "title": "Shoes",
    "description": "What a gorgeous dress!",
    "categories": [<Category>,...],
    "options": [<Option>,...],
    "available": true,
    "user": 7,
    "image": "path/to/image.jpg",
    "image_medium": "path/to/image.jpg",
    "image_small": "path/to/image.jpg",
    "image_thumb": "path/to/image.jpg",
    "quantity": 23,
    "price": 100
  }],
  "page": 1,
  "count": 10,
  "pages": 100
}
```

This endpoint retrieves all items in a paginated list.

### HTTP Request

`GET /items`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
categories | null | Comma-delimited list of category ids. Items from those categories will be returned.
available | true | If set to false, the result will include only items that are unavailable (quantity < 1 or active=false).
options | null | Comma-delimited list of option ids. The result will include items from those options.
page | 1 | The result will include items from that page.
limit | 10 | The number of items to be returned.
term | null | The result will include items that match that term based on a keyword search.
ids | null | Comma-delimited list of item ids. The result will only return those ids if they exist.

## Create New Item

```shell
curl "https://api.shoppewith.me/1.1/items"
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "title": "Shoes",
  "description": "What a gorgeous dress!",
  "categories": [<Category>,...],
  "options": [<Option>,...],
  "available": true,
  "user": 7,
  "image": "path/to/image.jpg",
  "image_medium": "path/to/image.jpg",
  "image_small": "path/to/image.jpg",
  "image_thumb": "path/to/image.jpg",
  "quantity": 23,
  "price": 100
}
```

This endpoint creates a new item and returns it.

### HTTP Request

`POST /items`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------

## Get a Specific Item

```shell
curl "https://api.shoppewith.me/1.1/items/2"
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "title": "Shoes",
  "description": "What a gorgeous dress!",
  "categories": [<Category>,...],
  "options": [<Option>,...],
  "available": true,
  "user": 7,
  "image": "path/to/image.jpg",
  "image_medium": "path/to/image.jpg",
  "image_small": "path/to/image.jpg",
  "image_thumb": "path/to/image.jpg",
  "quantity": 23,
  "price": 100
}
```

This endpoint retrieves a specific item.

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

### HTTP Request

`GET /items/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the item to retrieve

## Delete a Specific Item

```shell
curl "https://api.shoppewith.me/1.1/items/2"
  -X DELETE
  -H "Authorization: Bearer [authorizationtoken]"
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific item.

### HTTP Request

`DELETE https://api.shoppewith.me/1.1/items/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the item to delete
