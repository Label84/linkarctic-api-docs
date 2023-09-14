# Categories

You can categorize your bookmarks by attaching one-or more categories to them.

- [List categories](#list-categories)
- [Get category](#get-category)
- [Create category](#create-category)
- [Update category](#update-category)
- [Delete category](#delete-category)

## List categories

Retrieve all categories of a board.

Endpoint: `GET` `/api/v1/boards/{uuid}/categories`

### List category response

Status: `200 OK`

```json
{
    "data": [
        {
            "name": "testing",
            "bookmarks_count": 1
        },
        {
            "name": "development",
            "bookmarks_count": 4
        },
        // ...
    ]
}
```

## Get category

Retrieve a single category by its name.

Endpoint: `GET` `/api/v1/boards/{uuid}/categories/{name}`

### Get category response

Status: `200 OK`

```json
{
    "data": {
        "name": "testing",
        "bookmarks_count": null
    }
}
```

## Create category

Creates a category.

Endpoint: `POST` `/api/v1/boards/{uuid}/categories`

| Field | Required | Description | Format |
|---|---|---|---|
| name | YES | The name of the category | unique, min. 2 characters, max. 10 characters |

### Create category response

Status: `200 OK`

```json
{
    "data": {
        "name": "production",
        "bookmarks_count": null
    }
}
```

## Update category

Update an existing category.

Endpoint: `PUT/PATCH` `/api/v1/boards/{uuid}/categories/{name}`

| Field | Required | Description | Format |
|---|---|---|---|
| name | YES | The name of the category | unique, min. 2 characters, max. 10 characters |

### Update category response

Status: `200 OK`

```json
{
    "data": {
        "name": "production-2",
        "bookmarks_count": null
    }
}
```

## Delete category

Delete a category. This will not impact any bookmark that have this category attached.

Endpoint: `DELETE` `/api/v1/boards/{uuid}/categories/{name}`

### Delete category response

Status: `200 OK`

```json
"OK"
```
