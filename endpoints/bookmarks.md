# Bookmarks

Bookmark is an item that you want to add to the board. The bookmark description can consist of one-or more sentences and can include one-or more URLs.

- [List bookmarks](#list-bookmarks)
- [Get bookmark](#get-bookmark)
- [Create bookmark](#create-bookmark)
- [Update bookmark](#update-bookmark)
- [Delete bookmark](#delete-bookmark)

## List bookmarks

Retrieve all bookmarks of a board.

Endpoint: `GET` `/api/v1/boards/{uuid}/bookmarks`

### List bookmark response

Status: `200 OK`

```json
{
    "data": [
        {
            "uuid": "09045cac-264d-4530-93e3-0292c7879408",
            "description": "test for example.org",
            "formatted_description": "test for <a href=\"example.org\" target=\"_blank\" referrerpolicy=\"origin\" class=\"text-focus-blue hover:underline\">Example Domain</a>",
            "links": [
                {
                    "url": "example.org",
                    "host": "example.org",
                    "favicon": null
                }
            ],
            "categories": [
                {
                    "name": "testing",
                    "bookmarks_count": null
                }
            ]
        },
        // ...
    ]
}
```

## Get bookmark

Retrieve a single bookmark by its UUID.

Endpoint: `GET` `/api/v1/boards/{uuid}/bookmarks/{uuid}`

### Get bookmark response

Status: `200 OK`

```json
{
    "data": {
        "uuid": "09045cac-264d-4530-93e3-0292c7879408",
        "description": "test for example.org",
        "formatted_description": "test for <a href=\"example.org\" target=\"_blank\" referrerpolicy=\"origin\" class=\"text-focus-blue hover:underline\">Example Domain</a>",
        "links": [
            {
                "url": "example.org",
                "host": "example.org",
                "favicon": null
            }
        ],
        "categories": [
            {
                "name": "testing",
                "bookmarks_count": null
            }
        ]
    }
}
```

## Create bookmark

Creates a bookmark.

Endpoint: `POST` `/api/v1/boards/{uuid}/bookmarks`

| Field | Required | Description | Format |
|---|---|---|---|
| description | YES | The content of the bookmark | min. 2 characters, max. 2500 characters |
| categories | NO | The categories to attach to this bookmark | array containing the name of the categories |

### Create bookmark response

Status: `200 OK`

```json
{
    "data": {
        "uuid": "33dea3c8-b013-4e12-b293-358ddbd5e7ee",
        "description": "test for example.org",
        "formatted_description": "test for <a href=\"example.org\" target=\"_blank\" referrerpolicy=\"origin\" class=\"text-focus-blue hover:underline\">Example Domain</a>",
        "links": [
            {
                "url": "example.org",
                "host": "example.org",
                "favicon": null
            }
        ],
        "categories": []
    }
}
```

## Update bookmark

Update an existing bookmark.

Endpoint: `PUT/PATCH` `/api/v1/boards/{uuid}/bookmarks/{uuid}`

| Field | Required | Description | Format |
|---|---|---|---|
| description | YES | The content of the bookmark | min. 2 characters, max. 2500 characters |
| categories | NO | The categories to attach to this bookmark | array containing the name of the categories |

### Update bookmark response

Status: `200 OK`

```json
{
    "data": {
        "uuid": "33dea3c8-b013-4e12-b293-358ddbd5e7ee",
        "description": "test for google.com",
        "formatted_description": "test for <a href=\"google.com\" target=\"_blank\" referrerpolicy=\"origin\" class=\"text-focus-blue hover:underline\">Google</a>",
        "links": [
            {
                "url": "google.com",
                "host": "google.com",
                "favicon": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAMAAABEpIrGAAAAqFBMVEVHcEz7+/v+/v709PX////7+/v09fX4+Pj////8/Pz7+/v////z+PP29vf09PX////+/v7///////////83qlfrQzPsTkFHiPUlpkszf/RAhfX6uwD8wBLW4vyQs/j96N3/+vPh8eR8wJiHrfjylpBhuXftX0rR6Nb608j0qKNwofBKsGWzy/rzn5n0o57uc2/94J78zFb3u7es1rC6z/rHuTCVsC08ooagt3gtAAAAE3RSTlMA08Eb4kVwOqb5kV7jkn8NfnFw9v5R3wAAAVtJREFUOI2dU9lywjAMTIAchgmljU3sJBRycRZoocf//1ltyZ4cpi/dl0jeHWllxY7TxVPgecGT8weCkMQAEgaP6EncwcSShPEAYZ+fDHlZ5BG/P9T1YW8rRnhyYRoXzEeGn0G6XrKlBmNrOJppAVZnmpNftt1gDeSfVbhhwNa3W83Y1hh9aR1eFX/G43N/kjEYyCR/sGcdG4vvWb692jzYnKrgI88znL96RVQrlU3NJWdSgM5FihBv5sKHggSR9gW5FKx1BSGUSHwawQI8ZHl2B8FK4ZgmAjwspMDDKb4obc2nsgIEnrnpzTeltDF8lSbpsb1r2OWdS8Vpp8KiVAWgA+4TesSNFFBOm+bE+U8iqraD47gqJidVQ4NjA1eve4ydS6PgvGw3AfAxL0oOKAvM/fafi4z/YrcrTBx1/9q5vcj54N2QPk3sx+V3JMS3aKgSuUTCjR49zf/jF+G2OgtU1MugAAAAAElFTkSuQmCC"
            }
        ],
        "categories": []
    }
}
```

## Delete bookmark

Delete a bookmark. All links created for this bookmark will be deleted as well.

Endpoint: `DELETE` `/api/v1/boards/{uuid}/bookmarks/{uuid}`

### Delete bookmark response

Status: `200 OK`

```json
"OK"
```
