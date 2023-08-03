# Reminder

Reminders are items that have a date (+ time) attached and sorted by date.

- [List reminders](#list-reminders)
- [Get reminder](#get-reminder)
- [Create reminder](#create-reminder)
- [Update reminder](#update-reminder)
- [Delete reminder](#delete-reminder)

## List reminders

Retrieve all reminders.

Endpoint: `GET` `/api/v1/reminders`

### List reminder response

Status: `200 OK`

```json
{
    "data": [
        {
            "description": "Date night with gf",
            "date": "2023-08-01",
            "start_time": "20:00",
            "end_time": "23:00",
        },
        // ...
    ]
}
```

## Get reminder

Retrieve a single reminder by its uuid.

Endpoint: `GET` `/api/v1/reminders/{uuid}`

### Get reminder response

Status: `200 OK`

```json
{
    "data": {
        "description": "Date night with gf",
        "date": "2023-08-01",
        "start_time": "20:00",
        "end_time": "23:00",
    }
}
```

## Create reminder

Creates a reminder.

Endpoint: `POST` `/api/v1/reminders`

| Field | Required | Description | Format |
|---|---|---|---|
| description | YES | The description of the reminder | min. 2 characters, max. 2500 characters |
| date | YES | The date of the reminder | format `Y-m-d` (2023-08-01) |
| start_time | NO | The start time | format `H:i` (22:00) |
| end_time | NO | The end time | format `H:i` (23:00) |

### Create reminder response

Status: `200 OK`

```json
{
    "data": {
        "description": "Date night with gf",
        "date": "2023-08-01",
        "start_time": "20:00",
        "end_time": "23:00"
    }
}
```

## Update reminder

Update an existing reminder.

Endpoint: `PUT/PATCH` `/api/v1/reminders/{uuid}`

| Field | Required | Description | Format |
|---|---|---|---|
| description | YES | The description of the reminder | min. 2 characters, max. 2500 characters |
| date | YES | The date of the reminder | format `Y-m-d` (2023-08-01) |
| start_time | NO | The start time | format `H:i` (22:00) |
| end_time | NO | The end time | format `H:i` (23:00) |

### Update reminder response

Status: `200 OK`

```json
{
    "data": {
        "description": "Home alone",
        "date": "2023-08-01",
        "start_time": "20:30",
        "end_time": "23:00",
    }
}
```

## Delete reminder

Delete a reminder.

Endpoint: `DELETE` `/api/v1/reminders/{uuid}`

### Delete reminder response

Status: `200 OK`

```json
"OK"
```
