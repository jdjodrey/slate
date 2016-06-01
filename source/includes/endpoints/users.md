# Users

The Teamworks User API allows customers to directly manage the users within their organization including user attributes and associated data such as Contacts and Addresses.

All User endpoints have the following base resource URI:

`https://www.teamworksapp.com/api/user/v2`

<aside class="notice">
All API endpoints must be consumed using SSL.
</aside>

## List Teams

This endpoint retrieves all teams available to a user. It returns an array of [Team](#team) objects.

### HTTP Request

`GET /teams`

## Get Team

This endpoint returns a [Team](#team) object for the specified team ID.

### HTTP Request

`GET /teams/{teamId}`

### URL Parameters

Parameter | Description
--------- | -----------
teamId | The ID of the team to retrieve

## Activate User

This endpoint activates an inactive user for the given team.

### HTTP Request

`POST /teams/{teamId}/users/{userId}/activate`

### URL Parameters

Parameter | Description
--------- | -----------
teamId | The ID of the team this user is on
userId | The ID of the user to activate

## Inactivate User

This endpoint inactivates an active user for the given team.

### HTTP Request

`POST /teams/{teamId}/users/{userId}/inactivate`

### URL Parameters

Parameter | Description
--------- | -----------
teamId | The ID of the team this user is on
userId | The ID of the user to inactivate

## Add User

This endpoint adds an existing user to the given team.

### HTTP Request

`POST /teams/{teamId}/users/{userId}`

### URL Parameters

Parameter | Description
--------- | -----------
teamId | The ID of the team this user is on
userId | The ID of the user to add to this team

## Remove User

This endpoint removes the specified user from the given team.

### HTTP Request

`DELETE /teams/{teamId}/users/{userId}`

### URL Parameters

Parameter | Description
--------- | -----------
teamId | The ID of the team this user is on
userId | The ID of the user to remove from this team

## Get Team User

This endpoint returns a [User](#user) object for the specified user ID on the given team.

### HTTP Request

`GET /teams/{teamId}/users/{userId}`

### URL Parameters

Parameter | Description
--------- | -----------
teamId | The ID of the team this user is on
userId | The ID of the user to retrieve

## List Team Users

This endpoint retrieves all the users on the given team. It returns an array of [User](#user) objects.

### HTTP Request

`GET /teams/{teamId}/users`

### URL Parameters

Parameter | Description
--------- | -----------
teamId | The ID of the team to retrieve users for

### Query Filter Parameters

Parameter | Description
--------- | -----------
userTypes | Specify the user types of the users you want
athleteStatus | Specify the athlete statuses of the athletes you would like returned. By default, only athletes with an "active" status such as "Current" are returned
fields | List of fields you are interested in. If you only need a list of ids, names, and mobile numbers then specify those
active | Specify if you want to return only active users, only inactive users, or all of them. Options are: true, false, all

## Create User

This endpoint creates a new user on the given team.

### HTTP Request

`POST /teams/{teamId}/users`

### URL Parameters

Parameter | Description
--------- | -----------
teamId | The ID of the team to create a user on

## Update User

This endpoint updates attributes for the user on the given team.

### HTTP Request

`PUT /teams/{teamId}/users/{userId}`

### URL Parameters

Parameter | Description
--------- | -----------
teamId | The ID of the team this user is on
userId | The ID of the user to update

## Reset Password

### HTTP Request

`POST /teams/{teamId}/users/{userId}/passwordReset`

### URL Parameters

Parameter | Description
--------- | -----------
teamId | The ID of the team this user is on
userId | The ID of the user to activate
