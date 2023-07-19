# Bookmark Category

You can attach - add a category to a bookmark, and detach - remove a category from a bookmark.

- [Attach category](#attach-category)
- [Detach category](#detach-category)

## Attach category

Attach a category to a bookmark.

Endpoint: `PUT/PATCH` `/api/v1/bookmarks/{uuid}/categories/{name}`

### Attach category response

Status: `200 OK`

```json
    "data": {
        "uuid": "33dea3c8-b013-4e12-b293-358ddbd5e7ee",
        "description": "just a test",
        "formatted_description": "just a test",
        "links": [],
        "categories": [
            {
                "name": "testing",
                "bookmarks_count": null
            },
            {
                "name": "development",
                "bookmarks_count": null
            },
        ]
    }
```

## Detach category

Detach a category from a bookmark.

Endpoint: `PUT/PATCH` `/api/v1/bookmarks/{uuid}/categories/{name}`

### Detach category response

Status: `200 OK`

```json
    "data": {
        "uuid": "33dea3c8-b013-4e12-b293-358ddbd5e7ee",
        "description": "just a test",
        "formatted_description": "just a test",
        "links": [],
        "categories": [
            {
                "name": "testing",
                "bookmarks_count": null
            },
        ]
    }
```
