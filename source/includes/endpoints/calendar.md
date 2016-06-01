# Calendar

The Teamworks Calendar API allows customers to directly manage events within their organization including event attributes and associated data such as attendees and event reminders.

All Calendar endpoints have the following base resource URI:

`https://www.teamworksapp.com/api/calendar/v1`

<aside class="notice">
All API endpoints must be consumed using SSL.
</aside>

## Create Event

This endpoint creates a new calendar event.

### HTTP Request

`POST /calendars/events`

## List User Events

This endpoint retrieves all the events for the given user. It returns an array of [Event](#event) objects.

### HTTP Request

`GET /calendars/{userId}/events`

### URL Parameters

Parameter | Description
--------- | -----------
userId | The ID of the user you want events for

### Query Filter Parameters

Parameter | Description
--------- | -----------
appointmentTypeId | Only include events with the given appointment type ids
startDate | Specify the start date of the range of events you would like to filter by.  This filter is <b>required</b> for the list of events.  Dates supplied must be in ISO-86001 format, e.g YYYY-MM-DDDD
endDate | Specify the end date of events you would like to filter by.  This filter is <b>required</b> for the list of events.  Dates supplied must be in ISO-86001 format, e.g YYYY-MM-DDDD
fields | List of fields you are interested in. If you only need a list of ids, labels, and attendees then specify those

## Get Event

This endpoint returns an [Event](#event) object for the provided ID.

### HTTP Request

`GET /calendars/events/{eventId}`

### URL Parameters

Parameter | Description
--------- | -----------
eventId | The ID of the event you wish to retrieve

## Update Event

This endpoint updates the event with the given ID. It returns the updated [Event](#event) object.

### HTTP Request

`PUT /calendars/events/{eventId}`

### URL Parameters

Parameter | Description
--------- | -----------
eventId | The ID of the event you want to update

## Delete Event

This endpoint deletes the event with the given ID.

### HTTP Request

`DELETE /calendars/events/{eventId}`

### URL Parameters

Parameter | Description
--------- | -----------
eventId | The ID of the event you want to delete

## List Appointment Types

> This endpoint returns data that looks like this

```json
[
  {
    "label": "Team",
    "id": 310,
    "color": "FF6666"
  },
  {
    "label": "Weights / Conditioning",
    "id": 314,
    "color": "66CC99"
  }
]
```

This endpoint retrieves all available appointment types.

### HTTP Request

`GET /types/appointment`
