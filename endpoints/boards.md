# Boards

Board is like a workspace that can groups the bookmarks and categories.

- [List boards](#list-boards)
- [Get board](#get-board)
- [Create board](#create-board)
- [Update board](#update-board)
- [Delete board](#delete-board)

## List boards

Retrieve all boards that are bound to the current API token.

Endpoint: `GET` `/api/v1/boards`

### List boards response

Status: `200 OK`

```json
{
    "data": [
        {
            "uuid": "09045cac-264d-4530-93e3-0292c7879408",
            "name": "Project A",
        },
        // ...
    ]
}
```

## Get board

Retrieve a single board by its UUID.

Endpoint: `GET` `/api/v1/boards/{uuid}`

### Get board response

Status: `200 OK`

```json
{
    "data": {
        "uuid": "09045cac-264d-4530-93e3-0292c7879408",
        "name": "Project A",
    }
}
```

## Create board

Creates a board.

> [!NOTE]
> The newly created board is NOT automatically bound to the current API token.

Endpoint: `POST` `/api/v1/boards`

| Field | Required | Description | Format |
|---|---|---|---|
| name | YES | The name of the board | min. 4 characters, max. 20 characters |

### Create board response

Status: `200 OK`

```json
{
    "data": {
        "uuid": "33dea3c8-b013-4e12-b293-358ddbd5e7ee",
        "name": "Project A",
    }
}
```

## Update board

Update an existing board.

Endpoint: `PUT/PATCH` `/api/v1/boards/{uuid}`

| Field | Required | Description | Format |
|---|---|---|---|
| name | YES | The name of the board | min. 4 characters, max. 20 characters |

### Update board response

Status: `200 OK`

```json
{
    "data": {
        "uuid": "33dea3c8-b013-4e12-b293-358ddbd5e7ee",
        "name": "Project B",
    }
}
```

## Delete board

Delete a board. All bookmarks and categories will be deleted as well.

Endpoint: `DELETE` `/api/v1/boards/{uuid}`

### Delete board response

Status: `200 OK`

```json
"OK"
```
